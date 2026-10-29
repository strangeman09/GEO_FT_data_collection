# SINDy comparison

Settings per run folder ('k', 'threshold', 'threshold_mode', 'alpha', 'library', 'control', 'anomaly'): [(5, 0.01, 'cv', 0.05, 'poly2', 'diurnal', 'event_mean')]

## Per combo (medians over events)

| combo | n_events | pairwise_jaccard_median | median_active | jaccard_vs_combined_median | jaccard_vs_combined_min | own_r2 | combined_r2 | own_ho_r2 | combined_ho_r2 | own_ho_sim | combined_ho_sim | own_ho_blow | combined_ho_blow |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| d1_bb | 25 | 0.000 | 0.000 | 0.000 | 0.000 | -0.061 | -0.031 | -0.315 | -0.285 | 0.811 | 0.757 | 0.000 | 0.000 |

`own_*` = the event's own model, `combined_*` = the combined model scored on that event; `*_ho_*` = held-out (last fraction of the event, model refit on the first part); `*_sim` = median normalised RMSE of a 4-day simulation (RMSE / data std); `*_blow` = mean fraction of simulations that blew up.

## d1_bb: per event

| event | jaccard_vs_combined | n_active | own_r2 | combined_r2 | own_ho_r2 | combined_ho_r2 | own_ho_sim | combined_ho_sim | own_ho_blow | combined_ho_blow |
|---|---|---|---|---|---|---|---|---|---|---|
| andrew_1992 | 0.000 | 1 | 0.050 | -0.053 | -0.152 | -0.230 | 0.982 | 1.206 | 0.000 | 0.000 |
| bangladesh_1991_1991 | 0.000 | 0 | -0.110 | -0.023 | -8.725 | -0.907 | 0.910 | 0.757 | 0.000 | 0.000 |
| bhola_1970 | 0.000 | 0 | -0.103 | -0.098 | -0.110 | 0.039 | 0.844 | 1.022 | 0.000 | 0.000 |
| camille_1969 | 0.000 | 0 | -0.229 | -0.223 | -0.624 | -0.516 | 0.810 | 0.653 | 0.000 | 0.000 |
| donna_1960 | 0.000 | 0 | -0.122 | -0.091 | -0.647 | -0.642 | 0.674 | 0.675 | 0.000 | 0.000 |
| dorian_2019 | 0.000 | 0 | -0.096 | -0.103 | -0.025 | -0.128 | 0.679 | 0.627 | 0.000 | 0.000 |
| fifi_1974 | 0.000 | 0 | -0.067 | 0.007 | -0.048 | -0.020 | 0.811 | 0.862 | 0.000 | 0.000 |
| great_atlantic_hurricane_1944 | 0.000 | 1 | -0.043 | -0.152 | -1.666 | -2.466 | 1.288 | 1.177 | 0.000 | 0.000 |
| haiyan_2013 | 0.000 | 1 | -0.014 | -0.024 | -0.156 | -0.154 | 0.562 | 0.582 | 0.000 | 0.000 |
| harvey_2017 | 0.000 | 0 | -0.053 | 0.075 | -0.070 | 0.073 | 1.025 | 0.855 | 0.000 | 0.000 |
| hazel_1954 | 0.000 | 0 | -0.045 | -0.044 | -0.287 | -0.275 | 0.792 | 0.764 | 0.000 | 0.000 |
| hugo_1989 | 0.000 | 0 | -0.058 | 0.016 | -0.109 | 0.026 | 0.934 | 0.717 | 0.000 | 0.000 |
| iota_2020 | 0.000 | 1 | 0.013 | -0.029 | -0.119 | 0.007 | 0.764 | 0.690 | 0.000 | 0.000 |
| irma_2017 | 0.000 | 0 | -0.039 | 0.063 | -0.732 | -0.977 | 0.849 | 0.816 | 0.000 | 0.000 |
| ivan_2004 | 0.000 | 0 | -0.111 | -0.066 | -0.262 | -0.221 | 0.583 | 0.583 | 0.000 | 0.000 |
| katrina_2005 | 0.000 | 0 | -0.044 | 0.033 | -3.882 | -1.123 | 1.207 | 0.964 | 0.000 | 0.000 |
| maria_2017 | 0.000 | 0 | -0.098 | -0.100 | -0.213 | -0.391 | 0.520 | 0.684 | 0.000 | 0.000 |
| mitch_1998 | 0.000 | 0 | -0.067 | 0.025 | -2.515 | -2.427 | 0.796 | 0.805 | 0.000 | 0.000 |
| nargis_2008 | 0.000 | 0 | -0.047 | 0.101 | -1.025 | -0.285 | 0.576 | 0.522 | 0.000 | 0.000 |
| nina_1975 | 0.000 | 0 | -0.014 | 0.006 | -1.064 | -1.002 | 0.893 | 0.915 | 0.000 | 0.000 |
| odisha_1999_1999 | 0.000 | 0 | -0.107 | -0.035 | -0.315 | -0.220 | 0.548 | 0.617 | 0.000 | 0.000 |
| sandy_2012 | 0.000 | 0 | -0.038 | 0.061 | -0.580 | -0.413 | 1.297 | 1.235 | 0.000 | 0.000 |
| tip_1979 | 0.000 | 0 | -0.226 | -0.116 | -0.426 | -0.390 | 0.700 | 0.732 | 0.000 | 0.000 |
| vera_1959 | 0.000 | 0 | -0.061 | -0.104 | -0.585 | -0.594 | 0.849 | 0.944 | 0.000 | 0.000 |
| wilma_2005 | 0.000 | 0 | -0.118 | -0.031 | -0.308 | -0.139 | 0.917 | 0.681 | 0.000 | 0.000 |


## Combined models (scored on all data)

| dataset | output | combo | n_samples | n_segments | n_active_terms | threshold | deriv_r2 | sim_nrmse | sim_blowup_frac | heldout_n | heldout_r2 | heldout_sim_nrmse | heldout_blowup_frac |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| dataset1 | backbone | d1_bb | 2567 | 25 | 6 | 0.100 | 0.015 | 0.854 | 0.000 | 648 | 0.008 | 0.778 | 0.000 |

