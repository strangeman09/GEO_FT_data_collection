# SINDy comparison

Settings per run folder ('k', 'threshold', 'threshold_mode', 'alpha', 'library', 'control', 'anomaly'): [(3, 0.01, 'cv', 0.05, 'poly1', 'none', 'event_mean')]

## Per combo (medians over events)

| combo | n_events | pairwise_jaccard_median | median_active | jaccard_vs_combined_median | jaccard_vs_combined_min | own_r2 | combined_r2 | own_ho_r2 | combined_ho_r2 | own_ho_sim | combined_ho_sim | own_ho_blow | combined_ho_blow |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| d2_enc | 25 | 0.667 | 8.000 | 0.778 | 0.111 | 0.592 | 0.565 | 0.411 | 0.502 | 1.128 | 1.033 | 0.000 | 0.000 |

`own_*` = the event's own model, `combined_*` = the combined model scored on that event; `*_ho_*` = held-out (last fraction of the event, model refit on the first part); `*_sim` = median normalised RMSE of a 4-day simulation (RMSE / data std); `*_blow` = mean fraction of simulations that blew up.

## d2_enc: per event

| event | jaccard_vs_combined | n_active | own_r2 | combined_r2 | own_ho_r2 | combined_ho_r2 | own_ho_sim | combined_ho_sim | own_ho_blow | combined_ho_blow |
|---|---|---|---|---|---|---|---|---|---|---|
| andrew_1992 | 1.000 | 9 | 0.612 | 0.341 | 0.087 | 0.372 | 1.293 | 1.162 | 0.000 | 0.000 |
| bangladesh_1991_1991 | 0.556 | 5 | 0.684 | 0.674 | 0.563 | 0.640 | 0.744 | 0.729 | 0.000 | 0.000 |
| bhola_1970 | 0.750 | 12 | 0.845 | 0.787 | 0.375 | 0.790 | 1.059 | 0.941 | 0.000 | 0.000 |
| camille_1969 | 0.111 | 1 | 0.025 | 0.116 | -3.430 | -0.069 | 1.593 | 1.236 | 0.000 | 0.000 |
| donna_1960 | 1.000 | 9 | 0.469 | 0.406 | 0.361 | 0.413 | 1.152 | 1.181 | 0.000 | 0.000 |
| dorian_2019 | 1.000 | 9 | 0.473 | 0.429 | 0.347 | 0.482 | 1.214 | 1.202 | 0.000 | 0.000 |
| fifi_1974 | 0.889 | 8 | 0.725 | 0.681 | 0.516 | 0.625 | 1.128 | 1.097 | 0.000 | 0.000 |
| great_atlantic_hurricane_1944 | 0.750 | 12 | 0.606 | 0.599 | 0.296 | 0.613 | 0.963 | 0.983 | 0.000 | 0.000 |
| haiyan_2013 | 0.667 | 6 | 0.894 | 0.835 | 0.411 | 0.821 | 1.446 | 0.951 | 0.000 | 0.000 |
| harvey_2017 | 0.778 | 7 | 0.484 | 0.138 | 0.513 | 0.199 | 0.885 | 0.939 | 0.000 | 0.000 |
| hazel_1954 | 1.000 | 9 | 0.352 | 0.199 | 0.194 | 0.290 | 0.820 | 0.805 | 0.000 | 0.000 |
| hugo_1989 | 1.000 | 9 | 0.586 | 0.579 | 0.519 | 0.622 | 0.953 | 0.980 | 0.000 | 0.000 |
| iota_2020 | 0.667 | 6 | 0.318 | 0.097 | -1.586 | -0.530 | 1.250 | 1.095 | 0.000 | 0.000 |
| irma_2017 | 0.778 | 7 | 0.645 | 0.565 | 0.638 | 0.644 | 0.835 | 0.902 | 0.000 | 0.000 |
| ivan_2004 | 0.889 | 8 | 0.556 | 0.463 | -1.350 | 0.423 | 1.259 | 1.091 | 0.000 | 0.000 |
| katrina_2005 | 0.818 | 11 | 0.476 | 0.320 | 0.333 | 0.303 | 1.192 | 1.226 | 0.000 | 0.000 |
| maria_2017 | 0.889 | 8 | 0.740 | 0.727 | 0.742 | 0.740 | 1.177 | 1.029 | 0.000 | 0.000 |
| mitch_1998 | 1.000 | 9 | 0.592 | 0.566 | 0.466 | 0.502 | 0.844 | 1.040 | 0.000 | 0.000 |
| nargis_2008 | 0.333 | 3 | 0.727 | 0.728 | 0.826 | 0.742 | 0.743 | 0.779 | 0.000 | 0.000 |
| nina_1975 | 0.750 | 12 | 0.479 | 0.424 | 0.436 | 0.419 | 0.975 | 1.016 | 0.000 | 0.000 |
| odisha_1999_1999 | 0.778 | 7 | 0.768 | 0.742 | 0.502 | 0.708 | 1.288 | 1.033 | 0.000 | 0.000 |
| sandy_2012 | 0.778 | 7 | 0.232 | -0.206 | -0.310 | -0.463 | 0.973 | 1.053 | 0.000 | 0.000 |
| tip_1979 | 0.889 | 8 | 0.754 | 0.697 | 0.750 | 0.569 | 0.998 | 1.076 | 0.000 | 0.000 |
| vera_1959 | 1.000 | 9 | 0.863 | 0.815 | 0.740 | 0.731 | 1.305 | 1.358 | 0.000 | 0.000 |
| wilma_2005 | 0.222 | 2 | -0.489 | 0.034 | -1.285 | 0.108 | 1.407 | 0.965 | 0.000 | 0.000 |


## Combined models (scored on all data)

| dataset | output | combo | n_samples | n_segments | n_active_terms | threshold | deriv_r2 | sim_nrmse | sim_blowup_frac | heldout_n | heldout_r2 | heldout_sim_nrmse | heldout_blowup_frac |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| dataset2 | encoder | d2_enc | 2542 | 25 | 6 | 0.100 | 0.617 | 0.764 | 0.000 | 634 | 0.598 | 0.877 | 0.000 |

