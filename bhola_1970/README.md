# bhola (1970-11-08 to 1970-11-13)

Hourly ERA5 (0.25 deg) through frozen Aurora 1.5. `dataset1` = global, `dataset2` = storm box (`EastPakistan_Bangladesh`, see `bbox.json`).

- `*_encoder_output.npy` (N, 512), `*_backbone_output.npy` (N, 1024): mean over all token axes, one row per hourly input time in `*_times.npy` (inputs are t-6h and t).
- `*_rollout_*`: autoregressive rollout from the event start; `*_rollout_times.npy` are valid times.
- `*_meta.json`: shapes, bbox, region index, variables.
- `track.csv`: IBTrACS best track; `track_hourly_025.csv`: hourly track snapped to the ERA5 grid.
- `visualizations/`: plots.

The 6h prediction and rollout surface fields are not published (too large).

## Files

- `track.csv` (0.00 MB)
- `track_hourly_025.csv` (0.02 MB)
- `bbox.json` (0.00 MB)
- `visualizations/latent_dataset1_global.png` (0.36 MB)
- `visualizations/latent_dataset2_regional.png` (0.56 MB)
- `visualizations/predictions_vs_era5.png` (0.43 MB)
- `visualizations/rollout_vs_era5.png` (0.22 MB)
- `visualizations/snapshots_msl_wind.png` (0.44 MB)
- `visualizations/track_era5_vs_ibtracs.png` (0.13 MB)
- `visualizations/track_hourly_025.png` (0.22 MB)
- `dataset1/bhola_19701108-19701113_global_backbone_output.npy` (1.94 MB)
- `dataset1/bhola_19701108-19701113_global_encoder_output.npy` (0.97 MB)
- `dataset1/bhola_19701108-19701113_global_rollout_backbone_output.npy` (0.09 MB)
- `dataset1/bhola_19701108-19701113_global_rollout_encoder_output.npy` (0.05 MB)
- `dataset1/bhola_19701108-19701113_global_rollout_times.npy` (0.00 MB)
- `dataset1/bhola_19701108-19701113_global_times.npy` (0.00 MB)
- `dataset1/bhola_19701108-19701113_global_meta.json` (0.00 MB)
- `dataset1/bhola_19701108-19701113_global_rollout_meta.json` (0.00 MB)
- `dataset2/bhola_19701108-19701113_EastPakistan_Bangladesh_backbone_output.npy` (1.94 MB)
- `dataset2/bhola_19701108-19701113_EastPakistan_Bangladesh_encoder_output.npy` (0.97 MB)
- `dataset2/bhola_19701108-19701113_EastPakistan_Bangladesh_rollout_backbone_output.npy` (0.09 MB)
- `dataset2/bhola_19701108-19701113_EastPakistan_Bangladesh_rollout_encoder_output.npy` (0.05 MB)
- `dataset2/bhola_19701108-19701113_EastPakistan_Bangladesh_rollout_times.npy` (0.00 MB)
- `dataset2/bhola_19701108-19701113_EastPakistan_Bangladesh_times.npy` (0.00 MB)
- `dataset2/bhola_19701108-19701113_EastPakistan_Bangladesh_meta.json` (0.00 MB)
- `dataset2/bhola_19701108-19701113_EastPakistan_Bangladesh_rollout_meta.json` (0.00 MB)
