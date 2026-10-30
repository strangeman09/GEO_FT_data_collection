# PCA vs UMAP vs t-SNE before SINDy

Code: `geo_ft/sindy_manifold.py` in the aurora-ra repo (https://github.com/aashishvinod/aurora-ra/tree/main/geo_ft); it reuses `sindy_events.py`: same data, 25 events, 4 combos, 6-hourly samples, CV threshold, 75/25 held-out scoring,
per-event + combined fits, continuous and discrete time, team library/control settings per combo.

Files here: [comparison_table.md](comparison_table.md) (96 rows = reducer x dim x combo x continuous/discrete x anomaly mode) and the embedding plots
`emb/<reducer>_<dim>/<anomaly>/traj_<combo>.png` (4 example events coloured by day, pooled embedding by event and by UTC hour), e.g.
[emb/umap_3/event_mean/traj_d2_enc.png](emb/umap_3/event_mean/traj_d2_enc.png) and [emb/pca_3/event_mean/traj_d2_enc.png](emb/pca_3/event_mean/traj_d2_enc.png).
The CSVs (`diagnostics.csv`, `per_event.csv`, `combined_rows.csv`, `comparison_table.csv`), combined equations and `versions.txt` are in aurora-ra under
`geo_ft/sindy_study/manifold/`.

## Verdict

**Neither t-SNE nor UMAP reveals storm dynamics that PCA missed. The only signal anywhere is the time-of-day cycle we already found, and the manifold methods recover it less well than PCA.**

1. **Continuous time (event_mean):** no reducer finds anything. Per-event models are empty or nearly so (0-5/25 non-empty), across all
   continuous runs only one non-empty model beats the zero-derivative baseline (PCA d2_bb k=3; none for UMAP or t-SNE), median per-event held-out R2 is negative everywhere
   (PCA -0.1 to -0.5, UMAP/t-SNE -0.1 to -3.9, i.e. worse), combined held-out R2 <= 0.02 for PCA and <= 0 for UMAP/t-SNE.
2. **Discrete time (event_mean):** the only run with a real held-out signal is the regional encoder (d2_enc), as before.
   PCA: 20/23 (k=3) and 17/23 (k=5) non-empty events beat the no-change baseline, combined R2 0.60. UMAP: 11/21 for both dims, combined 0.50-0.52.
   t-SNE: 13/20 (2-D), 6/17 (3-D), combined 0.43 / 0.28. The d2_bb PCA signal (combined 0.38) is not reproduced by UMAP (-0.26/-0.03) or t-SNE
   (-0.34/-0.14), and the global combos (d1_*) have no signal under any reducer (combined R2 <= 0.13, PCA k=5 only; UMAP/t-SNE negative). So the manifold methods
   never exceed PCA on any combo.
3. **It is time-of-day, not storms.** The signal sits exactly where the embedded coordinates carry a 24h cycle (share of within-event variance at 24h:
   d2_enc 0.23-0.31 for all three reducers; d1 and d2_bb 0.00-0.20) and where lag-1 autocorrelation is low (0.26-0.46 for d2_enc, 0.7-0.99 elsewhere). With
   per-hour means removed (`event_diurnal`) the 24h fraction drops to <= 0.002 and every reducer has held-out R2 <= 0 in discrete and continuous time
   (best combined: PCA d2_enc k=5 discrete 0.003; "own beats baseline" is 0 in 46 of 48 cells; the other two, tsne_3 d1_bb and pca_3 d2_bb discrete, are 1 of 4 non-empty, i.e. noise).
4. **Smoothness diagnostics:** UMAP and t-SNE embeddings of the event-mean anomalies are very smooth in time (UMAP/t-SNE lag-1 AC 0.97-0.998 in the d1 combos and the
   event_diurnal runs, median step 0.01-0.05 std versus 0.10-0.32 for PCA). They track slow within-event drift (which the neighbour graph preserves) and discard the
   fast coordinate structure, so one-step increments are tiny and unpredictable relative to noise: when UMAP k=5 gives many non-empty discrete models
   (up to 20/25 for d1_bb under event_diurnal) they are all worse than no-change (held-out R2 -4 to -8). Only in d2_enc, where the 24h cycle dominates the
   embedding, are the coordinates as rough as PCA's.
5. No evidence for storm dynamics in any embedding; t-SNE/UMAP were not better than PCA in either mode or on any combo.

Caveats: the reducers are fit on all samples including each event's held-out tail (same as the PCA basis; only SINDy is held out). t-SNE has no
out-of-sample map, so its 25-event embedding is a single joint fit and distances between far-apart clusters are not meaningful; its coordinates depend on seed and perplexity
(one seed, perplexity 30, was run). UMAP is fit with `random_state=0` (single-threaded). Medians over "non-empty" models can rest on 1-3 events and be extreme (e.g. -3329); read them with the counts.
The diurnal control of the d1_bb continuous runs is kept under `event_diurnal` for comparability although the per-hour means are already removed.
