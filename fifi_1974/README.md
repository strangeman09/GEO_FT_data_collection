# fifi (1974-09-14 to 1974-09-24)

Hourly ERA5 (0.25 deg) through frozen Aurora 1.5. `dataset1` = global, `dataset2` = storm box (`WCaribbean_Honduras_Mexico`, see `bbox.json`).

- `*_encoder_output.npy` (N, 512), `*_backbone_output.npy` (N, 1024): mean over all token axes, one row per hourly input time in `*_times.npy` (inputs are t-6h and t).
- `*_rollout_*`: autoregressive rollout from the event start; `*_rollout_times.npy` are valid times.
- `*_meta.json`: shapes, bbox, region index, variables.
- `track.csv`: IBTrACS best track; `track_hourly_025.csv`: hourly track snapped to the ERA5 grid.
- `visualizations/`: plots.

The 6h prediction and rollout surface fields are not published (too large).

## Files

- `track.csv` (0.00 MB)
- `track_hourly_025.csv` (0.04 MB)
- `bbox.json` (0.00 MB)
- `visualizations/latent_dataset1_global.png` (0.42 MB)
- `visualizations/latent_dataset2_regional.png` (0.63 MB)
- `visualizations/predictions_vs_era5.png` (0.44 MB)
- `visualizations/rollout_vs_era5.png` (0.25 MB)
- `visualizations/snapshots_msl_wind.png` (0.58 MB)
- `visualizations/track_era5_vs_ibtracs.png` (0.12 MB)
- `visualizations/track_hourly_025.png` (0.21 MB)
- `dataset1/fifi_19740914-19740924_global_backbone_output.npy` (2.43 MB)
- `dataset1/fifi_19740914-19740924_global_encoder_output.npy` (1.22 MB)
- `dataset1/fifi_19740914-19740924_global_rollout_backbone_output.npy` (0.18 MB)
- `dataset1/fifi_19740914-19740924_global_rollout_encoder_output.npy` (0.09 MB)
- `dataset1/fifi_19740914-19740924_global_rollout_times.npy` (0.00 MB)
- `dataset1/fifi_19740914-19740924_global_times.npy` (0.00 MB)
- `dataset1/fifi_19740914-19740924_global_meta.json` (0.00 MB)
- `dataset1/fifi_19740914-19740924_global_rollout_meta.json` (0.00 MB)
- `dataset2/fifi_19740914-19740924_WCaribbean_Honduras_Mexico_backbone_output.npy` (2.43 MB)
- `dataset2/fifi_19740914-19740924_WCaribbean_Honduras_Mexico_encoder_output.npy` (1.22 MB)
- `dataset2/fifi_19740914-19740924_WCaribbean_Honduras_Mexico_rollout_backbone_output.npy` (0.18 MB)
- `dataset2/fifi_19740914-19740924_WCaribbean_Honduras_Mexico_rollout_encoder_output.npy` (0.09 MB)
- `dataset2/fifi_19740914-19740924_WCaribbean_Honduras_Mexico_rollout_times.npy` (0.00 MB)
- `dataset2/fifi_19740914-19740924_WCaribbean_Honduras_Mexico_times.npy` (0.00 MB)
- `dataset2/fifi_19740914-19740924_WCaribbean_Honduras_Mexico_meta.json` (0.00 MB)
- `dataset2/fifi_19740914-19740924_WCaribbean_Honduras_Mexico_rollout_meta.json` (0.00 MB)
