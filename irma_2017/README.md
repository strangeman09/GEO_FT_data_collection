# irma (2017-08-30 to 2017-09-12)

Hourly ERA5 (0.25 deg) through frozen Aurora 1.5. `dataset1` = global, `dataset2` = storm box (`Caribbean_FloridaKeys`, see `bbox.json`).

- `*_encoder_output.npy` (N, 512), `*_backbone_output.npy` (N, 1024): mean over all token axes, one row per hourly input time in `*_times.npy` (inputs are t-6h and t).
- `*_rollout_*`: autoregressive rollout from the event start; `*_rollout_times.npy` are valid times.
- `*_meta.json`: shapes, bbox, region index, variables.
- `track.csv`: IBTrACS best track; `track_hourly_025.csv`: hourly track snapped to the ERA5 grid.
- `visualizations/`: plots.

The 6h prediction and rollout surface fields are not published (too large).

## Files

- `track.csv` (0.01 MB)
- `track_hourly_025.csv` (0.05 MB)
- `bbox.json` (0.00 MB)
- `visualizations/latent_dataset1_global.png` (0.41 MB)
- `visualizations/latent_dataset2_regional.png` (0.64 MB)
- `visualizations/predictions_vs_era5.png` (0.42 MB)
- `visualizations/rollout_vs_era5.png` (0.26 MB)
- `visualizations/snapshots_msl_wind.png` (0.70 MB)
- `visualizations/track_era5_vs_ibtracs.png` (0.14 MB)
- `visualizations/track_hourly_025.png` (0.22 MB)
- `dataset1/irma_20170830-20170912_global_backbone_output.npy` (2.73 MB)
- `dataset1/irma_20170830-20170912_global_encoder_output.npy` (1.36 MB)
- `dataset1/irma_20170830-20170912_global_rollout_backbone_output.npy` (0.23 MB)
- `dataset1/irma_20170830-20170912_global_rollout_encoder_output.npy` (0.11 MB)
- `dataset1/irma_20170830-20170912_global_rollout_times.npy` (0.00 MB)
- `dataset1/irma_20170830-20170912_global_times.npy` (0.01 MB)
- `dataset1/irma_20170830-20170912_global_meta.json` (0.00 MB)
- `dataset1/irma_20170830-20170912_global_rollout_meta.json` (0.00 MB)
- `dataset2/irma_20170830-20170912_Caribbean_FloridaKeys_backbone_output.npy` (2.73 MB)
- `dataset2/irma_20170830-20170912_Caribbean_FloridaKeys_encoder_output.npy` (1.36 MB)
- `dataset2/irma_20170830-20170912_Caribbean_FloridaKeys_rollout_backbone_output.npy` (0.23 MB)
- `dataset2/irma_20170830-20170912_Caribbean_FloridaKeys_rollout_encoder_output.npy` (0.11 MB)
- `dataset2/irma_20170830-20170912_Caribbean_FloridaKeys_rollout_times.npy` (0.00 MB)
- `dataset2/irma_20170830-20170912_Caribbean_FloridaKeys_times.npy` (0.01 MB)
- `dataset2/irma_20170830-20170912_Caribbean_FloridaKeys_meta.json` (0.00 MB)
- `dataset2/irma_20170830-20170912_Caribbean_FloridaKeys_rollout_meta.json` (0.00 MB)
