# ivan (2004-09-02 to 2004-09-24)

Hourly ERA5 (0.25 deg) through frozen Aurora 1.5. `dataset1` = global, `dataset2` = storm box (`Grenada_Jamaica_Alabama`, see `bbox.json`).

- `*_encoder_output.npy` (N, 512), `*_backbone_output.npy` (N, 1024): mean over all token axes, one row per hourly input time in `*_times.npy` (inputs are t-6h and t).
- `*_rollout_*`: autoregressive rollout from the event start; `*_rollout_times.npy` are valid times.
- `*_meta.json`: shapes, bbox, region index, variables.
- `track.csv`: IBTrACS best track; `track_hourly_025.csv`: hourly track snapped to the ERA5 grid.
- `visualizations/`: plots.

The 6h prediction and rollout surface fields are not published (too large).

## Files

- `track.csv` (0.01 MB)
- `track_hourly_025.csv` (0.08 MB)
- `bbox.json` (0.00 MB)
- `visualizations/latent_dataset1_global.png` (0.35 MB)
- `visualizations/latent_dataset2_regional.png` (0.63 MB)
- `visualizations/predictions_vs_era5.png` (0.46 MB)
- `visualizations/rollout_vs_era5.png` (0.31 MB)
- `visualizations/snapshots_msl_wind.png` (0.81 MB)
- `visualizations/track_era5_vs_ibtracs.png` (0.15 MB)
- `visualizations/track_hourly_025.png` (0.22 MB)
- `dataset1/ivan_20040902-20040924_global_backbone_output.npy` (3.61 MB)
- `dataset1/ivan_20040902-20040924_global_encoder_output.npy` (1.81 MB)
- `dataset1/ivan_20040902-20040924_global_rollout_backbone_output.npy` (0.37 MB)
- `dataset1/ivan_20040902-20040924_global_rollout_encoder_output.npy` (0.19 MB)
- `dataset1/ivan_20040902-20040924_global_rollout_times.npy` (0.00 MB)
- `dataset1/ivan_20040902-20040924_global_times.npy` (0.01 MB)
- `dataset1/ivan_20040902-20040924_global_meta.json` (0.00 MB)
- `dataset1/ivan_20040902-20040924_global_rollout_meta.json` (0.00 MB)
- `dataset2/ivan_20040902-20040924_Grenada_Jamaica_Alabama_backbone_output.npy` (3.61 MB)
- `dataset2/ivan_20040902-20040924_Grenada_Jamaica_Alabama_encoder_output.npy` (1.81 MB)
- `dataset2/ivan_20040902-20040924_Grenada_Jamaica_Alabama_rollout_backbone_output.npy` (0.37 MB)
- `dataset2/ivan_20040902-20040924_Grenada_Jamaica_Alabama_rollout_encoder_output.npy` (0.19 MB)
- `dataset2/ivan_20040902-20040924_Grenada_Jamaica_Alabama_rollout_times.npy` (0.00 MB)
- `dataset2/ivan_20040902-20040924_Grenada_Jamaica_Alabama_times.npy` (0.01 MB)
- `dataset2/ivan_20040902-20040924_Grenada_Jamaica_Alabama_meta.json` (0.00 MB)
- `dataset2/ivan_20040902-20040924_Grenada_Jamaica_Alabama_rollout_meta.json` (0.00 MB)
