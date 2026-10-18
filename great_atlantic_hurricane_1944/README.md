# 1944 Great Atlantic Hurricane (IBTrACS 1944253N21302)
Event Sep 9-16 1944, window Sep 2-23 (7 day buffer). Frozen Aurora 1.5.
dataset1 = global, dataset2 = box 12-60N, 276-321E (192x180 cells on the ERA5 0.25 deg grid).

Per dataset (522 hourly samples, input (t-6h, t)):
- *_encoder_output.npy   (522, 512)  mean pooled encoder output
- *_backbone_output.npy  (522, 1024) mean pooled backbone output
- *_times.npy            sample time t (6h prediction valid at t+6h)
- *_rollout_*            same for the 31 step rollout from Sep 9 00Z (6h steps)
- *_meta.json            shapes, settings
track.csv = IBTrACS fixes, track_hourly_025.csv = hourly track snapped to 0.25 deg with
global/box grid indices and the ERA5 centre. Full prediction fields are kept on the server.
