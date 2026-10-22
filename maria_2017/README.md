# maria (2017-09-16 to 2017-09-30)

Hourly ERA5 (0.25 deg) through frozen Aurora 1.5. `dataset1` = global, `dataset2` = storm box (`Dominica_PuertoRico`, see `bbox.json`).

- `*_encoder_output.npy` (N, 512), `*_backbone_output.npy` (N, 1024): mean over all token axes, one row per hourly input time in `*_times.npy` (inputs are t-6h and t).
- `*_rollout_*`: autoregressive rollout from the event start; `*_rollout_times.npy` are valid times.
- `*_meta.json`: shapes, bbox, region index, variables.
- `track.csv`: IBTrACS best track; `track_hourly_025.csv`: hourly track snapped to the ERA5 grid.
- `visualizations/`: plots.

The 6h prediction and rollout surface fields are not published (too large).

## Files

- `track.csv` (0.01 MB)
- `track_hourly_025.csv` (0.06 MB)
- `bbox.json` (0.00 MB)
- `visualizations/latent_dataset1_global.png` (0.36 MB)
- `visualizations/latent_dataset2_regional.png` (0.56 MB)
- `visualizations/predictions_vs_era5.png` (0.41 MB)
- `visualizations/rollout_vs_era5.png` (0.25 MB)
- `visualizations/snapshots_msl_wind.png` (0.85 MB)
- `visualizations/track_era5_vs_ibtracs.png` (0.14 MB)
- `visualizations/track_hourly_025.png` (0.22 MB)
- `dataset1/maria_20170916-20170930_global_backbone_output.npy` (2.83 MB)
- `dataset1/maria_20170916-20170930_global_encoder_output.npy` (1.41 MB)
- `dataset1/maria_20170916-20170930_global_rollout_backbone_output.npy` (0.24 MB)
- `dataset1/maria_20170916-20170930_global_rollout_encoder_output.npy` (0.12 MB)
- `dataset1/maria_20170916-20170930_global_rollout_times.npy` (0.00 MB)
- `dataset1/maria_20170916-20170930_global_times.npy` (0.01 MB)
- `dataset1/maria_20170916-20170930_global_meta.json` (0.00 MB)
- `dataset1/maria_20170916-20170930_global_rollout_meta.json` (0.00 MB)
- `dataset2/maria_20170916-20170930_Dominica_PuertoRico_backbone_output.npy` (2.83 MB)
- `dataset2/maria_20170916-20170930_Dominica_PuertoRico_encoder_output.npy` (1.41 MB)
- `dataset2/maria_20170916-20170930_Dominica_PuertoRico_rollout_backbone_output.npy` (0.24 MB)
- `dataset2/maria_20170916-20170930_Dominica_PuertoRico_rollout_encoder_output.npy` (0.12 MB)
- `dataset2/maria_20170916-20170930_Dominica_PuertoRico_rollout_times.npy` (0.00 MB)
- `dataset2/maria_20170916-20170930_Dominica_PuertoRico_times.npy` (0.01 MB)
- `dataset2/maria_20170916-20170930_Dominica_PuertoRico_meta.json` (0.00 MB)
- `dataset2/maria_20170916-20170930_Dominica_PuertoRico_rollout_meta.json` (0.00 MB)
