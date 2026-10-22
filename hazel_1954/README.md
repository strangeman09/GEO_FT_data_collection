# hazel (1954-10-05 to 1954-10-18)

Hourly ERA5 (0.25 deg) through frozen Aurora 1.5. `dataset1` = global, `dataset2` = storm box (`Windward_Haiti_Carolinas_Toronto`, see `bbox.json`).

- `*_encoder_output.npy` (N, 512), `*_backbone_output.npy` (N, 1024): mean over all token axes, one row per hourly input time in `*_times.npy` (inputs are t-6h and t).
- `*_rollout_*`: autoregressive rollout from the event start; `*_rollout_times.npy` are valid times.
- `*_meta.json`: shapes, bbox, region index, variables.
- `track.csv`: IBTrACS best track; `track_hourly_025.csv`: hourly track snapped to the ERA5 grid.
- `visualizations/`: plots.

The 6h prediction and rollout surface fields are not published (too large).

## Files

- `track.csv` (0.00 MB)
- `track_hourly_025.csv` (0.05 MB)
- `bbox.json` (0.00 MB)
- `visualizations/latent_dataset1_global.png` (0.41 MB)
- `visualizations/latent_dataset2_regional.png` (0.51 MB)
- `visualizations/predictions_vs_era5.png` (0.46 MB)
- `visualizations/rollout_vs_era5.png` (0.26 MB)
- `visualizations/snapshots_msl_wind.png` (0.80 MB)
- `visualizations/track_era5_vs_ibtracs.png` (0.13 MB)
- `visualizations/track_hourly_025.png` (0.22 MB)
- `dataset1/hazel_19541005-19541018_global_backbone_output.npy` (2.73 MB)
- `dataset1/hazel_19541005-19541018_global_encoder_output.npy` (1.36 MB)
- `dataset1/hazel_19541005-19541018_global_rollout_backbone_output.npy` (0.23 MB)
- `dataset1/hazel_19541005-19541018_global_rollout_encoder_output.npy` (0.11 MB)
- `dataset1/hazel_19541005-19541018_global_rollout_times.npy` (0.00 MB)
- `dataset1/hazel_19541005-19541018_global_times.npy` (0.01 MB)
- `dataset1/hazel_19541005-19541018_global_meta.json` (0.00 MB)
- `dataset1/hazel_19541005-19541018_global_rollout_meta.json` (0.00 MB)
- `dataset2/hazel_19541005-19541018_Windward_Haiti_Carolinas_Toronto_backbone_output.npy` (2.73 MB)
- `dataset2/hazel_19541005-19541018_Windward_Haiti_Carolinas_Toronto_encoder_output.npy` (1.36 MB)
- `dataset2/hazel_19541005-19541018_Windward_Haiti_Carolinas_Toronto_rollout_backbone_output.npy` (0.23 MB)
- `dataset2/hazel_19541005-19541018_Windward_Haiti_Carolinas_Toronto_rollout_encoder_output.npy` (0.11 MB)
- `dataset2/hazel_19541005-19541018_Windward_Haiti_Carolinas_Toronto_rollout_times.npy` (0.00 MB)
- `dataset2/hazel_19541005-19541018_Windward_Haiti_Carolinas_Toronto_times.npy` (0.01 MB)
- `dataset2/hazel_19541005-19541018_Windward_Haiti_Carolinas_Toronto_meta.json` (0.00 MB)
- `dataset2/hazel_19541005-19541018_Windward_Haiti_Carolinas_Toronto_rollout_meta.json` (0.00 MB)
