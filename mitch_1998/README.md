# mitch (1998-10-22 to 1998-11-05)

Hourly ERA5 (0.25 deg) through frozen Aurora 1.5. `dataset1` = global, `dataset2` = storm box (`Honduras_Nicaragua_Florida`, see `bbox.json`).

- `*_encoder_output.npy` (N, 512), `*_backbone_output.npy` (N, 1024): mean over all token axes, one row per hourly input time in `*_times.npy` (inputs are t-6h and t).
- `*_rollout_*`: autoregressive rollout from the event start; `*_rollout_times.npy` are valid times.
- `*_meta.json`: shapes, bbox, region index, variables.
- `track.csv`: IBTrACS best track; `track_hourly_025.csv`: hourly track snapped to the ERA5 grid.
- `visualizations/`: plots.

The 6h prediction and rollout surface fields are not published (too large).

## Files

- `track.csv` (0.01 MB)
- `track_hourly_025.csv` (0.07 MB)
- `bbox.json` (0.00 MB)
- `visualizations/latent_dataset1_global.png` (0.40 MB)
- `visualizations/latent_dataset2_regional.png` (0.51 MB)
- `visualizations/predictions_vs_era5.png` (0.37 MB)
- `visualizations/rollout_vs_era5.png` (0.24 MB)
- `visualizations/snapshots_msl_wind.png` (1.17 MB)
- `visualizations/track_era5_vs_ibtracs.png` (0.14 MB)
- `visualizations/track_hourly_025.png` (0.22 MB)
- `dataset1/mitch_19981022-19981105_global_backbone_output.npy` (2.83 MB)
- `dataset1/mitch_19981022-19981105_global_encoder_output.npy` (1.41 MB)
- `dataset1/mitch_19981022-19981105_global_rollout_backbone_output.npy` (0.24 MB)
- `dataset1/mitch_19981022-19981105_global_rollout_encoder_output.npy` (0.12 MB)
- `dataset1/mitch_19981022-19981105_global_rollout_times.npy` (0.00 MB)
- `dataset1/mitch_19981022-19981105_global_times.npy` (0.01 MB)
- `dataset1/mitch_19981022-19981105_global_meta.json` (0.00 MB)
- `dataset1/mitch_19981022-19981105_global_rollout_meta.json` (0.00 MB)
- `dataset2/mitch_19981022-19981105_Honduras_Nicaragua_Florida_backbone_output.npy` (2.83 MB)
- `dataset2/mitch_19981022-19981105_Honduras_Nicaragua_Florida_encoder_output.npy` (1.41 MB)
- `dataset2/mitch_19981022-19981105_Honduras_Nicaragua_Florida_rollout_backbone_output.npy` (0.24 MB)
- `dataset2/mitch_19981022-19981105_Honduras_Nicaragua_Florida_rollout_encoder_output.npy` (0.12 MB)
- `dataset2/mitch_19981022-19981105_Honduras_Nicaragua_Florida_rollout_times.npy` (0.00 MB)
- `dataset2/mitch_19981022-19981105_Honduras_Nicaragua_Florida_times.npy` (0.01 MB)
- `dataset2/mitch_19981022-19981105_Honduras_Nicaragua_Florida_meta.json` (0.00 MB)
- `dataset2/mitch_19981022-19981105_Honduras_Nicaragua_Florida_rollout_meta.json` (0.00 MB)
