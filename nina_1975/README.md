# nina (1975-07-30 to 1975-08-08)

Hourly ERA5 (0.25 deg) through frozen Aurora 1.5. `dataset1` = global, `dataset2` = storm box (`Philippines_Taiwan_China`, see `bbox.json`).

- `*_encoder_output.npy` (N, 512), `*_backbone_output.npy` (N, 1024): mean over all token axes, one row per hourly input time in `*_times.npy` (inputs are t-6h and t).
- `*_rollout_*`: autoregressive rollout from the event start; `*_rollout_times.npy` are valid times.
- `*_meta.json`: shapes, bbox, region index, variables.
- `track.csv`: IBTrACS best track; `track_hourly_025.csv`: hourly track snapped to the ERA5 grid.
- `visualizations/`: plots.

The 6h prediction and rollout surface fields are not published (too large).

## Files

- `track.csv` (0.00 MB)
- `track_hourly_025.csv` (0.03 MB)
- `bbox.json` (0.00 MB)
- `visualizations/latent_dataset1_global.png` (0.37 MB)
- `visualizations/latent_dataset2_regional.png` (0.53 MB)
- `visualizations/predictions_vs_era5.png` (0.43 MB)
- `visualizations/rollout_vs_era5.png` (0.23 MB)
- `visualizations/snapshots_msl_wind.png` (0.62 MB)
- `visualizations/track_era5_vs_ibtracs.png` (0.12 MB)
- `visualizations/track_hourly_025.png` (0.21 MB)
- `dataset1/nina_19750730-19750808_global_backbone_output.npy` (2.33 MB)
- `dataset1/nina_19750730-19750808_global_encoder_output.npy` (1.17 MB)
- `dataset1/nina_19750730-19750808_global_rollout_backbone_output.npy` (0.16 MB)
- `dataset1/nina_19750730-19750808_global_rollout_encoder_output.npy` (0.08 MB)
- `dataset1/nina_19750730-19750808_global_rollout_times.npy` (0.00 MB)
- `dataset1/nina_19750730-19750808_global_times.npy` (0.00 MB)
- `dataset1/nina_19750730-19750808_global_meta.json` (0.00 MB)
- `dataset1/nina_19750730-19750808_global_rollout_meta.json` (0.00 MB)
- `dataset2/nina_19750730-19750808_Philippines_Taiwan_China_backbone_output.npy` (2.33 MB)
- `dataset2/nina_19750730-19750808_Philippines_Taiwan_China_encoder_output.npy` (1.17 MB)
- `dataset2/nina_19750730-19750808_Philippines_Taiwan_China_rollout_backbone_output.npy` (0.16 MB)
- `dataset2/nina_19750730-19750808_Philippines_Taiwan_China_rollout_encoder_output.npy` (0.08 MB)
- `dataset2/nina_19750730-19750808_Philippines_Taiwan_China_rollout_times.npy` (0.00 MB)
- `dataset2/nina_19750730-19750808_Philippines_Taiwan_China_times.npy` (0.00 MB)
- `dataset2/nina_19750730-19750808_Philippines_Taiwan_China_meta.json` (0.00 MB)
- `dataset2/nina_19750730-19750808_Philippines_Taiwan_China_rollout_meta.json` (0.00 MB)
