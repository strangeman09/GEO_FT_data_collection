# camille (1969-08-14 to 1969-08-22)

Hourly ERA5 (0.25 deg) through frozen Aurora 1.5. `dataset1` = global, `dataset2` = storm box (`Cayman_MississippiCoast_Virginia`, see `bbox.json`).

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
- `visualizations/latent_dataset1_global.png` (0.39 MB)
- `visualizations/latent_dataset2_regional.png` (0.57 MB)
- `visualizations/predictions_vs_era5.png` (0.45 MB)
- `visualizations/rollout_vs_era5.png` (0.23 MB)
- `visualizations/snapshots_msl_wind.png` (0.66 MB)
- `visualizations/track_era5_vs_ibtracs.png` (0.12 MB)
- `visualizations/track_hourly_025.png` (0.20 MB)
- `dataset1/camille_19690814-19690822_global_backbone_output.npy` (2.24 MB)
- `dataset1/camille_19690814-19690822_global_encoder_output.npy` (1.12 MB)
- `dataset1/camille_19690814-19690822_global_rollout_backbone_output.npy` (0.14 MB)
- `dataset1/camille_19690814-19690822_global_rollout_encoder_output.npy` (0.07 MB)
- `dataset1/camille_19690814-19690822_global_rollout_times.npy` (0.00 MB)
- `dataset1/camille_19690814-19690822_global_times.npy` (0.00 MB)
- `dataset1/camille_19690814-19690822_global_meta.json` (0.00 MB)
- `dataset1/camille_19690814-19690822_global_rollout_meta.json` (0.00 MB)
- `dataset2/camille_19690814-19690822_Cayman_MississippiCoast_Virginia_backbone_output.npy` (2.24 MB)
- `dataset2/camille_19690814-19690822_Cayman_MississippiCoast_Virginia_encoder_output.npy` (1.12 MB)
- `dataset2/camille_19690814-19690822_Cayman_MississippiCoast_Virginia_rollout_backbone_output.npy` (0.14 MB)
- `dataset2/camille_19690814-19690822_Cayman_MississippiCoast_Virginia_rollout_encoder_output.npy` (0.07 MB)
- `dataset2/camille_19690814-19690822_Cayman_MississippiCoast_Virginia_rollout_times.npy` (0.00 MB)
- `dataset2/camille_19690814-19690822_Cayman_MississippiCoast_Virginia_times.npy` (0.00 MB)
- `dataset2/camille_19690814-19690822_Cayman_MississippiCoast_Virginia_meta.json` (0.00 MB)
- `dataset2/camille_19690814-19690822_Cayman_MississippiCoast_Virginia_rollout_meta.json` (0.00 MB)
