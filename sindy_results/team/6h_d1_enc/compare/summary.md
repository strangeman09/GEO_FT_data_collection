# SINDy comparison

Settings per run folder ('k', 'threshold', 'threshold_mode', 'alpha', 'library', 'control', 'anomaly'): [(5, 0.01, 'cv', 0.05, 'poly2', 'none', 'event_mean')]

## Per combo (medians over events)

| combo | n_events | pairwise_jaccard_median | median_active | jaccard_vs_combined_median | jaccard_vs_combined_min | own_r2 | combined_r2 | own_ho_r2 | combined_ho_r2 | own_ho_sim | combined_ho_sim | own_ho_blow | combined_ho_blow |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| d1_enc | 25 | nan | 0.000 | 0.000 | 0.000 | -0.108 | 0.065 | -0.260 | -0.207 | 0.829 | 0.785 | 0.000 | 0.000 |

`own_*` = the event's own model, `combined_*` = the combined model scored on that event; `*_ho_*` = held-out (last fraction of the event, model refit on the first part); `*_sim` = median normalised RMSE of a 4-day simulation (RMSE / data std); `*_blow` = mean fraction of simulations that blew up.

## d1_enc: per event

| event | jaccard_vs_combined | n_active | own_r2 | combined_r2 | own_ho_r2 | combined_ho_r2 | own_ho_sim | combined_ho_sim | own_ho_blow | combined_ho_blow |
|---|---|---|---|---|---|---|---|---|---|---|
| andrew_1992 | 0.000 | 0 | -0.113 | -0.026 | -0.118 | -0.051 | 0.725 | 0.631 | 0.000 | 0.000 |
| bangladesh_1991_1991 | 0.000 | 0 | -0.205 | -0.513 | -1.654 | -1.622 | 0.975 | 0.844 | 0.000 | 0.000 |
| bhola_1970 | 0.000 | 0 | -0.133 | -0.059 | -0.117 | -0.137 | 0.817 | 0.785 | 0.000 | 0.000 |
| camille_1969 | 0.000 | 0 | -0.202 | 0.020 | -0.295 | -0.159 | 0.859 | 0.794 | 0.000 | 0.000 |
| donna_1960 | 0.000 | 0 | -0.153 | 0.069 | -0.774 | -0.774 | 0.807 | 0.803 | 0.000 | 0.000 |
| dorian_2019 | 0.000 | 0 | -0.107 | 0.121 | -0.178 | -0.087 | 0.692 | 0.495 | 0.000 | 0.000 |
| fifi_1974 | 0.000 | 0 | -0.117 | 0.006 | -0.143 | -0.343 | 0.682 | 0.672 | 0.000 | 0.000 |
| great_atlantic_hurricane_1944 | 0.000 | 0 | -0.050 | 0.088 | -3.367 | -3.751 | 1.364 | 1.487 | 0.000 | 0.000 |
| haiyan_2013 | 0.000 | 0 | -0.176 | 0.077 | -0.303 | -0.279 | 0.720 | 0.755 | 0.000 | 0.000 |
| harvey_2017 | 0.000 | 0 | -0.108 | 0.163 | -0.395 | -0.275 | 0.916 | 0.684 | 0.000 | 0.000 |
| hazel_1954 | 0.000 | 0 | -0.074 | 0.022 | -0.231 | -0.265 | 0.925 | 0.985 | 0.000 | 0.000 |
| hugo_1989 | 0.000 | 0 | -0.059 | 0.065 | -0.047 | 0.012 | 0.838 | 0.789 | 0.000 | 0.000 |
| iota_2020 | 0.000 | 0 | -0.087 | -0.010 | -0.035 | -0.033 | 0.829 | 0.937 | 0.000 | 0.000 |
| irma_2017 | 0.000 | 0 | -0.090 | 0.158 | -0.720 | -1.444 | 0.779 | 0.868 | 0.000 | 0.000 |
| ivan_2004 | 0.000 | 0 | -0.143 | -0.008 | -0.648 | -0.702 | 0.433 | 0.437 | 0.000 | 0.000 |
| katrina_2005 | 0.000 | 0 | -0.050 | 0.041 | -4.465 | -0.229 | 0.734 | 0.663 | 0.000 | 0.000 |
| maria_2017 | 0.000 | 0 | -0.205 | -0.042 | -0.237 | -0.207 | 0.478 | 0.562 | 0.000 | 0.000 |
| mitch_1998 | 0.000 | 0 | -0.068 | 0.036 | -1.065 | -1.170 | 0.959 | 0.951 | 0.000 | 0.000 |
| nargis_2008 | 0.000 | 0 | -0.049 | 0.137 | -0.444 | 0.143 | 0.881 | 0.461 | 0.000 | 0.000 |
| nina_1975 | 0.000 | 0 | -0.009 | -0.002 | -0.149 | -0.063 | 1.317 | 1.264 | 0.000 | 0.000 |
| odisha_1999_1999 | 0.000 | 0 | -0.115 | 0.074 | -0.190 | -0.044 | 0.786 | 0.582 | 0.000 | 0.000 |
| sandy_2012 | 0.000 | 0 | -0.105 | 0.159 | -1.745 | -0.827 | 1.115 | 0.841 | 0.000 | 0.000 |
| tip_1979 | 0.000 | 0 | -0.211 | 0.135 | -0.260 | -0.159 | 0.531 | 0.554 | 0.000 | 0.000 |
| vera_1959 | 0.000 | 0 | -0.073 | 0.122 | -0.114 | 0.021 | 0.859 | 0.778 | 0.000 | 0.000 |
| wilma_2005 | 0.000 | 0 | -0.135 | 0.070 | -0.117 | -0.037 | 0.863 | 0.790 | 0.000 | 0.000 |


## Combined models (scored on all data)

| dataset | output | combo | n_samples | n_segments | n_active_terms | threshold | deriv_r2 | sim_nrmse | sim_blowup_frac | heldout_n | heldout_r2 | heldout_sim_nrmse | heldout_blowup_frac |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| dataset1 | encoder | d1_enc | 2567 | 25 | 15 | 0.030 | 0.103 | 0.562 | 0.000 | 648 | 0.021 | 0.596 | 0.000 |

