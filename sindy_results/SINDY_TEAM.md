# SINDy step: running your events

You fit sparse ODEs / maps (pysindy) to the mean-pooled Aurora latents of **your** events, using the PCA basis that is
already fitted on all 25 events (`geo_ft/sindy_basis/`, event-mean anomalies). Nobody refits the basis, so everyone's
equations are in the same coordinates. No GPU, no ERA5, no `GEO_FT_ROOT`: it only reads the published latents.
Takes a few minutes on a laptop. Commands are bash (Linux server, WSL, or Git Bash on Windows).

| Person | Events |
|---|---|
| Aabhwan | irma_2017 maria_2017 dorian_2019 iota_2020 hugo_1989 nargis_2008 haiyan_2013 sandy_2012 |
| Abdul | hazel_1954 donna_1960 camille_1969 fifi_1974 vera_1959 nina_1975 bhola_1970 harvey_2017 |

(The names are the folder names in the data repo, `<event>_<year>`.)

## 1. Setup (once)

```bash
# Python >= 3.11. Use your aurora_v15 env or any other.
pip install pysindy==2.1.0 scikit-learn scipy numpy pandas matplotlib
# tested with: Python 3.14, pysindy 2.1.0, scikit-learn 1.9.1, scipy 1.18.1, numpy 2.5.1, pandas 3.0.5, matplotlib 3.11.2
# (on Python 3.11 pip picks older numpy/scipy; pysindy 2.1.0 is the one that matters, the 2.x API differs from 1.x)

python -m zipfile -e geo_ft_sindy.zip .       # creates aurora-ra/  (or: unzip geo_ft_sindy.zip)
git clone https://github.com/strangeman09/GEO_FT_data_collection.git     # the latents, all 25 events (git pull for updates)
cd aurora-ra
```

Run everything below from the `aurora-ra/` folder.

## 2. Check your install (10 seconds)

```bash
python geo_ft/sindy_events.py selftest
```

It must print `support recovered exactly: True` (Lorenz), a control test, and the Henon map
`z0[k+1] = +1.000 1 +1.000 z1 -1.400 z0^2` / `z1[k+1] = +0.300 z0`. If it crashes, send me the traceback.

## 3. Fit your events

Pick your block, then paste the rest as is. `DATA` is the path of the cloned data repo (the folder that contains
`irma_2017/` etc.).

```bash
# --- Aabhwan ---
NAME=aabhwan
EVENTS="irma_2017 maria_2017 dorian_2019 iota_2020 hugo_1989 nargis_2008 haiyan_2013 sandy_2012"
# --- Abdul (use these two lines instead) ---
# NAME=abdul
# EVENTS="hazel_1954 donna_1960 camille_1969 fifi_1974 vera_1959 nina_1975 bhola_1970 harvey_2017"

DATA=../GEO_FT_data_collection      # adjust if you cloned elsewhere
OUT=sindy_$NAME
run() { python geo_ft/sindy_events.py fit --data_root "$DATA" --basis_dir geo_ft/sindy_basis \
        --events $EVENTS --threshold_mode cv "$@"; }

# 6-hourly continuous-time SINDy, recommended settings per combo
run --out_dir $OUT/6h_d1_enc --combos d1_enc --k 5 --library poly2
run --out_dir $OUT/6h_d1_bb  --combos d1_bb  --k 5 --library poly2 --control diurnal
run --out_dir $OUT/6h_d2     --combos d2_enc d2_bb --k 3 --library poly1

# discrete-time SINDy, z(t+1) = f(z(t)), recommended settings per combo
run --out_dir $OUT/discrete_k5 --combos d1_enc d1_bb d2_bb --k 5 --library poly1 --discrete
run --out_dir $OUT/discrete_k3 --combos d2_enc            --k 3 --library poly1 --discrete
```

Notes: d1 = global run, d2 = regional box; enc = encoder, bb = backbone. The threshold is chosen per fit by blocked
time-series cross-validation. Each command prints one line per event and combo. If you re-run, existing event folders
are skipped (`SKIP ... exists`); delete the folder or add `--overwrite`.

## 4. What to look at

Each output folder has one sub-folder per event, containing:

- `equations_<combo>.txt`: the discovered equations. For the 6h runs `(z0)' = ...`; for `discrete_*` `z0[k+1] = ...`
  (the `z_i` term with coefficient near 1 is just persistence). `(z0)' = 0` means CV found nothing predictable: for the
  6h continuous runs that is the usual outcome for a single event.
- `metrics.csv`, one row per combo: `n_active_terms`, `threshold` (chosen), `deriv_r2` (in-sample), and the held-out
  columns `heldout_r2`, `heldout_sim_nrmse`, `heldout_blowup_frac` (model refit on the first 75% of the event, scored on
  the last 25%). A `heldout_r2` clearly above 0 means the model beats "predict no change / zero derivative"; negative
  means it does not. For `discrete_*` the R² is on the increment z(t+1) - z(t).
- `coefficients.csv`, `config.json`: all coefficients (zeros included) and the settings used.

There are no plots at this step; the heatmaps and the comparison with the combined model come from `compare`, which I
run after collecting everyone's folders. Just glance at `metrics.csv` and the equations of one or two events.

## 5. Send back

```bash
python -m zipfile -c sindy_$NAME.zip sindy_$NAME
```

Send me `sindy_$NAME.zip` (under 1 MB).
