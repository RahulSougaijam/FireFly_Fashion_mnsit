# V8 results summary (auto-generated)

## Test metrics
```
                               Accuracy          Precision             Recall                 F1                AUC          Test loss  Params Epochs Train time (s)
Model                                                                                                                                                               
Default CNN           0.9159 +/- 0.0029  0.9161 +/- 0.0030  0.9159 +/- 0.0029  0.9157 +/- 0.0030  0.9948 +/- 0.0003  0.2386 +/- 0.0063  421642   14.2             35
V7-selected (frozen)  0.9163 +/- 0.0016  0.9167 +/- 0.0015  0.9163 +/- 0.0016  0.9161 +/- 0.0015  0.9950 +/- 0.0002  0.2369 +/- 0.0050  389964   17.2             42
Strong manual recipe  0.9305 +/- 0.0019  0.9306 +/- 0.0018  0.9305 +/- 0.0019  0.9305 +/- 0.0019  0.9962 +/- 0.0001  0.1967 +/- 0.0038  521098   30.0            239
FA-selected (V8)      0.9353 +/- 0.0012  0.9356 +/- 0.0012  0.9353 +/- 0.0012  0.9353 +/- 0.0012  0.9967 +/- 0.0001  0.1935 +/- 0.0026  314331   30.0            480
RS-selected (V8)      0.9336 +/- 0.0012  0.9338 +/- 0.0012  0.9336 +/- 0.0012  0.9336 +/- 0.0012  0.9966 +/- 0.0001  0.1908 +/- 0.0025  433489   30.0            282
```

## Pairwise tests (pp)
```
                                    comparison  mean_diff_pp  ci95_low_pp  ci95_high_pp  t_test_p  wilcoxon_p  cohens_dz  tost_p  n_seeds  holm_p_all_pairs  primary  holm_p_primary
0           Default CNN - V7-selected (frozen)       -0.0425      -0.1942        0.1467    0.6452      0.2925    -0.1366  0.0002       12            0.6452    False             NaN
1           Default CNN - Strong manual recipe       -1.4617      -1.6725       -1.2283    0.0000      0.0005    -3.5860  1.0000       12            0.0000    False             NaN
2               Default CNN - FA-selected (V8)       -1.9375      -2.0917       -1.7708    0.0000      0.0005    -6.6299  1.0000       12            0.0000     True          0.0000
3               Default CNN - RS-selected (V8)       -1.7675      -1.9475       -1.5792    0.0000      0.0005    -5.2891  1.0000       12            0.0000    False             NaN
4  V7-selected (frozen) - Strong manual recipe       -1.4192      -1.5183       -1.3075    0.0000      0.0005    -7.2794  1.0000       12            0.0000    False             NaN
5      V7-selected (frozen) - FA-selected (V8)       -1.8950      -1.9767       -1.8158    0.0000      0.0005   -12.6899  1.0000       12            0.0000    False             NaN
6      V7-selected (frozen) - RS-selected (V8)       -1.7250      -1.8233       -1.6200    0.0000      0.0005    -9.0653  1.0000       12            0.0000    False             NaN
7      Strong manual recipe - FA-selected (V8)       -0.4758      -0.5867       -0.3567    0.0000      0.0005    -2.2534  0.3497       12            0.0000     True          0.0000
8      Strong manual recipe - RS-selected (V8)       -0.3058      -0.4000       -0.2183    0.0001      0.0005    -1.7906  0.0012       12            0.0002    False             NaN
9          FA-selected (V8) - RS-selected (V8)        0.1700       0.0883        0.2500    0.0027      0.0078     1.1135  0.0000       12            0.0053     True          0.0027
```

## Generalization
```
                              Train acc            Val acc           Test acc     Gap train-test       Gap val-test         Train loss           Val loss          Test loss
Default CNN           0.9517 +/- 0.0064  0.9252 +/- 0.0022  0.9159 +/- 0.0029  0.0358 +/- 0.0051  0.0093 +/- 0.0025  0.1343 +/- 0.0163  0.2108 +/- 0.0041  0.2386 +/- 0.0063
V7-selected (frozen)  0.9538 +/- 0.0047  0.9263 +/- 0.0026  0.9163 +/- 0.0016  0.0374 +/- 0.0053  0.0099 +/- 0.0019  0.1256 +/- 0.0105  0.2102 +/- 0.0041  0.2369 +/- 0.0050
Strong manual recipe  0.9491 +/- 0.0015  0.9368 +/- 0.0016  0.9305 +/- 0.0019  0.0186 +/- 0.0023  0.0063 +/- 0.0024  0.1361 +/- 0.0031  0.1765 +/- 0.0040  0.1967 +/- 0.0038
FA-selected (V8)      0.9694 +/- 0.0016  0.9417 +/- 0.0012  0.9353 +/- 0.0012  0.0341 +/- 0.0019  0.0064 +/- 0.0014  0.0831 +/- 0.0036  0.1746 +/- 0.0035  0.1935 +/- 0.0026
RS-selected (V8)      0.9632 +/- 0.0016  0.9389 +/- 0.0008  0.9336 +/- 0.0012  0.0296 +/- 0.0021  0.0053 +/- 0.0014  0.1013 +/- 0.0028  0.1732 +/- 0.0032  0.1908 +/- 0.0025
```

## Toy benchmarks
```
     function  evaluations_per_run  runs  FA_median   RS_median  FA_better_in_runs  mannwhitney_p_FA_smaller
0      Sphere                 2000    30   0.000007   17.942571                 30                       0.0
1   Rastrigin                 2000    30  15.920600   83.711949                 30                       0.0
2  Rosenbrock                 2000    30   8.066106  308.087231                 30                       0.0
```
