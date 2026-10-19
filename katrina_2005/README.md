# Hurricane Katrina 2005 (IBTrACS 2005236N23285)
Event Aug 23-31 2005, window Aug 16 - Sep 7 (7 day buffer). Frozen Aurora 1.5.
dataset1 = global, dataset2 = box 15-49N, 262-293E (136x124 cells on the ERA5 0.25 deg grid).
ERA5 from CDS + ARCO-ERA5 (Google Cloud copy of ERA5, checked to match CDS to rounding level).

Per dataset (546 hourly samples, input (t-6h, t)):
- *_encoder_output.npy   (546, 512)  mean pooled encoder output
- *_backbone_output.npy  (546, 1024) mean pooled backbone output
- *_times.npy            sample time t (6h prediction valid at t+6h)
- *_rollout_*            same for the 35 step rollout from Aug 23 00Z (6h steps)
- *_meta.json            shapes, settings
track.csv = IBTrACS fixes, track_hourly_025.csv = hourly track snapped to 0.25 deg with
global/box grid indices and the ERA5 centre. Full prediction fields are kept on the server.
