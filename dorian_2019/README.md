# dorian (2019-08-24 to 2019-09-07)

Hourly ERA5 (0.25 deg) through frozen Aurora 1.5. `dataset1` = global, `dataset2` = storm box (`Bahamas_Carolinas_NovaScotia`, see `bbox.json`).

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
- `visualizations/latent_dataset1_global.png` (0.37 MB)
- `visualizations/latent_dataset2_regional.png` (0.54 MB)
- `visualizations/predictions_vs_era5.png` (0.42 MB)
- `visualizations/rollout_vs_era5.png` (0.25 MB)
- `visualizations/snapshots_msl_wind.png` (0.80 MB)
- `visualizations/track_era5_vs_ibtracs.png` (0.14 MB)
- `visualizations/track_hourly_025.png` (0.23 MB)
- `dataset1/dorian_20190824-20190907_global_backbone_output.npy` (2.83 MB)
- `dataset1/dorian_20190824-20190907_global_encoder_output.npy` (1.41 MB)
- `dataset1/dorian_20190824-20190907_global_rollout_backbone_output.npy` (0.24 MB)
- `dataset1/dorian_20190824-20190907_global_rollout_encoder_output.npy` (0.12 MB)
- `dataset1/dorian_20190824-20190907_global_rollout_times.npy` (0.00 MB)
- `dataset1/dorian_20190824-20190907_global_times.npy` (0.01 MB)
- `dataset1/dorian_20190824-20190907_global_meta.json` (0.00 MB)
- `dataset1/dorian_20190824-20190907_global_rollout_meta.json` (0.00 MB)
- `dataset2/dorian_20190824-20190907_Bahamas_Carolinas_NovaScotia_backbone_output.npy` (2.83 MB)
- `dataset2/dorian_20190824-20190907_Bahamas_Carolinas_NovaScotia_encoder_output.npy` (1.41 MB)
- `dataset2/dorian_20190824-20190907_Bahamas_Carolinas_NovaScotia_rollout_backbone_output.npy` (0.24 MB)
- `dataset2/dorian_20190824-20190907_Bahamas_Carolinas_NovaScotia_rollout_encoder_output.npy` (0.12 MB)
- `dataset2/dorian_20190824-20190907_Bahamas_Carolinas_NovaScotia_rollout_times.npy` (0.00 MB)
- `dataset2/dorian_20190824-20190907_Bahamas_Carolinas_NovaScotia_times.npy` (0.01 MB)
- `dataset2/dorian_20190824-20190907_Bahamas_Carolinas_NovaScotia_meta.json` (0.00 MB)
- `dataset2/dorian_20190824-20190907_Bahamas_Carolinas_NovaScotia_rollout_meta.json` (0.00 MB)
