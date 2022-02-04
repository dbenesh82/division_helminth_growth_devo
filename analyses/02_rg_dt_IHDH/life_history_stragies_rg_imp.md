Life history strategies
================

-   [Optimal life history strategies?](#optimal-life-history-strategies)
    -   [Non-taxonomic models](#non-taxonomic-models)
    -   [Taxonomic mixed models](#taxonomic-mixed-models)
    -   [Model parameters](#model-parameters)
        -   [Larval growth](#larval-growth)
        -   [Larval development](#larval-development)
        -   [Adult growth](#adult-growth)
        -   [Adult development](#adult-development)
        -   [Size at maturity](#size-at-maturity)
        -   [Age at maturity](#age-at-maturity)
    -   [Plotted model predictions - Figs 3 and
        4](#plotted-model-predictions---figs-3-and-4)
    -   [Model effect sizes](#model-effect-sizes)
-   [Trait covariation](#trait-covariation)
    -   [Taxonomic trait covariation](#taxonomic-trait-covariation)
        -   [Correlations within stages](#correlations-within-stages)
        -   [Correlations across stages](#correlations-across-stages)
-   [Conclusions](#conclusions)

How should parasites divide their growth and development among the
multiple hosts of a complex life cycle? Here we look at parasite life
history strategies in two-host life cycles.

I rearranged the stage-level parasite data so that pairs represent
values in the current host and then the next host.

For simplicity let’s restrict ourselves to two stages: first
intermediate host and second definitive host. In other words, we’re only
looking at worms with two-host life cycles.

# Optimal life history strategies?

## Non-taxonomic models

When do worms spend more time in one host and less in another? We fit a
series of multivariate mixed models to explore parasite life history
strategies. Our response variables are parasite life history traits like
growth and development as well as their covariance (hence the
multivariate approach). We’ll first fit models without considering
parasite ancestry/taxonomy so that we can explore the correlations
between host traits and parasite life history. Life history models
suggest parasite growth should increase in hosts in which the growth
rate to mortality ratio is high, like big endothermic hosts. Moreover,
if the next host is large and endothermic, then growth should be
suppressed in the current host so as to avoid inducing mortality and
thus reducing the likelihood of transmission.

We took six parasite traits as response variables: growth in the
intermediate host, developmental time in the intermediate host, growth
in the definitive host, developmental time in the definitive host, and
size and age at maturity. We fit the following series of models: 1)
intercept-only, no covariance between traits, 2) allow covariance
between traits, 3) add fixed, main effects characterizing the parasite’s
hosts (intermediate host size, definitive host size, and endothermy of
definitive host), 4) interactions between fixed effects, and 5)
interactions between host traits and parasite group (acanths, nematodes,
cestodes). Regarding the fixed effects, we have a couple predictions
from theory, some of which have been shown previously: a) parasite size
and developmental time increase with host size, b) larval growth and
development decrease when the next host is relatively “good” (i.e. big
and endothermic).

Here are the number of species and families overall:

<div class="kable-table">

| n\_spp | n\_fams |
|-------:|--------:|
|    597 |      86 |

</div>

Let’s make sure all traits have been imputed:

<div class="kable-table">

| rg\_int | rg\_def | dd\_int | dd\_def | fs\_def | ag\_def |
|--------:|--------:|--------:|--------:|--------:|--------:|
|     597 |     597 |     597 |     597 |     597 |     597 |

</div>

Here are the number of species for each trait when data is not imputed:

<div class="kable-table">

| rg\_int | rg\_def | dd\_int | dd\_def | fs\_def | ag\_def |
|--------:|--------:|--------:|--------:|--------:|--------:|
|     364 |     379 |     277 |     167 |     494 |     105 |

</div>

And as proportions:

<div class="kable-table">

|   rg\_int |   rg\_def |   dd\_int |  dd\_def |   fs\_def |   ag\_def |
|----------:|----------:|----------:|---------:|----------:|----------:|
| 0.3902848 | 0.3651591 | 0.5360134 | 0.720268 | 0.1725293 | 0.8241206 |

</div>

The independent variables were host traits. Here is the average IH mass
in mg:

    ## [1] 21.87069

And DH mass in g:

    ## [1] 559.7284

There were more helminths with endotherm DHs than ectotherms in the
data.

<div class="kable-table">

| endo\_def |   n |      prop |
|----------:|----:|----------:|
|         0 | 204 | 0.3417085 |
|         1 | 393 | 0.6582915 |

</div>

    ## [1] "non-taxonomic models, imputation 1 finished"
    ## [1] "non-taxonomic models, imputation 2 finished"
    ## [1] "non-taxonomic models, imputation 3 finished"
    ## [1] "non-taxonomic models, imputation 4 finished"
    ## [1] "non-taxonomic models, imputation 5 finished"
    ## [1] "non-taxonomic models, imputation 6 finished"
    ## [1] "non-taxonomic models, imputation 7 finished"
    ## [1] "non-taxonomic models, imputation 8 finished"
    ## [1] "non-taxonomic models, imputation 9 finished"
    ## [1] "non-taxonomic models, imputation 10 finished"
    ## [1] "non-taxonomic models, imputation 11 finished"
    ## [1] "non-taxonomic models, imputation 12 finished"
    ## [1] "non-taxonomic models, imputation 13 finished"
    ## [1] "non-taxonomic models, imputation 14 finished"
    ## [1] "non-taxonomic models, imputation 15 finished"
    ## [1] "non-taxonomic models, imputation 16 finished"
    ## [1] "non-taxonomic models, imputation 17 finished"
    ## [1] "non-taxonomic models, imputation 18 finished"
    ## [1] "non-taxonomic models, imputation 19 finished"
    ## [1] "non-taxonomic models, imputation 20 finished"
    ## [1] "non-taxonomic models, imputation 21 finished"
    ## [1] "non-taxonomic models, imputation 22 finished"
    ## [1] "non-taxonomic models, imputation 23 finished"
    ## [1] "non-taxonomic models, imputation 24 finished"
    ## [1] "non-taxonomic models, imputation 25 finished"
    ## [1] "non-taxonomic models, imputation 26 finished"
    ## [1] "non-taxonomic models, imputation 27 finished"
    ## [1] "non-taxonomic models, imputation 28 finished"
    ## [1] "non-taxonomic models, imputation 29 finished"
    ## [1] "non-taxonomic models, imputation 30 finished"
    ## [1] "non-taxonomic models, imputation 31 finished"
    ## [1] "non-taxonomic models, imputation 32 finished"
    ## [1] "non-taxonomic models, imputation 33 finished"
    ## [1] "non-taxonomic models, imputation 34 finished"
    ## [1] "non-taxonomic models, imputation 35 finished"
    ## [1] "non-taxonomic models, imputation 36 finished"
    ## [1] "non-taxonomic models, imputation 37 finished"
    ## [1] "non-taxonomic models, imputation 38 finished"
    ## [1] "non-taxonomic models, imputation 39 finished"
    ## [1] "non-taxonomic models, imputation 40 finished"
    ## [1] "non-taxonomic models, imputation 41 finished"
    ## [1] "non-taxonomic models, imputation 42 finished"
    ## [1] "non-taxonomic models, imputation 43 finished"
    ## [1] "non-taxonomic models, imputation 44 finished"
    ## [1] "non-taxonomic models, imputation 45 finished"
    ## [1] "non-taxonomic models, imputation 46 finished"
    ## [1] "non-taxonomic models, imputation 47 finished"
    ## [1] "non-taxonomic models, imputation 48 finished"
    ## [1] "non-taxonomic models, imputation 49 finished"
    ## [1] "non-taxonomic models, imputation 50 finished"
    ## [1] "non-taxonomic models, imputation 51 finished"
    ## [1] "non-taxonomic models, imputation 52 finished"
    ## [1] "non-taxonomic models, imputation 53 finished"
    ## [1] "non-taxonomic models, imputation 54 finished"
    ## [1] "non-taxonomic models, imputation 55 finished"
    ## [1] "non-taxonomic models, imputation 56 finished"
    ## [1] "non-taxonomic models, imputation 57 finished"
    ## [1] "non-taxonomic models, imputation 58 finished"
    ## [1] "non-taxonomic models, imputation 59 finished"
    ## [1] "non-taxonomic models, imputation 60 finished"
    ## [1] "non-taxonomic models, imputation 61 finished"
    ## [1] "non-taxonomic models, imputation 62 finished"
    ## [1] "non-taxonomic models, imputation 63 finished"
    ## [1] "non-taxonomic models, imputation 64 finished"
    ## [1] "non-taxonomic models, imputation 65 finished"
    ## [1] "non-taxonomic models, imputation 66 finished"
    ## [1] "non-taxonomic models, imputation 67 finished"
    ## [1] "non-taxonomic models, imputation 68 finished"
    ## [1] "non-taxonomic models, imputation 69 finished"
    ## [1] "non-taxonomic models, imputation 70 finished"
    ## [1] "non-taxonomic models, imputation 71 finished"
    ## [1] "non-taxonomic models, imputation 72 finished"
    ## [1] "non-taxonomic models, imputation 73 finished"
    ## [1] "non-taxonomic models, imputation 74 finished"
    ## [1] "non-taxonomic models, imputation 75 finished"
    ## [1] "non-taxonomic models, imputation 76 finished"
    ## [1] "non-taxonomic models, imputation 77 finished"
    ## [1] "non-taxonomic models, imputation 78 finished"
    ## [1] "non-taxonomic models, imputation 79 finished"
    ## [1] "non-taxonomic models, imputation 80 finished"
    ## [1] "non-taxonomic models, imputation 81 finished"
    ## [1] "non-taxonomic models, imputation 82 finished"
    ## [1] "non-taxonomic models, imputation 83 finished"
    ## [1] "non-taxonomic models, imputation 84 finished"
    ## [1] "non-taxonomic models, imputation 85 finished"
    ## [1] "non-taxonomic models, imputation 86 finished"
    ## [1] "non-taxonomic models, imputation 87 finished"
    ## [1] "non-taxonomic models, imputation 88 finished"
    ## [1] "non-taxonomic models, imputation 89 finished"
    ## [1] "non-taxonomic models, imputation 90 finished"
    ## [1] "non-taxonomic models, imputation 91 finished"
    ## [1] "non-taxonomic models, imputation 92 finished"
    ## [1] "non-taxonomic models, imputation 93 finished"
    ## [1] "non-taxonomic models, imputation 94 finished"
    ## [1] "non-taxonomic models, imputation 95 finished"
    ## [1] "non-taxonomic models, imputation 96 finished"
    ## [1] "non-taxonomic models, imputation 97 finished"
    ## [1] "non-taxonomic models, imputation 98 finished"
    ## [1] "non-taxonomic models, imputation 99 finished"
    ## [1] "non-taxonomic models, imputation 100 finished"

Here is the model deviance for the non-taxonomic models. Allowing
covariance among life history traits (red) improves model fit, and we
explore these more below. Also, adding the fixed main effects (green)
and interactions (blue) improves model fit, as does adding phylum
interactions (light blue).

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-14-1.png)<!-- -->
Now we combine the chains for the fixed parameters and variance
componenets.

There are a lot of parameters - the model has six response variables and
15 fixed effects. Let’s start by looking at larval growth. As expected,
growth increased with intermediate host mass. Also, worms grow less when
the next host is an endotherm, though this varies with worm phylum.

<div class="kable-table">

|                                                                | param                                       |        lwr |        fit |        upr | sig |
|:---------------------------------------------------------------|:--------------------------------------------|-----------:|-----------:|-----------:|:----|
| traitrg\_int\_host:def\_host\_mass\_c                          | def\_host\_mass\_c                          | -0.2857392 |  0.0611311 |  0.4278314 | ns  |
| traitrg\_int\_host:def\_host\_mass\_c:endo\_def\_c             | def\_host\_mass\_c:endo\_def\_c             | -0.3233873 | -0.0952567 |  0.1375343 | ns  |
| traitrg\_int\_host:def\_host\_mass\_c:parasite\_phylumCestoda  | def\_host\_mass\_c:parasite\_phylumCestoda  | -0.2773154 |  0.1476809 |  0.5507547 | ns  |
| traitrg\_int\_host:def\_host\_mass\_c:parasite\_phylumNematoda | def\_host\_mass\_c:parasite\_phylumNematoda | -0.6764397 | -0.2522709 |  0.1255430 | ns  |
| traitrg\_int\_host:endo\_def\_c                                | endo\_def\_c                                | -4.1672109 | -2.5010646 | -0.7653450 | sig |
| traitrg\_int\_host:endo\_def\_c:parasite\_phylumCestoda        | endo\_def\_c:parasite\_phylumCestoda        | -1.5985717 |  0.2227194 |  2.0990624 | ns  |
| traitrg\_int\_host:endo\_def\_c:parasite\_phylumNematoda       | endo\_def\_c:parasite\_phylumNematoda       | -1.6963534 |  0.2534113 |  2.0831428 | ns  |
| traitrg\_int\_host:int\_host\_mass\_c                          | int\_host\_mass\_c                          |  0.1933968 |  0.4551546 |  0.7316208 | sig |
| traitrg\_int\_host:int\_host\_mass\_c:def\_host\_mass\_c       | int\_host\_mass\_c:def\_host\_mass\_c       | -0.0083496 |  0.0138034 |  0.0345514 | ns  |
| traitrg\_int\_host:int\_host\_mass\_c:endo\_def\_c             | int\_host\_mass\_c:endo\_def\_c             | -0.4050408 | -0.2620794 | -0.1152597 | sig |
| traitrg\_int\_host:int\_host\_mass\_c:parasite\_phylumCestoda  | int\_host\_mass\_c:parasite\_phylumCestoda  | -0.1438258 |  0.1322346 |  0.4335681 | ns  |
| traitrg\_int\_host:int\_host\_mass\_c:parasite\_phylumNematoda | int\_host\_mass\_c:parasite\_phylumNematoda | -0.4389366 | -0.1550333 |  0.1173969 | ns  |
| traitrg\_int\_host:parasite\_phylumCestoda                     | parasite\_phylumCestoda                     | -3.4783421 | -2.6599635 | -1.8229613 | sig |
| traitrg\_int\_host:parasite\_phylumNematoda                    | parasite\_phylumNematoda                    | -6.3327874 | -5.5311658 | -4.6621098 | sig |
| traitrg\_int\_host                                             | traitrg\_int\_host                          |  9.1692437 |  9.9526339 | 10.6698262 | sig |

</div>

Now we move on to traits in the definitive host. Just looking at growth
(more data), it does not increase with definitive host mass,
surprisingly. It seems influenced by endothermy at least in some groups.
It also tends to decrease with intermediate host mass, suggesting growth
in a large intermediate hosts results in less growth in the definitive
host.

<div class="kable-table">

|                                                                | param                                       |        lwr |        fit |        upr | sig |
|:---------------------------------------------------------------|:--------------------------------------------|-----------:|-----------:|-----------:|:----|
| traitrg\_def\_host:def\_host\_mass\_c                          | def\_host\_mass\_c                          | -0.4362702 | -0.0088553 |  0.4005152 | ns  |
| traitrg\_def\_host:def\_host\_mass\_c:endo\_def\_c             | def\_host\_mass\_c:endo\_def\_c             | -0.2109078 |  0.0134460 |  0.2430767 | ns  |
| traitrg\_def\_host:def\_host\_mass\_c:parasite\_phylumCestoda  | def\_host\_mass\_c:parasite\_phylumCestoda  | -0.2711396 |  0.1778124 |  0.6382868 | ns  |
| traitrg\_def\_host:def\_host\_mass\_c:parasite\_phylumNematoda | def\_host\_mass\_c:parasite\_phylumNematoda | -0.2733188 |  0.1778907 |  0.6305893 | ns  |
| traitrg\_def\_host:endo\_def\_c                                | endo\_def\_c                                |  1.2891116 |  3.2015190 |  5.0997929 | sig |
| traitrg\_def\_host:endo\_def\_c:parasite\_phylumCestoda        | endo\_def\_c:parasite\_phylumCestoda        | -1.7466235 |  0.2863248 |  2.2849220 | ns  |
| traitrg\_def\_host:endo\_def\_c:parasite\_phylumNematoda       | endo\_def\_c:parasite\_phylumNematoda       | -3.1080429 | -1.0378787 |  0.9530640 | ns  |
| traitrg\_def\_host:int\_host\_mass\_c                          | int\_host\_mass\_c                          | -0.6895818 | -0.3968559 | -0.0835850 | sig |
| traitrg\_def\_host:int\_host\_mass\_c:def\_host\_mass\_c       | int\_host\_mass\_c:def\_host\_mass\_c       | -0.0286694 | -0.0044063 |  0.0185232 | ns  |
| traitrg\_def\_host:int\_host\_mass\_c:endo\_def\_c             | int\_host\_mass\_c:endo\_def\_c             |  0.2552640 |  0.3959712 |  0.5292143 | sig |
| traitrg\_def\_host:int\_host\_mass\_c:parasite\_phylumCestoda  | int\_host\_mass\_c:parasite\_phylumCestoda  | -0.4980004 | -0.1878203 |  0.1251463 | ns  |
| traitrg\_def\_host:int\_host\_mass\_c:parasite\_phylumNematoda | int\_host\_mass\_c:parasite\_phylumNematoda | -0.0816185 |  0.2282419 |  0.5315410 | ns  |
| traitrg\_def\_host:parasite\_phylumCestoda                     | parasite\_phylumCestoda                     |  2.2193803 |  3.0723067 |  3.9487611 | sig |
| traitrg\_def\_host:parasite\_phylumNematoda                    | parasite\_phylumNematoda                    |  1.7912855 |  2.6681879 |  3.5453450 | sig |
| traitrg\_def\_host                                             | traitrg\_def\_host                          |  2.8438527 |  3.6201427 |  4.4170096 | sig |

</div>

Instead of relative growth in the definitive host, we can look at the
overall size achieved. It also did not increase with definitive host
mass, though it tended to be larger in endotherms.

<div class="kable-table">

|                                                                | param                                       |        lwr |        fit |        upr | sig |
|:---------------------------------------------------------------|:--------------------------------------------|-----------:|-----------:|-----------:|:----|
| traitfs\_def\_host:def\_host\_mass\_c                          | def\_host\_mass\_c                          | -0.2113204 |  0.1400801 |  0.4899495 | ns  |
| traitfs\_def\_host:def\_host\_mass\_c:endo\_def\_c             | def\_host\_mass\_c:endo\_def\_c             | -0.2528737 | -0.0522880 |  0.1462771 | ns  |
| traitfs\_def\_host:def\_host\_mass\_c:parasite\_phylumCestoda  | def\_host\_mass\_c:parasite\_phylumCestoda  | -0.1339068 |  0.2384089 |  0.6238667 | ns  |
| traitfs\_def\_host:def\_host\_mass\_c:parasite\_phylumNematoda | def\_host\_mass\_c:parasite\_phylumNematoda | -0.4603509 | -0.0782594 |  0.3014506 | ns  |
| traitfs\_def\_host:endo\_def\_c                                | endo\_def\_c                                | -0.0068037 |  1.6371852 |  3.2498468 | ns  |
| traitfs\_def\_host:endo\_def\_c:parasite\_phylumCestoda        | endo\_def\_c:parasite\_phylumCestoda        | -2.0769686 | -0.2668791 |  1.6309157 | ns  |
| traitfs\_def\_host:endo\_def\_c:parasite\_phylumNematoda       | endo\_def\_c:parasite\_phylumNematoda       | -3.5271748 | -1.8691881 | -0.0717559 | sig |
| traitfs\_def\_host:int\_host\_mass\_c                          | int\_host\_mass\_c                          | -0.1577593 |  0.0875283 |  0.3435473 | ns  |
| traitfs\_def\_host:int\_host\_mass\_c:def\_host\_mass\_c       | int\_host\_mass\_c:def\_host\_mass\_c       | -0.0144728 |  0.0047396 |  0.0249045 | ns  |
| traitfs\_def\_host:int\_host\_mass\_c:endo\_def\_c             | int\_host\_mass\_c:endo\_def\_c             |  0.0553754 |  0.1716100 |  0.2850696 | sig |
| traitfs\_def\_host:int\_host\_mass\_c:parasite\_phylumCestoda  | int\_host\_mass\_c:parasite\_phylumCestoda  | -0.3912953 | -0.1254357 |  0.1396779 | ns  |
| traitfs\_def\_host:int\_host\_mass\_c:parasite\_phylumNematoda | int\_host\_mass\_c:parasite\_phylumNematoda | -0.2321343 |  0.0375254 |  0.3015769 | ns  |
| traitfs\_def\_host:parasite\_phylumCestoda                     | parasite\_phylumCestoda                     |  0.4091010 |  1.1645940 |  1.9063083 | sig |
| traitfs\_def\_host:parasite\_phylumNematoda                    | parasite\_phylumNematoda                    | -2.8320639 | -2.0961600 | -1.3444170 | sig |
| traitfs\_def\_host                                             | traitfs\_def\_host                          |  2.0563040 |  2.7535596 |  3.4185407 | sig |

</div>

Let’s plot the effects of the larval environment on worm life history
and then the effects of the adult environment. Blue vs red points
distinguish worms with ecto vs endotherm definitive hosts. Larval growth
increases and adult growth decreases with intermediate host size. Final
worm size is unaffected by intermediate host size.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-19-1.png)<!-- -->

Now, we plot how adult environment affects worm life history.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-20-1.png)<!-- -->

So habitats that favor larval growth (big intermediate hosts) are
associated with less adult growth. We can see this by plotting relative
growth in the two hosts. They are negatively correlated.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-21-1.png)<!-- -->
But are these still negatively correlated after we account for the model
fixed effects, like host mass and endothermy? We check this correlation
via the model residuals.

Here is the same plot as above. There is still a clear negative
correlation between relative growth in the two hosts (notice how the
endothermy effect was removed by using residuals).

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-24-1.png)<!-- -->
More generally, the correlations among response variables did not change
much after accounting for model fixed effects.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-25-1.png)<!-- -->

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-26-1.png)<!-- -->

We also average the residuals for size and age to assess over and
under-performance. For example, here is the correlation between
developmental time and relative growth in the intermediate host. Points
are colored by their average residuals (i.e. whether they overperform or
underperform).

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-27-1.png)<!-- -->
We can calculate over and underperformance for three developmental
periods: in the intermediate host, in the definitive host, and over the
whole life. When we plot these against each other, we see that larval
and adult growth are unrelated, larval growth slightly increases
lifetime growth, and adult growth clearly increases lifetime growth.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-28-1.png)<!-- -->
The absence of a negative relationship between larval and adult
performance is surprising, since higher larval growth resulted in less
adult growth. However, less adult growth was also associated with
shorter developmental times. Thus, in species with overachieving larvae,
the adults grow less but also have short development, suggesting they do
not underachieve as adults.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-29-1.png)<!-- -->

## Taxonomic mixed models

Since both parasite life history and host traits are phylogenetically
structured, it is possible that some of these effects disappear when we
control for parasite ancestry. We next fit the same series of models,
but including parasite taxonomy as nested random effects. The residuals
can covary, since our response variables are clearly correlated.

    ## [1] "taxonomic models, imputation 1 finished"
    ## [1] "taxonomic models, imputation 2 finished"
    ## [1] "taxonomic models, imputation 3 finished"
    ## [1] "taxonomic models, imputation 4 finished"
    ## [1] "taxonomic models, imputation 5 finished"
    ## [1] "taxonomic models, imputation 6 finished"
    ## [1] "taxonomic models, imputation 7 finished"
    ## [1] "taxonomic models, imputation 8 finished"
    ## [1] "taxonomic models, imputation 9 finished"
    ## [1] "taxonomic models, imputation 10 finished"
    ## [1] "taxonomic models, imputation 11 finished"
    ## [1] "taxonomic models, imputation 12 finished"
    ## [1] "taxonomic models, imputation 13 finished"
    ## [1] "taxonomic models, imputation 14 finished"
    ## [1] "taxonomic models, imputation 15 finished"
    ## [1] "taxonomic models, imputation 16 finished"
    ## [1] "taxonomic models, imputation 17 finished"
    ## [1] "taxonomic models, imputation 18 finished"
    ## [1] "taxonomic models, imputation 19 finished"
    ## [1] "taxonomic models, imputation 20 finished"
    ## [1] "taxonomic models, imputation 21 finished"
    ## [1] "taxonomic models, imputation 22 finished"
    ## [1] "taxonomic models, imputation 23 finished"
    ## [1] "taxonomic models, imputation 24 finished"
    ## [1] "taxonomic models, imputation 25 finished"
    ## [1] "taxonomic models, imputation 26 finished"
    ## [1] "taxonomic models, imputation 27 finished"
    ## [1] "taxonomic models, imputation 28 finished"
    ## [1] "taxonomic models, imputation 29 finished"
    ## [1] "taxonomic models, imputation 30 finished"
    ## [1] "taxonomic models, imputation 31 finished"
    ## [1] "taxonomic models, imputation 32 finished"
    ## [1] "taxonomic models, imputation 33 finished"
    ## [1] "taxonomic models, imputation 34 finished"
    ## [1] "taxonomic models, imputation 35 finished"
    ## [1] "taxonomic models, imputation 36 finished"
    ## [1] "taxonomic models, imputation 37 finished"
    ## [1] "taxonomic models, imputation 38 finished"
    ## [1] "taxonomic models, imputation 39 finished"
    ## [1] "taxonomic models, imputation 40 finished"
    ## [1] "taxonomic models, imputation 41 finished"
    ## [1] "taxonomic models, imputation 42 finished"
    ## [1] "taxonomic models, imputation 43 finished"
    ## [1] "taxonomic models, imputation 44 finished"
    ## [1] "taxonomic models, imputation 45 finished"
    ## [1] "taxonomic models, imputation 46 finished"
    ## [1] "taxonomic models, imputation 47 finished"
    ## [1] "taxonomic models, imputation 48 finished"
    ## [1] "taxonomic models, imputation 49 finished"
    ## [1] "taxonomic models, imputation 50 finished"
    ## [1] "taxonomic models, imputation 51 finished"
    ## [1] "taxonomic models, imputation 52 finished"
    ## [1] "taxonomic models, imputation 53 finished"
    ## [1] "taxonomic models, imputation 54 finished"
    ## [1] "taxonomic models, imputation 55 finished"
    ## [1] "taxonomic models, imputation 56 finished"
    ## [1] "taxonomic models, imputation 57 finished"
    ## [1] "taxonomic models, imputation 58 finished"
    ## [1] "taxonomic models, imputation 59 finished"
    ## [1] "taxonomic models, imputation 60 finished"
    ## [1] "taxonomic models, imputation 61 finished"
    ## [1] "taxonomic models, imputation 62 finished"
    ## [1] "taxonomic models, imputation 63 finished"
    ## [1] "taxonomic models, imputation 64 finished"
    ## [1] "taxonomic models, imputation 65 finished"
    ## [1] "taxonomic models, imputation 66 finished"
    ## [1] "taxonomic models, imputation 67 finished"
    ## [1] "taxonomic models, imputation 68 finished"
    ## [1] "taxonomic models, imputation 69 finished"
    ## [1] "taxonomic models, imputation 70 finished"
    ## [1] "taxonomic models, imputation 71 finished"
    ## [1] "taxonomic models, imputation 72 finished"
    ## [1] "taxonomic models, imputation 73 finished"
    ## [1] "taxonomic models, imputation 74 finished"
    ## [1] "taxonomic models, imputation 75 finished"
    ## [1] "taxonomic models, imputation 76 finished"
    ## [1] "taxonomic models, imputation 77 finished"
    ## [1] "taxonomic models, imputation 78 finished"
    ## [1] "taxonomic models, imputation 79 finished"
    ## [1] "taxonomic models, imputation 80 finished"
    ## [1] "taxonomic models, imputation 81 finished"
    ## [1] "taxonomic models, imputation 82 finished"
    ## [1] "taxonomic models, imputation 83 finished"
    ## [1] "taxonomic models, imputation 84 finished"
    ## [1] "taxonomic models, imputation 85 finished"
    ## [1] "taxonomic models, imputation 86 finished"
    ## [1] "taxonomic models, imputation 87 finished"
    ## [1] "taxonomic models, imputation 88 finished"
    ## [1] "taxonomic models, imputation 89 finished"
    ## [1] "taxonomic models, imputation 90 finished"
    ## [1] "taxonomic models, imputation 91 finished"
    ## [1] "taxonomic models, imputation 92 finished"
    ## [1] "taxonomic models, imputation 93 finished"
    ## [1] "taxonomic models, imputation 94 finished"
    ## [1] "taxonomic models, imputation 95 finished"
    ## [1] "taxonomic models, imputation 96 finished"
    ## [1] "taxonomic models, imputation 97 finished"
    ## [1] "taxonomic models, imputation 98 finished"
    ## [1] "taxonomic models, imputation 99 finished"
    ## [1] "taxonomic models, imputation 100 finished"

    ## [1] "total growth models, imputation 1 finished"
    ## [1] "total growth models, imputation 2 finished"
    ## [1] "total growth models, imputation 3 finished"
    ## [1] "total growth models, imputation 4 finished"
    ## [1] "total growth models, imputation 5 finished"
    ## [1] "total growth models, imputation 6 finished"
    ## [1] "total growth models, imputation 7 finished"
    ## [1] "total growth models, imputation 8 finished"
    ## [1] "total growth models, imputation 9 finished"
    ## [1] "total growth models, imputation 10 finished"
    ## [1] "total growth models, imputation 11 finished"
    ## [1] "total growth models, imputation 12 finished"
    ## [1] "total growth models, imputation 13 finished"
    ## [1] "total growth models, imputation 14 finished"
    ## [1] "total growth models, imputation 15 finished"
    ## [1] "total growth models, imputation 16 finished"
    ## [1] "total growth models, imputation 17 finished"
    ## [1] "total growth models, imputation 18 finished"
    ## [1] "total growth models, imputation 19 finished"
    ## [1] "total growth models, imputation 20 finished"
    ## [1] "total growth models, imputation 21 finished"
    ## [1] "total growth models, imputation 22 finished"
    ## [1] "total growth models, imputation 23 finished"
    ## [1] "total growth models, imputation 24 finished"
    ## [1] "total growth models, imputation 25 finished"
    ## [1] "total growth models, imputation 26 finished"
    ## [1] "total growth models, imputation 27 finished"
    ## [1] "total growth models, imputation 28 finished"
    ## [1] "total growth models, imputation 29 finished"
    ## [1] "total growth models, imputation 30 finished"
    ## [1] "total growth models, imputation 31 finished"
    ## [1] "total growth models, imputation 32 finished"
    ## [1] "total growth models, imputation 33 finished"
    ## [1] "total growth models, imputation 34 finished"
    ## [1] "total growth models, imputation 35 finished"
    ## [1] "total growth models, imputation 36 finished"
    ## [1] "total growth models, imputation 37 finished"
    ## [1] "total growth models, imputation 38 finished"
    ## [1] "total growth models, imputation 39 finished"
    ## [1] "total growth models, imputation 40 finished"
    ## [1] "total growth models, imputation 41 finished"
    ## [1] "total growth models, imputation 42 finished"
    ## [1] "total growth models, imputation 43 finished"
    ## [1] "total growth models, imputation 44 finished"
    ## [1] "total growth models, imputation 45 finished"
    ## [1] "total growth models, imputation 46 finished"
    ## [1] "total growth models, imputation 47 finished"
    ## [1] "total growth models, imputation 48 finished"
    ## [1] "total growth models, imputation 49 finished"
    ## [1] "total growth models, imputation 50 finished"
    ## [1] "total growth models, imputation 51 finished"
    ## [1] "total growth models, imputation 52 finished"
    ## [1] "total growth models, imputation 53 finished"
    ## [1] "total growth models, imputation 54 finished"
    ## [1] "total growth models, imputation 55 finished"
    ## [1] "total growth models, imputation 56 finished"
    ## [1] "total growth models, imputation 57 finished"
    ## [1] "total growth models, imputation 58 finished"
    ## [1] "total growth models, imputation 59 finished"
    ## [1] "total growth models, imputation 60 finished"
    ## [1] "total growth models, imputation 61 finished"
    ## [1] "total growth models, imputation 62 finished"
    ## [1] "total growth models, imputation 63 finished"
    ## [1] "total growth models, imputation 64 finished"
    ## [1] "total growth models, imputation 65 finished"
    ## [1] "total growth models, imputation 66 finished"
    ## [1] "total growth models, imputation 67 finished"
    ## [1] "total growth models, imputation 68 finished"
    ## [1] "total growth models, imputation 69 finished"
    ## [1] "total growth models, imputation 70 finished"
    ## [1] "total growth models, imputation 71 finished"
    ## [1] "total growth models, imputation 72 finished"
    ## [1] "total growth models, imputation 73 finished"
    ## [1] "total growth models, imputation 74 finished"
    ## [1] "total growth models, imputation 75 finished"
    ## [1] "total growth models, imputation 76 finished"
    ## [1] "total growth models, imputation 77 finished"
    ## [1] "total growth models, imputation 78 finished"
    ## [1] "total growth models, imputation 79 finished"
    ## [1] "total growth models, imputation 80 finished"
    ## [1] "total growth models, imputation 81 finished"
    ## [1] "total growth models, imputation 82 finished"
    ## [1] "total growth models, imputation 83 finished"
    ## [1] "total growth models, imputation 84 finished"
    ## [1] "total growth models, imputation 85 finished"
    ## [1] "total growth models, imputation 86 finished"
    ## [1] "total growth models, imputation 87 finished"
    ## [1] "total growth models, imputation 88 finished"
    ## [1] "total growth models, imputation 89 finished"
    ## [1] "total growth models, imputation 90 finished"
    ## [1] "total growth models, imputation 91 finished"
    ## [1] "total growth models, imputation 92 finished"
    ## [1] "total growth models, imputation 93 finished"
    ## [1] "total growth models, imputation 94 finished"
    ## [1] "total growth models, imputation 95 finished"
    ## [1] "total growth models, imputation 96 finished"
    ## [1] "total growth models, imputation 97 finished"
    ## [1] "total growth models, imputation 98 finished"
    ## [1] "total growth models, imputation 99 finished"
    ## [1] "total growth models, imputation 100 finished"

Adding taxonomy is clearly important. It improves the model without
fixed effects…

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-35-1.png)<!-- -->

…as well as the model with fixed effects.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-36-1.png)<!-- -->

This suggests that parasite traits are taxonomically structured, even
after controlling for host masses. We also compared models treating
phylogeny as nested taxonomic levels or as a phylogenetic tree. In the
models with the phylogeny, the variance components were very large,
which usually happens when closely related species are quite different
(i.e. big phenotypic change on short branches, which may be more
measurement error than evolution). Despite this, the phylogenetic models
were much worse than the taxonomic ones. This suggests that not all
parts of the tree are informative.

## Model parameters

### Larval growth

Since taxonomy clearly impacts parasite life history, we should
reexamine the fixed effects, starting with larval growth. Larval
parasites grow more when the intermediate host is large. The
relationship with endothermy seems to depend on intermediate host size.

<div class="kable-table">

|                                                                | param                                       |        lwr |        fit |        upr | sig |
|:---------------------------------------------------------------|:--------------------------------------------|-----------:|-----------:|-----------:|:----|
| traitrg\_int\_host:def\_host\_mass\_c                          | def\_host\_mass\_c                          | -0.3407552 | -0.1173825 |  0.1142824 | ns  |
| traitrg\_int\_host:def\_host\_mass\_c:endo\_def\_c             | def\_host\_mass\_c:endo\_def\_c             | -0.1891410 | -0.0389459 |  0.1092543 | ns  |
| traitrg\_int\_host:def\_host\_mass\_c:parasite\_phylumCestoda  | def\_host\_mass\_c:parasite\_phylumCestoda  | -0.0894379 |  0.1503524 |  0.4086980 | ns  |
| traitrg\_int\_host:def\_host\_mass\_c:parasite\_phylumNematoda | def\_host\_mass\_c:parasite\_phylumNematoda | -0.0398896 |  0.2186263 |  0.4595925 | ns  |
| traitrg\_int\_host:endo\_def\_c                                | endo\_def\_c                                | -5.5926720 | -1.4761380 |  2.8901216 | ns  |
| traitrg\_int\_host:endo\_def\_c:parasite\_phylumCestoda        | endo\_def\_c:parasite\_phylumCestoda        | -4.2913348 |  0.5361858 |  5.2975235 | ns  |
| traitrg\_int\_host:endo\_def\_c:parasite\_phylumNematoda       | endo\_def\_c:parasite\_phylumNematoda       | -4.1878020 |  0.2630217 |  4.7670470 | ns  |
| traitrg\_int\_host:int\_host\_mass\_c                          | int\_host\_mass\_c                          |  0.0950219 |  0.2967372 |  0.5023614 | sig |
| traitrg\_int\_host:int\_host\_mass\_c:def\_host\_mass\_c       | int\_host\_mass\_c:def\_host\_mass\_c       | -0.0232057 | -0.0100404 |  0.0044967 | ns  |
| traitrg\_int\_host:int\_host\_mass\_c:endo\_def\_c             | int\_host\_mass\_c:endo\_def\_c             | -0.3793882 | -0.2536534 | -0.1356943 | sig |
| traitrg\_int\_host:int\_host\_mass\_c:parasite\_phylumCestoda  | int\_host\_mass\_c:parasite\_phylumCestoda  | -0.1585893 |  0.0750265 |  0.2876381 | ns  |
| traitrg\_int\_host:int\_host\_mass\_c:parasite\_phylumNematoda | int\_host\_mass\_c:parasite\_phylumNematoda | -0.3404408 | -0.1153077 |  0.1088387 | ns  |
| traitrg\_int\_host:parasite\_phylumCestoda                     | parasite\_phylumCestoda                     | -3.8831169 | -1.2780194 |  1.4261971 | ns  |
| traitrg\_int\_host:parasite\_phylumNematoda                    | parasite\_phylumNematoda                    | -7.8991490 | -5.1538639 | -2.8085850 | sig |
| traitrg\_int\_host                                             | traitrg\_int\_host                          |  7.1903532 |  9.1470207 | 10.9471481 | sig |

</div>

Here is how much relative larval growth increased with a doubling of
intermediate host mass.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.1671581      0.0235798      0.0007457      0.0007522 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.1216 0.1518 0.1669 0.1819 0.2139

However, this relationship depended on whether the next host was an
endotherm or not. Here is how much larval growth increased with
intermediate host mass when the definitive host was an ectotherm:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.2038447      0.0282818      0.0008943      0.0009396 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.1482 0.1850 0.2042 0.2214 0.2582

And when it was an endotherm (though this was also dependent on the
parasite group):

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.1335628      0.0261855      0.0008281      0.0008281 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## 0.08125 0.11619 0.13366 0.15171 0.18479

Here is how much larval growth decreased when the next host was an
endotherm (avg int and def host masses).

<div class="kable-table">

| int\_host\_mass\_c | def\_host\_mass\_c | endo\_def | lwr\_rg\_int\_pred | fit\_rg\_int\_pred | upr\_rg\_int\_pred | fold\_change.lwr | fold\_change.fit | fold\_change.upr |
|-------------------:|-------------------:|----------:|-------------------:|-------------------:|-------------------:|-----------------:|-----------------:|-----------------:|
|          0.1914443 |                  0 |         0 |           5.500225 |           7.672900 |          10.039115 |        244.74708 |        2149.3053 |        22905.107 |
|          0.1297289 |                  0 |         1 |           4.005806 |           6.248772 |           8.677531 |         54.91608 |         517.3769 |         5869.539 |

</div>

Here is the average increase in size in an average intermediate host
(fold change).

<div class="kable-table">

|                    | param              | avg\_fold\_change\_IH\_lwr | avg\_fold\_change\_IH | avg\_fold\_change\_IH\_upr |
|:-------------------|:-------------------|---------------------------:|----------------------:|---------------------------:|
| traitrg\_int\_host | traitrg\_int\_host |                   103.1174 |              999.6011 |                   10393.63 |

</div>

We can also explore how the average growth values depend on the model.

The models are reasonably consistent.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-46-1.png)<!-- -->

### Larval development

The average time spent developing as larvae (days at 20 C):

<div class="kable-table">

|                    | param              | avg\_dd\_IH\_lwr | avg\_dd\_IH | avg\_dd\_IH\_upr |
|:-------------------|:-------------------|-----------------:|------------:|-----------------:|
| traitdd\_int\_host | traitdd\_int\_host |         14.40784 |    32.80428 |         78.47552 |

</div>

The models are reasonably consistent.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-48-1.png)<!-- -->

Larval developmental time increased significantly with intermediate host
mass, but only when the next host was an ectotherm.

<div class="kable-table">

|                                                          | param                                 |        lwr |        fit |        upr | sig |
|:---------------------------------------------------------|:--------------------------------------|-----------:|-----------:|-----------:|:----|
| traitdd\_int\_host:def\_host\_mass\_c                    | def\_host\_mass\_c                    | -0.0101610 |  0.0079518 |  0.0266706 | ns  |
| traitdd\_int\_host:def\_host\_mass\_c:endo\_def\_c       | def\_host\_mass\_c:endo\_def\_c       | -0.0673513 | -0.0308553 |  0.0078443 | ns  |
| traitdd\_int\_host:endo\_def\_c                          | endo\_def\_c                          | -0.0207273 |  0.2081118 |  0.4136359 | ns  |
| traitdd\_int\_host:int\_host\_mass\_c                    | int\_host\_mass\_c                    |  0.0373604 |  0.0530400 |  0.0690574 | sig |
| traitdd\_int\_host:int\_host\_mass\_c:def\_host\_mass\_c | int\_host\_mass\_c:def\_host\_mass\_c | -0.0033870 | -0.0000051 |  0.0033300 | ns  |
| traitdd\_int\_host:int\_host\_mass\_c:endo\_def\_c       | int\_host\_mass\_c:endo\_def\_c       | -0.0906270 | -0.0606485 | -0.0317821 | sig |
| traitdd\_int\_host                                       | traitdd\_int\_host                    |  5.3758227 |  6.1986092 |  7.0708370 | sig |

</div>

Here is the percent increase in larval DT with a doubling of
intermediate host mass.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.0284955      0.0052584      0.0001663      0.0001663 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## 0.01842 0.02491 0.02839 0.03201 0.03873

However, this relationship depended on whether the next host was an
endotherm or not. Here is how much larval development increased with
intermediate host mass when the definitive host was an ectotherm:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.0374247      0.0058874      0.0001862      0.0001862 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## 0.02623 0.03333 0.03745 0.04150 0.04903

And when it was an endotherm; a doubling of intermediate host mass has
half the effect on larval developmental time.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.0158962      0.0059513      0.0001882      0.0001882 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##     2.5%      25%      50%      75%    97.5% 
    ## 0.004424 0.011953 0.015804 0.020004 0.027780

Nematodes had shorter developmental times as larvae.

<div class="kable-table">

|                                                                | param                                       |        lwr |        fit |        upr | sig |
|:---------------------------------------------------------------|:--------------------------------------------|-----------:|-----------:|-----------:|:----|
| traitdd\_int\_host:def\_host\_mass\_c                          | def\_host\_mass\_c                          | -0.0594087 |  0.0002506 |  0.0587176 | ns  |
| traitdd\_int\_host:def\_host\_mass\_c:endo\_def\_c             | def\_host\_mass\_c:endo\_def\_c             | -0.0705357 | -0.0312191 |  0.0072180 | ns  |
| traitdd\_int\_host:def\_host\_mass\_c:parasite\_phylumCestoda  | def\_host\_mass\_c:parasite\_phylumCestoda  | -0.0620894 |  0.0054269 |  0.0745141 | ns  |
| traitdd\_int\_host:def\_host\_mass\_c:parasite\_phylumNematoda | def\_host\_mass\_c:parasite\_phylumNematoda | -0.0504057 |  0.0146546 |  0.0821176 | ns  |
| traitdd\_int\_host:endo\_def\_c                                | endo\_def\_c                                | -0.9348289 |  0.0787145 |  1.1724558 | ns  |
| traitdd\_int\_host:endo\_def\_c:parasite\_phylumCestoda        | endo\_def\_c:parasite\_phylumCestoda        | -1.3732184 | -0.0951995 |  1.0610171 | ns  |
| traitdd\_int\_host:endo\_def\_c:parasite\_phylumNematoda       | endo\_def\_c:parasite\_phylumNematoda       | -0.8862698 |  0.1965870 |  1.2106608 | ns  |
| traitdd\_int\_host:int\_host\_mass\_c                          | int\_host\_mass\_c                          |  0.0088375 |  0.0653387 |  0.1284659 | sig |
| traitdd\_int\_host:int\_host\_mass\_c:def\_host\_mass\_c       | int\_host\_mass\_c:def\_host\_mass\_c       | -0.0036190 |  0.0001082 |  0.0036740 | ns  |
| traitdd\_int\_host:int\_host\_mass\_c:endo\_def\_c             | int\_host\_mass\_c:endo\_def\_c             | -0.0949340 | -0.0644692 | -0.0284359 | sig |
| traitdd\_int\_host:int\_host\_mass\_c:parasite\_phylumCestoda  | int\_host\_mass\_c:parasite\_phylumCestoda  | -0.0778476 | -0.0138071 |  0.0493823 | ns  |
| traitdd\_int\_host:int\_host\_mass\_c:parasite\_phylumNematoda | int\_host\_mass\_c:parasite\_phylumNematoda | -0.0786459 | -0.0126384 |  0.0520761 | ns  |
| traitdd\_int\_host:parasite\_phylumCestoda                     | parasite\_phylumCestoda                     | -1.6034942 | -0.5060883 |  0.5211146 | ns  |
| traitdd\_int\_host:parasite\_phylumNematoda                    | parasite\_phylumNematoda                    | -2.0066930 | -1.0449298 |  0.0442139 | ns  |
| traitdd\_int\_host                                             | traitdd\_int\_host                          |  5.9672366 |  6.6937628 |  7.4365327 | sig |

</div>

### Adult growth

For adult growth, there is an effect of endothermy and a negative
relationship with intermediate host size.

<div class="kable-table">

|                                                                | param                                       |        lwr |        fit |        upr | sig |
|:---------------------------------------------------------------|:--------------------------------------------|-----------:|-----------:|-----------:|:----|
| traitrg\_def\_host:def\_host\_mass\_c                          | def\_host\_mass\_c                          | -0.1839369 |  0.1516491 |  0.4365778 | ns  |
| traitrg\_def\_host:def\_host\_mass\_c:endo\_def\_c             | def\_host\_mass\_c:endo\_def\_c             | -0.1057171 |  0.0794086 |  0.2873681 | ns  |
| traitrg\_def\_host:def\_host\_mass\_c:parasite\_phylumCestoda  | def\_host\_mass\_c:parasite\_phylumCestoda  | -0.3409417 | -0.0050313 |  0.3343055 | ns  |
| traitrg\_def\_host:def\_host\_mass\_c:parasite\_phylumNematoda | def\_host\_mass\_c:parasite\_phylumNematoda | -0.3043094 |  0.0011543 |  0.3524349 | ns  |
| traitrg\_def\_host:endo\_def\_c                                | endo\_def\_c                                |  1.0186687 |  4.0194804 |  7.0393427 | sig |
| traitrg\_def\_host:endo\_def\_c:parasite\_phylumCestoda        | endo\_def\_c:parasite\_phylumCestoda        | -5.6112612 | -1.9410499 |  1.5291531 | ns  |
| traitrg\_def\_host:endo\_def\_c:parasite\_phylumNematoda       | endo\_def\_c:parasite\_phylumNematoda       | -4.9904317 | -1.6827245 |  1.3992422 | ns  |
| traitrg\_def\_host:int\_host\_mass\_c                          | int\_host\_mass\_c                          | -0.6619530 | -0.4037812 | -0.1434231 | sig |
| traitrg\_def\_host:int\_host\_mass\_c:def\_host\_mass\_c       | int\_host\_mass\_c:def\_host\_mass\_c       | -0.0117594 |  0.0065823 |  0.0259646 | ns  |
| traitrg\_def\_host:int\_host\_mass\_c:endo\_def\_c             | int\_host\_mass\_c:endo\_def\_c             |  0.1224826 |  0.2657056 |  0.4120714 | sig |
| traitrg\_def\_host:int\_host\_mass\_c:parasite\_phylumCestoda  | int\_host\_mass\_c:parasite\_phylumCestoda  | -0.2472618 |  0.0406355 |  0.3329601 | ns  |
| traitrg\_def\_host:int\_host\_mass\_c:parasite\_phylumNematoda | int\_host\_mass\_c:parasite\_phylumNematoda | -0.0936434 |  0.1910364 |  0.4730763 | ns  |
| traitrg\_def\_host:parasite\_phylumCestoda                     | parasite\_phylumCestoda                     | -0.3644731 |  2.0999480 |  4.2438690 | ns  |
| traitrg\_def\_host:parasite\_phylumNematoda                    | parasite\_phylumNematoda                    |  0.3940033 |  2.5151724 |  4.6654566 | sig |
| traitrg\_def\_host                                             | traitrg\_def\_host                          |  2.6277473 |  4.2661782 |  5.9787111 | sig |

</div>

There was not a clear relationship with definitive host mass, but that
is because the relationship varies somewhat among groups. When we look
at the parameters in the model without parasite groups, there is a
positive relationship between definitive host mass and adult growth.

<div class="kable-table">

|                                                          | param                                 |        lwr |        fit |        upr | sig |
|:---------------------------------------------------------|:--------------------------------------|-----------:|-----------:|-----------:|:----|
| traitrg\_def\_host:def\_host\_mass\_c                    | def\_host\_mass\_c                    |  0.0542614 |  0.1480738 |  0.2483002 | sig |
| traitrg\_def\_host:def\_host\_mass\_c:endo\_def\_c       | def\_host\_mass\_c:endo\_def\_c       | -0.0930118 |  0.0908307 |  0.2749015 | ns  |
| traitrg\_def\_host:endo\_def\_c                          | endo\_def\_c                          |  1.7165383 |  2.5882649 |  3.4205212 | sig |
| traitrg\_def\_host:int\_host\_mass\_c                    | int\_host\_mass\_c                    | -0.3543417 | -0.2893354 | -0.2148663 | sig |
| traitrg\_def\_host:int\_host\_mass\_c:def\_host\_mass\_c | int\_host\_mass\_c:def\_host\_mass\_c | -0.0102461 |  0.0076320 |  0.0251236 | ns  |
| traitrg\_def\_host:int\_host\_mass\_c:endo\_def\_c       | int\_host\_mass\_c:endo\_def\_c       |  0.0582282 |  0.2007777 |  0.3341396 | sig |
| traitrg\_def\_host                                       | traitrg\_def\_host                    |  4.3210560 |  5.9511962 |  7.3686010 | sig |

</div>

Here is how much relative adult growth increased with a doubling of
definitive host mass overall.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.0996718      0.0315429      0.0009975      0.0009975 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## 0.03631 0.07900 0.09997 0.12047 0.16516

And here is how much adult growth decreased with a doubling of
intermediate host mass.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##     -0.1543502      0.0206592      0.0006533      0.0006533 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## -0.1942 -0.1688 -0.1542 -0.1406 -0.1128

However, this decrease depended on whether the definitive host was an
endotherm or not. Adult growth decreased this much with a doubling of
intermediate host mass when the next host was an ectotherm:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##     -0.1809404      0.0205062      0.0006485      0.0006485 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## -0.2178 -0.1950 -0.1817 -0.1676 -0.1384

But much less when the definitive host was an endotherm:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##     -0.1225619      0.0242217      0.0007660      0.0007162 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##     2.5%      25%      50%      75%    97.5% 
    ## -0.16908 -0.13987 -0.12339 -0.10665 -0.07481

Here is the average increase in size in a definitive host (fold change).

<div class="kable-table">

|                    | param              | avg\_fold\_change\_DH\_lwr | avg\_fold\_change\_DH | avg\_fold\_change\_DH\_upr |
|:-------------------|:-------------------|---------------------------:|----------------------:|---------------------------:|
| traitrg\_def\_host | traitrg\_def\_host |                   75.26807 |              384.2126 |                   1585.414 |

</div>

Here is how much adult worms grew in endotherms vs ectotherms.

<div class="kable-table">

| int\_host\_mass\_c | def\_host\_mass\_c | endo\_def | lwr\_rg\_def\_pred | fit\_rg\_def\_pred | upr\_rg\_def\_pred | fold\_change.lwr | fold\_change.fit | fold\_change.upr |
|-------------------:|-------------------:|----------:|-------------------:|-------------------:|-------------------:|-----------------:|-----------------:|-----------------:|
|                  0 |         -0.0276736 |         0 |           3.040176 |           4.654754 |           6.199943 |         20.90891 |         105.0833 |         492.7211 |
|                  0 |         -0.0665247 |         1 |           5.493862 |           7.234802 |           8.643344 |        243.19465 |        1386.8663 |        5672.2666 |

</div>

Here is how much adult worms grew in a small, endothermic definitive
host (10 g)…

<div class="kable-table">

| int\_host\_mass\_c | def\_host\_mass\_c | endo\_def | lwr\_rg\_def\_pred | fit\_rg\_def\_pred | upr\_rg\_def\_pred | fold\_change.lwr | fold\_change.fit | fold\_change.upr |
|-------------------:|-------------------:|----------:|-------------------:|-------------------:|-------------------:|-----------------:|-----------------:|-----------------:|
|                  0 |            -3.8358 |         1 |           4.702795 |           6.509368 |           7.899816 |         110.2549 |         671.4021 |         2696.786 |

</div>

..and in a large endothermic definitive host (10 kg).

<div class="kable-table">

| int\_host\_mass\_c | def\_host\_mass\_c | endo\_def | lwr\_rg\_def\_pred | fit\_rg\_def\_pred | upr\_rg\_def\_pred | fold\_change.lwr | fold\_change.fit | fold\_change.upr |
|-------------------:|-------------------:|----------:|-------------------:|-------------------:|-------------------:|-----------------:|-----------------:|-----------------:|
|                  0 |           5.209859 |         1 |           6.399541 |           8.261085 |           9.757643 |         601.5688 |         3870.292 |         17285.84 |

</div>

How does adult growth compare with larval growth?

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-64-1.png)<!-- -->

What percent of *relative* growth does an average worm (avg host masses)
do in the definitive host, controlling for taxonomy? Another way to
think of this is “doublings” per host. Here is the percent growth in the
definitive host. It is quite evenly split.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##       0.462276       0.057322       0.001813       0.001813 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.3586 0.4279 0.4613 0.4952 0.5738

But this depends on the group. Acanths grow relatively less in the
definitive host, because they have bigger larvae.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##       0.318217       0.052934       0.001674       0.001791 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.2119 0.2839 0.3180 0.3515 0.4228

cestodes:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##       0.446173       0.049985       0.001581       0.001469 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.3456 0.4149 0.4484 0.4759 0.5423

Nematodes grow relatively more as adults than larvae:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##       0.636295       0.075565       0.002390       0.004016 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.5145 0.5906 0.6284 0.6729 0.7979

It is also worth comparing *total* growth in the two hosts, not just
*relative* growth.

Most growth is conducted in the DH. That is not strongly dependent on
correcting for host size, taxonomy, etc.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-70-1.png)<!-- -->

The average worm accumulates around 10 mg in the definitive host.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##        13.0890        15.3873         0.4866         0.4866 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ##  1.450  5.404  9.089 15.489 48.646

By contrast, they average less than 100 ug in the intermediate host.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##          126.7         1698.1           53.7           53.7 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ##   2.812  18.901  35.910  68.985 311.878

Thus, essentially all of the *total* growth is in the DH, controlling
for host masses and taxonomy.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##       0.987850       0.049349       0.001561       0.001561 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.9400 0.9906 0.9960 0.9984 0.9998

This high percentage is essentially the same for acanths:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##       0.977909       0.032467       0.001027       0.001345 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.8920 0.9752 0.9880 0.9945 0.9989

cestodes:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.9934238      0.0156439      0.0004947      0.0007622 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.9640 0.9936 0.9972 0.9988 0.9998

and nematodes:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.9931209      0.0138833      0.0004390      0.0007268 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.9568 0.9935 0.9972 0.9987 0.9997

### Adult development

The average time spent in the definitive host (days at 20 C):

<div class="kable-table">

|                    | param              | avg\_dd\_DH\_lwr | avg\_dd\_DH | avg\_dd\_DH\_upr |
|:-------------------|:-------------------|-----------------:|------------:|-----------------:|
| traitdd\_def\_host | traitdd\_def\_host |         25.93859 |    56.63351 |         122.2511 |

</div>

Adult development was longer in big hosts, but mainly ectotherms, and
shorter when the intermediate host was large and the definitive host was
an ectotherm.

<div class="kable-table">

|                                                          | param                                 |        lwr |        fit |       upr | sig |
|:---------------------------------------------------------|:--------------------------------------|-----------:|-----------:|----------:|:----|
| traitdd\_def\_host:def\_host\_mass\_c                    | def\_host\_mass\_c                    |  0.0305338 |  0.0440570 | 0.0572150 | sig |
| traitdd\_def\_host:def\_host\_mass\_c:endo\_def\_c       | def\_host\_mass\_c:endo\_def\_c       | -0.0226554 |  0.0060539 | 0.0328825 | ns  |
| traitdd\_def\_host:endo\_def\_c                          | endo\_def\_c                          |  0.1524555 |  0.3129598 | 0.4743295 | sig |
| traitdd\_def\_host:int\_host\_mass\_c                    | int\_host\_mass\_c                    | -0.0107016 |  0.0011318 | 0.0134684 | ns  |
| traitdd\_def\_host:int\_host\_mass\_c:def\_host\_mass\_c | int\_host\_mass\_c:def\_host\_mass\_c | -0.0027173 | -0.0000807 | 0.0025454 | ns  |
| traitdd\_def\_host:int\_host\_mass\_c:endo\_def\_c       | int\_host\_mass\_c:endo\_def\_c       | -0.0130772 |  0.0089842 | 0.0317293 | ns  |
| traitdd\_def\_host                                       | traitdd\_def\_host                    |  5.9637822 |  6.7446510 | 7.5141270 | sig |

</div>

Here is the percent increase in adult DT with a doubling of definitive
host mass.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.0313132      0.0048245      0.0001526      0.0001526 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## 0.02190 0.02811 0.03133 0.03463 0.04047

However, this relationship depended on whether the definitive host was
an endotherm or not. Here is how much prepatent periods increased when
the definitive host was an ectotherm:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.0310287      0.0051438      0.0001627      0.0001627 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## 0.02139 0.02750 0.03101 0.03451 0.04046

And when it was an endotherm; a doubling of definitive host mass has
about half the effect on larval developmental time.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.0331712      0.0061960      0.0001959      0.0001815 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## 0.02141 0.02904 0.03312 0.03726 0.04512

Most trends were consistent across groups.

<div class="kable-table">

|                                                                | param                                       |        lwr |        fit |       upr | sig |
|:---------------------------------------------------------------|:--------------------------------------------|-----------:|-----------:|----------:|:----|
| traitdd\_def\_host:def\_host\_mass\_c                          | def\_host\_mass\_c                          | -0.0107925 |  0.0374814 | 0.0825607 | ns  |
| traitdd\_def\_host:def\_host\_mass\_c:endo\_def\_c             | def\_host\_mass\_c:endo\_def\_c             | -0.0217667 |  0.0093358 | 0.0399501 | ns  |
| traitdd\_def\_host:def\_host\_mass\_c:parasite\_phylumCestoda  | def\_host\_mass\_c:parasite\_phylumCestoda  | -0.0487635 |  0.0013487 | 0.0516649 | ns  |
| traitdd\_def\_host:def\_host\_mass\_c:parasite\_phylumNematoda | def\_host\_mass\_c:parasite\_phylumNematoda | -0.0352955 |  0.0146496 | 0.0670334 | ns  |
| traitdd\_def\_host:endo\_def\_c                                | endo\_def\_c                                | -0.4836191 |  0.4064991 | 1.3193294 | ns  |
| traitdd\_def\_host:endo\_def\_c:parasite\_phylumCestoda        | endo\_def\_c:parasite\_phylumCestoda        | -1.3386993 | -0.2234335 | 0.7799323 | ns  |
| traitdd\_def\_host:endo\_def\_c:parasite\_phylumNematoda       | endo\_def\_c:parasite\_phylumNematoda       | -1.0074711 | -0.0641348 | 0.8541242 | ns  |
| traitdd\_def\_host:int\_host\_mass\_c                          | int\_host\_mass\_c                          | -0.0391576 |  0.0110857 | 0.0545024 | ns  |
| traitdd\_def\_host:int\_host\_mass\_c:def\_host\_mass\_c       | int\_host\_mass\_c:def\_host\_mass\_c       | -0.0034666 | -0.0006792 | 0.0023408 | ns  |
| traitdd\_def\_host:int\_host\_mass\_c:endo\_def\_c             | int\_host\_mass\_c:endo\_def\_c             | -0.0181469 |  0.0045237 | 0.0277758 | ns  |
| traitdd\_def\_host:int\_host\_mass\_c:parasite\_phylumCestoda  | int\_host\_mass\_c:parasite\_phylumCestoda  | -0.0533294 | -0.0083460 | 0.0430858 | ns  |
| traitdd\_def\_host:int\_host\_mass\_c:parasite\_phylumNematoda | int\_host\_mass\_c:parasite\_phylumNematoda | -0.0593541 | -0.0121445 | 0.0378870 | ns  |
| traitdd\_def\_host:parasite\_phylumCestoda                     | parasite\_phylumCestoda                     | -1.6706434 | -0.6796517 | 0.3565179 | ns  |
| traitdd\_def\_host:parasite\_phylumNematoda                    | parasite\_phylumNematoda                    | -0.7013709 |  0.0257119 | 0.7417126 | ns  |
| traitdd\_def\_host                                             | traitdd\_def\_host                          |  6.3430604 |  6.9410540 | 7.5331426 | sig |

</div>

How does adult development compare with larval development?

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-83-1.png)<!-- -->

### Size at maturity

The pattern for adult size was similar to adult growth - it increases
with definitive host mass when we do not consider differences among
parasite groups.

<div class="kable-table">

|                                                          | param                                 |        lwr |        fit |       upr | sig |
|:---------------------------------------------------------|:--------------------------------------|-----------:|-----------:|----------:|:----|
| traitfs\_def\_host:def\_host\_mass\_c                    | def\_host\_mass\_c                    |  0.1499538 |  0.2242541 | 0.2988050 | sig |
| traitfs\_def\_host:def\_host\_mass\_c:endo\_def\_c       | def\_host\_mass\_c:endo\_def\_c       | -0.0865543 |  0.0525474 | 0.1970625 | ns  |
| traitfs\_def\_host:endo\_def\_c                          | endo\_def\_c                          |  0.1867126 |  0.8458409 | 1.5457712 | sig |
| traitfs\_def\_host:int\_host\_mass\_c                    | int\_host\_mass\_c                    | -0.0728451 | -0.0188248 | 0.0382038 | ns  |
| traitfs\_def\_host:int\_host\_mass\_c:def\_host\_mass\_c | int\_host\_mass\_c:def\_host\_mass\_c | -0.0127509 |  0.0006576 | 0.0140541 | ns  |
| traitfs\_def\_host:int\_host\_mass\_c:endo\_def\_c       | int\_host\_mass\_c:endo\_def\_c       | -0.0822292 |  0.0254616 | 0.1408018 | ns  |
| traitfs\_def\_host                                       | traitfs\_def\_host                    |  0.8441759 |  2.5837757 | 4.2656379 | sig |

</div>

Here is how much size at maturity increases with a doubling of
definitive host mass.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.1681146      0.0312792      0.0009891      0.0009891 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.1095 0.1456 0.1682 0.1881 0.2301

But the effect is not evident once we allow interactions between
parasite phylua and host traits. Also, unlike for adult growth, there is
no relationship between adult size and intermediate host size.

<div class="kable-table">

|                                                                | param                                       |        lwr |        fit |        upr | sig |
|:---------------------------------------------------------------|:--------------------------------------------|-----------:|-----------:|-----------:|:----|
| traitfs\_def\_host:def\_host\_mass\_c                          | def\_host\_mass\_c                          | -0.0609832 |  0.1722438 |  0.4053767 | ns  |
| traitfs\_def\_host:def\_host\_mass\_c:endo\_def\_c             | def\_host\_mass\_c:endo\_def\_c             | -0.0923113 |  0.0598840 |  0.2302057 | ns  |
| traitfs\_def\_host:def\_host\_mass\_c:parasite\_phylumCestoda  | def\_host\_mass\_c:parasite\_phylumCestoda  | -0.2133262 |  0.0324819 |  0.2903426 | ns  |
| traitfs\_def\_host:def\_host\_mass\_c:parasite\_phylumNematoda | def\_host\_mass\_c:parasite\_phylumNematoda | -0.1727701 |  0.0827832 |  0.3531858 | ns  |
| traitfs\_def\_host:endo\_def\_c                                | endo\_def\_c                                | -0.3541900 |  2.9008074 |  5.9471699 | ns  |
| traitfs\_def\_host:endo\_def\_c:parasite\_phylumCestoda        | endo\_def\_c:parasite\_phylumCestoda        | -6.2139948 | -2.6765056 |  0.7353607 | ns  |
| traitfs\_def\_host:endo\_def\_c:parasite\_phylumNematoda       | endo\_def\_c:parasite\_phylumNematoda       | -5.1944759 | -2.0643554 |  1.3293943 | ns  |
| traitfs\_def\_host:int\_host\_mass\_c                          | int\_host\_mass\_c                          | -0.2012391 |  0.0243190 |  0.2416252 | ns  |
| traitfs\_def\_host:int\_host\_mass\_c:def\_host\_mass\_c       | int\_host\_mass\_c:def\_host\_mass\_c       | -0.0162921 | -0.0012819 |  0.0143083 | ns  |
| traitfs\_def\_host:int\_host\_mass\_c:endo\_def\_c             | int\_host\_mass\_c:endo\_def\_c             | -0.0920529 |  0.0277722 |  0.1370430 | ns  |
| traitfs\_def\_host:int\_host\_mass\_c:parasite\_phylumCestoda  | int\_host\_mass\_c:parasite\_phylumCestoda  | -0.2693463 | -0.0432756 |  0.1909172 | ns  |
| traitfs\_def\_host:int\_host\_mass\_c:parasite\_phylumNematoda | int\_host\_mass\_c:parasite\_phylumNematoda | -0.2708127 | -0.0448138 |  0.1786010 | ns  |
| traitfs\_def\_host:parasite\_phylumCestoda                     | parasite\_phylumCestoda                     | -2.3144574 |  0.1667963 |  2.3997685 | ns  |
| traitfs\_def\_host:parasite\_phylumNematoda                    | parasite\_phylumNematoda                    | -4.9708290 | -2.8452310 | -0.6967435 | sig |
| traitfs\_def\_host                                             | traitfs\_def\_host                          |  1.9384390 |  3.4241254 |  5.1069308 | sig |

</div>

### Age at maturity

Age at maturity tended to increase with definitive host mass.

<div class="kable-table">

|                                                          | param                                 |        lwr |        fit |       upr | sig |
|:---------------------------------------------------------|:--------------------------------------|-----------:|-----------:|----------:|:----|
| traitag\_def\_host:def\_host\_mass\_c                    | def\_host\_mass\_c                    |  0.0235034 |  0.0367844 | 0.0489656 | sig |
| traitag\_def\_host:def\_host\_mass\_c:endo\_def\_c       | def\_host\_mass\_c:endo\_def\_c       | -0.0292540 | -0.0056899 | 0.0197078 | ns  |
| traitag\_def\_host:endo\_def\_c                          | endo\_def\_c                          |  0.1451525 |  0.2888703 | 0.4207591 | sig |
| traitag\_def\_host:int\_host\_mass\_c                    | int\_host\_mass\_c                    |  0.0032340 |  0.0141940 | 0.0249406 | sig |
| traitag\_def\_host:int\_host\_mass\_c:def\_host\_mass\_c | int\_host\_mass\_c:def\_host\_mass\_c | -0.0025200 |  0.0000255 | 0.0022898 | ns  |
| traitag\_def\_host:int\_host\_mass\_c:endo\_def\_c       | int\_host\_mass\_c:endo\_def\_c       | -0.0261592 | -0.0054558 | 0.0145884 | ns  |
| traitag\_def\_host                                       | traitag\_def\_host                    |  6.5913936 |  7.3386926 | 8.0852870 | sig |

</div>

Here is how much age at maturity increased with a doubling of definitive
host mass.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.0256767      0.0046445      0.0001469      0.0001469 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## 0.01642 0.02278 0.02582 0.02870 0.03452

Here are the parameters from the larger model:

<div class="kable-table">

|                                                                | param                                       |        lwr |        fit |       upr | sig |
|:---------------------------------------------------------------|:--------------------------------------------|-----------:|-----------:|----------:|:----|
| traitag\_def\_host:def\_host\_mass\_c                          | def\_host\_mass\_c                          | -0.0145776 |  0.0276577 | 0.0701885 | ns  |
| traitag\_def\_host:def\_host\_mass\_c:endo\_def\_c             | def\_host\_mass\_c:endo\_def\_c             | -0.0296939 | -0.0020634 | 0.0270724 | ns  |
| traitag\_def\_host:def\_host\_mass\_c:parasite\_phylumCestoda  | def\_host\_mass\_c:parasite\_phylumCestoda  | -0.0475535 |  0.0001108 | 0.0439177 | ns  |
| traitag\_def\_host:def\_host\_mass\_c:parasite\_phylumNematoda | def\_host\_mass\_c:parasite\_phylumNematoda | -0.0253375 |  0.0191148 | 0.0652876 | ns  |
| traitag\_def\_host:endo\_def\_c                                | endo\_def\_c                                | -0.6326144 |  0.1697860 | 0.9595638 | ns  |
| traitag\_def\_host:endo\_def\_c:parasite\_phylumCestoda        | endo\_def\_c:parasite\_phylumCestoda        | -1.0837978 | -0.1417741 | 0.7792922 | ns  |
| traitag\_def\_host:endo\_def\_c:parasite\_phylumNematoda       | endo\_def\_c:parasite\_phylumNematoda       | -0.6701585 |  0.1460908 | 1.0074815 | ns  |
| traitag\_def\_host:int\_host\_mass\_c                          | int\_host\_mass\_c                          | -0.0030318 |  0.0373694 | 0.0785583 | ns  |
| traitag\_def\_host:int\_host\_mass\_c:def\_host\_mass\_c       | int\_host\_mass\_c:def\_host\_mass\_c       | -0.0033423 | -0.0006739 | 0.0020242 | ns  |
| traitag\_def\_host:int\_host\_mass\_c:endo\_def\_c             | int\_host\_mass\_c:endo\_def\_c             | -0.0308804 | -0.0103195 | 0.0104804 | ns  |
| traitag\_def\_host:int\_host\_mass\_c:parasite\_phylumCestoda  | int\_host\_mass\_c:parasite\_phylumCestoda  | -0.0640882 | -0.0217944 | 0.0217962 | ns  |
| traitag\_def\_host:int\_host\_mass\_c:parasite\_phylumNematoda | int\_host\_mass\_c:parasite\_phylumNematoda | -0.0703637 | -0.0260927 | 0.0187668 | ns  |
| traitag\_def\_host:parasite\_phylumCestoda                     | parasite\_phylumCestoda                     | -1.5420329 | -0.6584573 | 0.1519261 | ns  |
| traitag\_def\_host:parasite\_phylumNematoda                    | parasite\_phylumNematoda                    | -1.0830770 | -0.3394829 | 0.4263617 | ns  |
| traitag\_def\_host                                             | traitag\_def\_host                          |  7.0971257 |  7.6226121 | 8.2191972 | sig |

</div>

## Plotted model predictions - Figs 3 and 4

We plot the model predictions over the data to understand the patterns,
starting with how the larval host affects life history strategies.

Larval worms grow more and develop longer when the intermediate host is
large, but less when the definitive host is an endotherm (a and b).
Large intermediate hosts are also associated with less adult growth, but
not a small size or age at maturity. This suggests that more growth in
the intermediate host reduces the amount of growth needed to reach an
optimal size for reproduction.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-94-1.png)<!-- -->

What about the effect of the adult environment?

Larval growth is unrelated to definitive host size (a and b). Adult
growth is also only weakly related to definitive host size, though it
tends to be greater in an endotherm.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-96-1.png)<!-- -->

Look at growth rates as function of host traits.

Neither adult or larval growth depended much on host mass or endothermy.
![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-99-1.png)<!-- -->
Here is the average larval growth rate for a worm infecting typically
sized hosts.

<div class="kable-table">

| int\_host\_mass\_c | def\_host\_mass\_c | endo\_def | rgr\_int\_pred.lwr | rgr\_int\_pred.fit | rgr\_int\_pred.upr |
|-------------------:|-------------------:|----------:|-------------------:|-------------------:|-------------------:|
|                  0 |         -0.0276736 |         0 |          0.1067051 |          0.2539907 |          0.6186660 |
|                  0 |         -0.0665247 |         1 |          0.0819543 |          0.2352270 |          0.6305653 |

</div>

Here is the average adult growth rate. It is very similar to the larval
growth rate.

<div class="kable-table">

| int\_host\_mass\_c | def\_host\_mass\_c | endo\_def | rgr\_def\_pred.lwr | rgr\_def\_pred.fit | rgr\_def\_pred.upr |
|-------------------:|-------------------:|----------:|-------------------:|-------------------:|-------------------:|
|                  0 |         -0.0276736 |         0 |          0.0623941 |          0.1645828 |          0.3865205 |
|                  0 |         -0.0665247 |         1 |          0.0696771 |          0.1928490 |          0.4895860 |

</div>

## Model effect sizes

These results suggest that life history is determined by both
intermediate and definitive hosts, whereas adult strategies are
determined by just the definitive host.

Here’s the R<sup>2</sup> for these models.

The host trait interactions explain variation in larval growth, as does
the parasite group by host traits interaction. However, adding parasite
group mostly shifted explanatory power from the random to the fixed
effects (i.e. overall conditional R2 did not change much).

<div class="kable-table">

| trait          | model                                  | r2m                   | r2c                   |
|:---------------|:---------------------------------------|:----------------------|:----------------------|
| larval\_growth | int-only                               | 0 \[0-0\]             | 0.847 \[0.78-0.91\]   |
| larval\_growth | host traits, main effects              | 0.091 \[0.043-0.156\] | 0.843 \[0.772-0.908\] |
| larval\_growth | host traits, second-order interactions | 0.104 \[0.044-0.171\] | 0.843 \[0.771-0.924\] |
| larval\_growth | host traits x parasite group           | 0.437 \[0.254-0.614\] | 0.865 \[0.807-0.916\] |

</div>

The pattern for larval development was similar.

<div class="kable-table">

| trait      | model                                  | r2m                   | r2c                   |
|:-----------|:---------------------------------------|:----------------------|:----------------------|
| larval\_dt | int-only                               | 0 \[0-0\]             | 0.874 \[0.805-0.954\] |
| larval\_dt | host traits, main effects              | 0.06 \[0.019-0.121\]  | 0.871 \[0.794-0.953\] |
| larval\_dt | host traits, second-order interactions | 0.086 \[0.031-0.156\] | 0.875 \[0.809-0.95\]  |
| larval\_dt | host traits x parasite group           | 0.28 \[0.109-0.515\]  | 0.874 \[0.813-0.939\] |

</div>

The model explained less variation in adult growth.

<div class="kable-table">

| trait         | model                                  | r2m                   | r2c                   |
|:--------------|:---------------------------------------|:----------------------|:----------------------|
| adult\_growth | int-only                               | 0 \[0-0\]             | 0.644 \[0.546-0.759\] |
| adult\_growth | host traits, main effects              | 0.192 \[0.109-0.281\] | 0.637 \[0.559-0.737\] |
| adult\_growth | host traits, second-order interactions | 0.216 \[0.127-0.298\] | 0.638 \[0.561-0.75\]  |
| adult\_growth | host traits x parasite group           | 0.338 \[0.216-0.453\] | 0.654 \[0.569-0.745\] |

</div>

Adult developmental times seem to be specific to parasite groups.

<div class="kable-table">

| trait     | model                                  | r2m                   | r2c                   |
|:----------|:---------------------------------------|:----------------------|:----------------------|
| adult\_dt | int-only                               | 0 \[0-0\]             | 0.875 \[0.791-0.957\] |
| adult\_dt | host traits, main effects              | 0.056 \[0.019-0.113\] | 0.892 \[0.826-0.961\] |
| adult\_dt | host traits, second-order interactions | 0.056 \[0.017-0.115\] | 0.891 \[0.825-0.962\] |
| adult\_dt | host traits x parasite group           | 0.274 \[0.075-0.571\] | 0.896 \[0.829-0.951\] |

</div>

Variation in adult size was mostly taxonomic.

<div class="kable-table">

| trait       | model                                  | r2m                   | r2c                   |
|:------------|:---------------------------------------|:----------------------|:----------------------|
| adult\_size | int-only                               | 0 \[0-0\]             | 0.674 \[0.568-0.831\] |
| adult\_size | host traits, main effects              | 0.062 \[0.024-0.116\] | 0.711 \[0.606-0.851\] |
| adult\_size | host traits, second-order interactions | 0.069 \[0.028-0.126\] | 0.708 \[0.611-0.856\] |
| adult\_size | host traits x parasite group           | 0.337 \[0.154-0.532\] | 0.754 \[0.664-0.842\] |

</div>

As was age at maturity.

<div class="kable-table">

| trait      | model                                  | r2m                   | r2c                   |
|:-----------|:---------------------------------------|:----------------------|:----------------------|
| adult\_age | int-only                               | 0 \[0-0\]             | 0.871 \[0.795-0.953\] |
| adult\_age | host traits, main effects              | 0.07 \[0.021-0.136\]  | 0.889 \[0.826-0.962\] |
| adult\_age | host traits, second-order interactions | 0.067 \[0.019-0.124\] | 0.892 \[0.825-0.961\] |
| adult\_age | host traits x parasite group           | 0.24 \[0.089-0.513\]  | 0.887 \[0.826-0.95\]  |

</div>

For all traits, taxonomy is very important. For comparison, we can also
look at the models without taxonomy. The marginal R<sup>2</sup> values
are higher, particularly for larval traits, which suggests that some of
the explanatory power of e.g. host mass is confounded with worm
taxonomy. Even so, much of the variation in parasite life history is
explained better by worm taxonomy than by host traits.

<div class="kable-table">

| trait          | model                                  | r2m                   |
|:---------------|:---------------------------------------|:----------------------|
| adult\_age     | int-only                               | 0 \[0-0\]             |
| adult\_age     | host traits, main effects              | 0.116 \[0.059-0.19\]  |
| adult\_age     | host traits, second-order interactions | 0.149 \[0.089-0.221\] |
| adult\_age     | host traits x parasite group           | 0.255 \[0.175-0.334\] |
| adult\_dt      | int-only                               | 0 \[0-0\]             |
| adult\_dt      | host traits, main effects              | 0.059 \[0.019-0.133\] |
| adult\_dt      | host traits, second-order interactions | 0.116 \[0.063-0.186\] |
| adult\_dt      | host traits x parasite group           | 0.323 \[0.23-0.408\]  |
| adult\_growth  | int-only                               | 0 \[0-0\]             |
| adult\_growth  | host traits, main effects              | 0.315 \[0.256-0.375\] |
| adult\_growth  | host traits, second-order interactions | 0.325 \[0.269-0.385\] |
| adult\_growth  | host traits x parasite group           | 0.424 \[0.369-0.48\]  |
| adult\_size    | int-only                               | 0 \[0-0\]             |
| adult\_size    | host traits, main effects              | 0.075 \[0.04-0.123\]  |
| adult\_size    | host traits, second-order interactions | 0.086 \[0.048-0.129\] |
| adult\_size    | host traits x parasite group           | 0.388 \[0.332-0.442\] |
| larval\_dt     | int-only                               | 0 \[0-0\]             |
| larval\_dt     | host traits, main effects              | 0.113 \[0.06-0.175\]  |
| larval\_dt     | host traits, second-order interactions | 0.131 \[0.077-0.201\] |
| larval\_dt     | host traits x parasite group           | 0.327 \[0.253-0.401\] |
| larval\_growth | int-only                               | 0 \[0-0\]             |
| larval\_growth | host traits, main effects              | 0.258 \[0.196-0.318\] |
| larval\_growth | host traits, second-order interactions | 0.271 \[0.215-0.334\] |
| larval\_growth | host traits x parasite group           | 0.559 \[0.508-0.606\] |

</div>

Below, we partition trait variance by taxonomic level to determine where
in the taxonomic hierarchy parasite differ most.

# Trait covariation

Trait covariation can be assessed before or after accounting for the
fixed effects documented above (i.e. with or without correcting for host
mass and endothermy). It can also be affected by including parasite
taxonomy and taxonomic covariance in the model, i.e. taxonomy may drive
covariance. Therefore, let’s examine how trait covariance estimates
depended on model structure. We examine five models: 1) without fixed
effects or taxonomy (species-level), 2) with fixed effects but not
taxonomy, 3) with taxonomy but not fixed effects, 4) with taxonomy and
fixed effects, and 5) with fixed effects and taxonomic covariance. For
each of these models, we extract the residual covariance between traits
and convert it to a correlation coefficient.

    ## [1] "taxonomic models, imputation 1 finished"
    ## [1] "taxonomic models, imputation 2 finished"
    ## [1] "taxonomic models, imputation 3 finished"
    ## [1] "taxonomic models, imputation 4 finished"
    ## [1] "taxonomic models, imputation 5 finished"
    ## [1] "taxonomic models, imputation 6 finished"
    ## [1] "taxonomic models, imputation 7 finished"
    ## [1] "taxonomic models, imputation 8 finished"
    ## [1] "taxonomic models, imputation 9 finished"
    ## [1] "taxonomic models, imputation 10 finished"
    ## [1] "taxonomic models, imputation 11 finished"
    ## [1] "taxonomic models, imputation 12 finished"
    ## [1] "taxonomic models, imputation 13 finished"
    ## [1] "taxonomic models, imputation 14 finished"
    ## [1] "taxonomic models, imputation 15 finished"
    ## [1] "taxonomic models, imputation 16 finished"
    ## [1] "taxonomic models, imputation 17 finished"
    ## [1] "taxonomic models, imputation 18 finished"
    ## [1] "taxonomic models, imputation 19 finished"
    ## [1] "taxonomic models, imputation 20 finished"
    ## [1] "taxonomic models, imputation 21 finished"
    ## [1] "taxonomic models, imputation 22 finished"
    ## [1] "taxonomic models, imputation 23 finished"
    ## [1] "taxonomic models, imputation 24 finished"
    ## [1] "taxonomic models, imputation 25 finished"
    ## [1] "taxonomic models, imputation 26 finished"
    ## [1] "taxonomic models, imputation 27 finished"
    ## [1] "taxonomic models, imputation 28 finished"
    ## [1] "taxonomic models, imputation 29 finished"
    ## [1] "taxonomic models, imputation 30 finished"
    ## [1] "taxonomic models, imputation 31 finished"
    ## [1] "taxonomic models, imputation 32 finished"
    ## [1] "taxonomic models, imputation 33 finished"
    ## [1] "taxonomic models, imputation 34 finished"
    ## [1] "taxonomic models, imputation 35 finished"
    ## [1] "taxonomic models, imputation 36 finished"
    ## [1] "taxonomic models, imputation 37 finished"
    ## [1] "taxonomic models, imputation 38 finished"
    ## [1] "taxonomic models, imputation 39 finished"
    ## [1] "taxonomic models, imputation 40 finished"
    ## [1] "taxonomic models, imputation 41 finished"
    ## [1] "taxonomic models, imputation 42 finished"
    ## [1] "taxonomic models, imputation 43 finished"
    ## [1] "taxonomic models, imputation 44 finished"
    ## [1] "taxonomic models, imputation 45 finished"
    ## [1] "taxonomic models, imputation 46 finished"
    ## [1] "taxonomic models, imputation 47 finished"
    ## [1] "taxonomic models, imputation 48 finished"
    ## [1] "taxonomic models, imputation 49 finished"
    ## [1] "taxonomic models, imputation 50 finished"
    ## [1] "taxonomic models, imputation 51 finished"
    ## [1] "taxonomic models, imputation 52 finished"
    ## [1] "taxonomic models, imputation 53 finished"
    ## [1] "taxonomic models, imputation 54 finished"
    ## [1] "taxonomic models, imputation 55 finished"
    ## [1] "taxonomic models, imputation 56 finished"
    ## [1] "taxonomic models, imputation 57 finished"
    ## [1] "taxonomic models, imputation 58 finished"
    ## [1] "taxonomic models, imputation 59 finished"
    ## [1] "taxonomic models, imputation 60 finished"
    ## [1] "taxonomic models, imputation 61 finished"
    ## [1] "taxonomic models, imputation 62 finished"
    ## [1] "taxonomic models, imputation 63 finished"
    ## [1] "taxonomic models, imputation 64 finished"
    ## [1] "taxonomic models, imputation 65 finished"
    ## [1] "taxonomic models, imputation 66 finished"
    ## [1] "taxonomic models, imputation 67 finished"
    ## [1] "taxonomic models, imputation 68 finished"
    ## [1] "taxonomic models, imputation 69 finished"
    ## [1] "taxonomic models, imputation 70 finished"
    ## [1] "taxonomic models, imputation 71 finished"
    ## [1] "taxonomic models, imputation 72 finished"
    ## [1] "taxonomic models, imputation 73 finished"
    ## [1] "taxonomic models, imputation 74 finished"
    ## [1] "taxonomic models, imputation 75 finished"
    ## [1] "taxonomic models, imputation 76 finished"
    ## [1] "taxonomic models, imputation 77 finished"
    ## [1] "taxonomic models, imputation 78 finished"
    ## [1] "taxonomic models, imputation 79 finished"
    ## [1] "taxonomic models, imputation 80 finished"
    ## [1] "taxonomic models, imputation 81 finished"
    ## [1] "taxonomic models, imputation 82 finished"
    ## [1] "taxonomic models, imputation 83 finished"
    ## [1] "taxonomic models, imputation 84 finished"
    ## [1] "taxonomic models, imputation 85 finished"
    ## [1] "taxonomic models, imputation 86 finished"
    ## [1] "taxonomic models, imputation 87 finished"
    ## [1] "taxonomic models, imputation 88 finished"
    ## [1] "taxonomic models, imputation 89 finished"
    ## [1] "taxonomic models, imputation 90 finished"
    ## [1] "taxonomic models, imputation 91 finished"
    ## [1] "taxonomic models, imputation 92 finished"
    ## [1] "taxonomic models, imputation 93 finished"
    ## [1] "taxonomic models, imputation 94 finished"
    ## [1] "taxonomic models, imputation 95 finished"
    ## [1] "taxonomic models, imputation 96 finished"
    ## [1] "taxonomic models, imputation 97 finished"
    ## [1] "taxonomic models, imputation 98 finished"
    ## [1] "taxonomic models, imputation 99 finished"
    ## [1] "taxonomic models, imputation 100 finished"

Here are the correlations from the five models for the 15 trait
combinations. Adding fixed effects to a non-taxonomic model (compare red
points) sometimes shrank the correlation (6 cases), sometimes increased
the correlation (4), or had no effect (5). Once taxonomy was included in
the model, the correlations were not sensitive to the fixed effects
(compare green points), presumably because the fixed effects like host
mass were taxonomically structured. This is presumably also why adding
taxonomy moved correlations in the same direction as adding fixed
effects (compare red vs green points). In a few cases (\~7), the
correlations disappeared after we added taxonomic covariance (blue
points), indicating that the species-level correlation is entirely
explained by correlations at higher taxonomic levels.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-115-1.png)<!-- -->

Here is another way to visualize the differences. We focus on just the
relationship between growth and development in intermediate hosts and we
plot the marginal residuals (i.e. accounting for fixed effects but not
taxonomy) from the taxonomic mixed model. The covariance matrix that
fits best is the one estimated with fixed effects but without taxonomy.
The covariance is too wide when estimated without fixed effects and too
narrow when accounting for taxonomy.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-117-1.png)<!-- -->

Even though taxonomy and the fixed effects can alter trait correlations,
the estimates were still rather similar. Here is the pearson correlation
for the covariances with and without fixed effects (no taxonomy).

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  cors_wide$cor.fit_no_fixed_no_tax and cors_wide$cor.fit_fixed_no_tax
    ## t = 8.1111, df = 13, p-value = 1.922e-06
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  0.7548823 0.9713576
    ## sample estimates:
    ##       cor 
    ## 0.9137858

With taxonomy, the correlation with and without fixed effects is much
tighter.

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  cors_wide$cor.fit_no_fixed_tax and cors_wide$cor.fit_fixed_tax
    ## t = 105.71, df = 13, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  0.9981991 0.9998125
    ## sample estimates:
    ##       cor 
    ## 0.9994188

Here is the trend with fixed effects, but with and without taxonomy. It
is quite high.

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  cors_wide$cor.fit_fixed_no_tax and cors_wide$cor.fit_fixed_tax
    ## t = 13.221, df = 13, p-value = 6.482e-09
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  0.8946571 0.9884995
    ## sample estimates:
    ##       cor 
    ## 0.9647674

It is lower, though, when we compare correlations without taxonomy and
fixed effects to those with taxonomy and fixed effects. This indicates
that taxonomy and fixed effects can shift correlations somewhat.

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  cors_wide$cor.fit_no_fixed_no_tax and cors_wide$cor.fit_fixed_tax
    ## t = 4.9501, df = 13, p-value = 0.0002654
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  0.5052585 0.9338828
    ## sample estimates:
    ##       cor 
    ## 0.8083103

We therefore proceed with residuals “correcting” for fixed effects but
not taxonomy; taxonomic covariance is considered later. To visualize
covariances, we calculate confidence ellipses. The width of the ellipses
represent variance, whereas the tilt represents covariance.

Let’s look at the correlations between size and age within growth
periods, i.e. within intermediate hosts, within definitive hosts and
over the whole life cycle. In each case, it is significantly positive,
though some species grow faster than others (upper left quadrant). The
colors code an index of performance (the average of the standardized
residuals for size and inverse age).

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-122-1.png)<!-- -->

What about correlations across life stages? We consider 5 adult traits:
adult growth, adult developmental time (prepatent period), adult growth
rate, size at maturity, and age at maturity. We looked at how those
traits were affected by larval strategies (larval growth, developmental
time, and growth rate). These correlations are calculated after
accounting for host traits and parasite group (i.e. with fixed effects
removed). So these are worms that grow more/less, fast/slow, etc.
relative to host size and parasite group. Note though that host traits
had little impact on growth rate, so the residuals for larval growth
rate are similar to observed rates.

We start with adult growth.

We expected that worms that grow more in intermediate hosts should grow
less in definitive hosts. This is clearly the case. Parasite species
that grew more and faster as larvae grew less as adults. Long larval
development did not affect adult growth. Slow larval growth was
associated with more adult growth.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-126-1.png)<!-- -->
Moving on to the next adult trait: prepatent period.

Species that had slow larval growth and long larval development tended
to have longer prepatent periods. By contrast, worms with fast larval
growth tended to have slightly shorter prepatent periods.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-128-1.png)<!-- -->

Since fast growing larvae exhibit shorter adult development and less
adult growth, we would not expect adult growth rates to depend on larval
traits. Let’s check.

Indeed, larval and adult growth rates were uncorrelated. However, worms
that grew more and longer as larvae tended to grow slower as adults.
However, this trend might be a bit spurious, since the 3 groups seem to
separate out.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-130-1.png)<!-- -->

Here is the same plot separated for each group. It is less clear that
there is a consistent negative relationship. Also, cestodes and
nematodes separate along the x-axis, suggesting that the model considers
their growth relative to the host different. This is probably influenced
by taxonomic effects, i.e. some points have more weight than others.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-131-1.png)<!-- -->

Here is the simple pearson correlation for acanths,

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  rg_int_res and rgr_def_res
    ## t = -1.2575, df = 63, p-value = 0.2132
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.38566226  0.09088554
    ## sample estimates:
    ##        cor 
    ## -0.1564823

cestodes, and…

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  rg_int_res and rgr_def_res
    ## t = -10.438, df = 265, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.6196534 -0.4487926
    ## sample estimates:
    ##        cor 
    ## -0.5397585

nematodes.

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  rg_int_res and rgr_def_res
    ## t = -8.9242, df = 263, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.5695252 -0.3839171
    ## sample estimates:
    ##        cor 
    ## -0.4821125

One reason that adult growth rate may decrease with larval growth is
that growth rates overall decrease with size/age. In other words, the
biggest larvae are on the part of the curve where growth typically
slows. Let’s examine this.

We fit growth curves (age vs size) separately for each helminth group.

The curve is a better fit than a line, as the residual standard errors
are lower for acanths…

<div class="kable-table">

| line\_res\_se | curve\_res\_se | prop\_dec |
|--------------:|---------------:|----------:|
|      2.837053 |       1.493157 | 0.4736944 |

</div>

…cestodes…

<div class="kable-table">

| line\_res\_se | curve\_res\_se | prop\_dec |
|--------------:|---------------:|----------:|
|      3.963428 |       2.748519 | 0.3065299 |

</div>

…and nematodes.

<div class="kable-table">

| line\_res\_se | curve\_res\_se | prop\_dec |
|--------------:|---------------:|----------:|
|       3.65538 |       1.905884 | 0.4786085 |

</div>

We confirm this by plotting the curves (dotted lines). They fit better
than a straight line (red; this pure exponential growth given the log
transformed y-axis). Growth clearly slows with size/age.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-143-1.png)<!-- -->

We can also reformulate the data to plot growth rate as a function of
age. The dashed lines are from the fitted curves. Relative growth rate
decreases with age. Moreover, this formulation shows us that growth
rates vary more among young worms (i.e. when there is a low value for
age in the denominator of the growth rate calculation).

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-144-1.png)<!-- -->

We can make the same plot with size instead of age on the x-axis.
Relative growth rate decreases in larger worms, though there is more
variation when worms are small.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-145-1.png)<!-- -->

Therefore, the worms that grow more and longer as larvae (i.e. are
further to right on the last two plots) are expected to have lower adult
growth rates. Here is an easier way to see that. The species are split
by their larval style (i.e. if they grew more/longer than expected or
less/shorter). Species that grew more/longer as larvae tended to have
slower adult growth.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-147-1.png)<!-- -->

Decelerating growth is not obviously driven by single taxa. When we fit
curves to family averages (red), they are quite comparable to the curves
fit to species values (blue).

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-148-1.png)<!-- -->

Taxa that fall above or below these curves grew faster or slower than
expected, given the deceleration in growth rates overall. Thus, the
residuals around the curve can hint at whether more larval growth is
associated with slower adult growth than expected.

Here are the curves’ residuals plotted as a function of larval growth.
There is not a trend for larger larvae to end up with larger adults than
expected.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-150-1.png)<!-- -->

Here are the residuals plotted as a function of larval developmental
time. At least in cestodes, species with longer larval development
tended to have smaller adult sizes than expected.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-151-1.png)<!-- -->

Now let’s move on to size at maturity. Even if worms grow more than
expected as larvae, they are not predicted to have a
larger-than-expected size at maturity.

Indeed, worms that grew more than expected as larvae did not reach
larger final sizes. However, prolonged larval development was associated
with larger sizes at maturity. As a consequence, slow larval growth was
associated with larger reproductive sizes.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-153-1.png)<!-- -->

The final adult trait is age at maturity, which depends on the time
spent developing both as a larva and as an adult.

Species with larvae that had prolonged larval development and slow
growth had later ages at maturity, as we would expect.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-155-1.png)<!-- -->

When we put it all together, we find that species that grow more as
larvae grow less as adults but do not mature at a smaller final size.
Slow larval development is associated with slow adult development and
larger final adult sizes. This is consistent with developmental rate as
a species (or taxon) trait.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-156-1.png)<!-- -->

## Taxonomic trait covariation

Are the correlations above happening at a deeper taxonomic level? For
example, are species that grow more as larvae and less as adults all in
the same genus, family, etc. To get at this, we can ask what taxonomic
levels account for the variation in parasite growth and development? Are
the differences between genera or between classes? And is it the same
for every parasite trait? we can extract this information from the mixed
models.

Here is the variance explained by each taxonomic level in the models
without fixed effects. Uncertainty in the effects increase up the
taxonomic hierarchy. Growth traits vary most among families.
Developmental times also vary among families, but among orders and
classes too.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-159-1.png)<!-- -->

Here is the same plot but for the model including fixed effects.
Overall, the taxonomic effects decrease. Adult traits still tend to vary
more among genera than larval traits, but the differences deeper in the
phylogeny are not as clear.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-160-1.png)<!-- -->

Now let’s fit a model allowing taxonomic trait covariance, i.e. taxa
with high values for trait 1 may have higher or lower values for trait
2. To see where covariance arises, we add taxonomic levels from root to
tip. For example, we test covariance among orders and then, controlling
for order-level effects, we test whether there is covariance among
parasite families and so on.

Overall, adding taxonomic covariance is an improvement, at least judged
by model DIC. Also, below we see that covariances are significantly
different from zero.

    ## Delta DIC, +taxonomic covariance:  669.6054

Here are the number of distinct families that were included in the model

    ## [1] 86

Here are families that grew more as larvae than expected (large random
effects).

<div class="kable-table">

|                                                      | fam              |    re\_lwr |       re |  re\_upr |
|:-----------------------------------------------------|:-----------------|-----------:|---------:|---------:|
| traitrg\_int\_host.parasite\_family.Taeniidae        | Taeniidae        |  4.6515221 | 6.409386 | 8.306166 |
| traitrg\_int\_host.parasite\_family.Hedruridae       | Hedruridae       |  2.4523100 | 4.239908 | 6.048800 |
| traitrg\_int\_host.parasite\_family.Hartertiidae     | Hartertiidae     |  1.9248669 | 3.960189 | 6.265763 |
| traitrg\_int\_host.parasite\_family.Gnathostomatidae | Gnathostomatidae |  1.8694741 | 3.827768 | 5.760509 |
| traitrg\_int\_host.parasite\_family.Rhinebothriidae  | Rhinebothriidae  | -0.5110322 | 3.049619 | 6.645828 |
| traitrg\_int\_host.parasite\_family.Ophidascaridae   | Ophidascaridae   |  1.1929022 | 2.933022 | 4.747257 |
| traitrg\_int\_host.parasite\_family.Dioctophymidae   | Dioctophymidae   | -1.0227480 | 2.787764 | 6.608444 |
| traitrg\_int\_host.parasite\_family.Acrobothriidae   | Acrobothriidae   | -0.4613413 | 2.744995 | 5.608822 |
| traitrg\_int\_host.parasite\_family.Cystidicolidae   | Cystidicolidae   |  0.8675516 | 2.171801 | 3.696572 |
| traitrg\_int\_host.parasite\_family.Illiosentidae    | Illiosentidae    | -0.2230194 | 1.973162 | 4.091337 |

</div>

Here are the families that grew less as larvae than expected.

<div class="kable-table">

|                                                      | fam              |   re\_lwr |        re |    re\_upr |
|:-----------------------------------------------------|:-----------------|----------:|----------:|-----------:|
| traitrg\_int\_host.parasite\_family.Dracunculidae    | Dracunculidae    | -6.746683 | -4.726265 | -2.7318080 |
| traitrg\_int\_host.parasite\_family.Philometridae    | Philometridae    | -6.201717 | -4.702409 | -3.1231146 |
| traitrg\_int\_host.parasite\_family.Strongylidae     | Strongylidae     | -6.497189 | -3.461506 | -0.7247234 |
| traitrg\_int\_host.parasite\_family.Anoplocephalidae | Anoplocephalidae | -4.269285 | -2.704298 | -1.1118168 |
| traitrg\_int\_host.parasite\_family.Micropleuridae   | Micropleuridae   | -5.011993 | -2.487061 | -0.1310446 |
| traitrg\_int\_host.parasite\_family.Hymenolepididae  | Hymenolepididae  | -3.719566 | -2.361403 | -0.7433914 |
| traitrg\_int\_host.parasite\_family.Camallanidae     | Camallanidae     | -3.706308 | -2.205745 | -0.6835278 |
| traitrg\_int\_host.parasite\_family.Syngamidae       | Syngamidae       | -4.366030 | -2.156637 | -0.2089570 |
| traitrg\_int\_host.parasite\_family.Guyanemidae      | Guyanemidae      | -4.805099 | -2.124242 |  0.3287479 |
| traitrg\_int\_host.parasite\_family.Heterakidae      | Heterakidae      | -4.074175 | -2.116944 |  0.1173581 |

</div>

Here are the worm families that developed longer than expected as
larvae.

<div class="kable-table">

|                                                       | fam               |    re\_lwr |        re |   re\_upr |
|:------------------------------------------------------|:------------------|-----------:|----------:|----------:|
| traitdd\_int\_host.parasite\_family.Ophidascaridae    | Ophidascaridae    |  0.5929314 | 1.0149863 | 1.4689312 |
| traitdd\_int\_host.parasite\_family.Taeniidae         | Taeniidae         |  0.5663887 | 0.9865839 | 1.4516846 |
| traitdd\_int\_host.parasite\_family.Hedruridae        | Hedruridae        |  0.3791726 | 0.7709990 | 1.1676295 |
| traitdd\_int\_host.parasite\_family.Anisakidae        | Anisakidae        |  0.1161797 | 0.7067623 | 1.3250788 |
| traitdd\_int\_host.parasite\_family.Dioctophymidae    | Dioctophymidae    | -0.3058513 | 0.6372965 | 1.5169932 |
| traitdd\_int\_host.parasite\_family.Anoplocephalidae  | Anoplocephalidae  |  0.2498538 | 0.5989754 | 0.9625504 |
| traitdd\_int\_host.parasite\_family.Thelaziidae       | Thelaziidae       |  0.0042734 | 0.4908195 | 0.9714071 |
| traitdd\_int\_host.parasite\_family.Protostrongylidae | Protostrongylidae |  0.0646470 | 0.4822615 | 0.8424010 |
| traitdd\_int\_host.parasite\_family.Hartertiidae      | Hartertiidae      | -0.0368700 | 0.4616439 | 0.9653833 |
| traitdd\_int\_host.parasite\_family.Gnathostomatidae  | Gnathostomatidae  | -0.0543194 | 0.4410121 | 0.9756325 |

</div>

Here are the families that developed shorter than expected as larvae.

<div class="kable-table">

|                                                       | fam               |    re\_lwr |         re |    re\_upr |
|:------------------------------------------------------|:------------------|-----------:|-----------:|-----------:|
| traitdd\_int\_host.parasite\_family.Heterakidae       | Heterakidae       | -1.6471137 | -1.1070707 | -0.5520431 |
| traitdd\_int\_host.parasite\_family.Syngamidae        | Syngamidae        | -1.5313419 | -0.9943957 | -0.5212103 |
| traitdd\_int\_host.parasite\_family.Dracunculidae     | Dracunculidae     | -1.3944216 | -0.9288313 | -0.4372466 |
| traitdd\_int\_host.parasite\_family.Strongylidae      | Strongylidae      | -1.6080492 | -0.9030374 | -0.1941519 |
| traitdd\_int\_host.parasite\_family.Kathlaniidae      | Kathlaniidae      | -1.2520612 | -0.6181307 | -0.0067502 |
| traitdd\_int\_host.parasite\_family.Hymenolepididae   | Hymenolepididae   | -0.9151538 | -0.5904948 | -0.2760881 |
| traitdd\_int\_host.parasite\_family.Raphidascarididae | Raphidascarididae | -0.9539657 | -0.4437654 |  0.0593875 |
| traitdd\_int\_host.parasite\_family.Rictulariidae     | Rictulariidae     | -0.7752293 | -0.4416354 | -0.0958085 |
| traitdd\_int\_host.parasite\_family.Seuratidae        | Seuratidae        | -0.9032855 | -0.4394057 |  0.0542793 |
| traitdd\_int\_host.parasite\_family.Onchobothriidae   | Onchobothriidae   | -0.9385447 | -0.4013584 |  0.2078005 |

</div>

Let’s combine these into a single measure for larval growth/development.
We standardize the random effects for larval growth and development,
then we average them. Positive values are families that grew more/longer
than expected. Here are those families:

<div class="kable-table">

|                                                      | fam              |    re\_lwr |       re |   re\_upr |    t1\_lwr |        t1 |   t1\_upr |    t2\_lwr |       t2 |  t2\_upr |
|:-----------------------------------------------------|:-----------------|-----------:|---------:|----------:|-----------:|----------:|----------:|-----------:|---------:|---------:|
| traitdd\_int\_host.parasite\_family.Taeniidae        | Taeniidae        |  5.3827284 | 7.837192 | 10.322568 |  0.5663887 | 0.9865839 | 1.4516846 |  4.6515221 | 6.409386 | 8.306166 |
| traitdd\_int\_host.parasite\_family.Hedruridae       | Hedruridae       |  3.1117025 | 5.216562 |  7.597830 |  0.3791726 | 0.7709990 | 1.1676295 |  2.4523100 | 4.239908 | 6.048800 |
| traitdd\_int\_host.parasite\_family.Hartertiidae     | Hartertiidae     |  2.3039492 | 4.631188 |  7.342663 | -0.0368700 | 0.4616439 | 0.9653833 |  1.9248669 | 3.960189 | 6.265763 |
| traitdd\_int\_host.parasite\_family.Gnathostomatidae | Gnathostomatidae |  2.2295835 | 4.487591 |  6.910840 | -0.0543194 | 0.4410121 | 0.9756325 |  1.8694741 | 3.827768 | 5.760509 |
| traitdd\_int\_host.parasite\_family.Ophidascaridae   | Ophidascaridae   |  2.0973799 | 4.146462 |  6.337590 |  0.5929314 | 1.0149863 | 1.4689312 |  1.1929022 | 2.933022 | 4.747257 |
| traitdd\_int\_host.parasite\_family.Dioctophymidae   | Dioctophymidae   | -1.1641623 | 3.572499 |  7.911430 | -0.3058513 | 0.6372965 | 1.5169932 | -1.0227480 | 2.787764 | 6.608444 |
| traitdd\_int\_host.parasite\_family.Rhinebothriidae  | Rhinebothriidae  | -0.7940698 | 3.432570 |  7.820584 | -0.6062679 | 0.1989073 | 1.0325555 | -0.5110322 | 3.049619 | 6.645828 |
| traitdd\_int\_host.parasite\_family.Acrobothriidae   | Acrobothriidae   | -0.5445596 | 3.234719 |  6.555076 | -0.3606774 | 0.3108298 | 1.0201253 | -0.4613413 | 2.744995 | 5.608822 |
| traitdd\_int\_host.parasite\_family.Cystidicolidae   | Cystidicolidae   |  1.0792436 | 2.718827 |  4.420568 |  0.0605798 | 0.3985146 | 0.7510170 |  0.8675516 | 2.171801 | 3.696572 |
| traitdd\_int\_host.parasite\_family.Anisakidae       | Anisakidae       | -0.5505492 | 2.344857 |  5.127688 |  0.1161797 | 0.7067623 | 1.3250788 | -0.8811412 | 1.528768 | 3.862825 |

</div>

And here are the families that grew less than expected as larvae:

<div class="kable-table">

|                                                     | fam             |   re\_lwr |        re |    re\_upr |    t1\_lwr |         t1 |    t1\_upr |   t2\_lwr |        t2 |    t2\_upr |
|:----------------------------------------------------|:----------------|----------:|----------:|-----------:|-----------:|-----------:|-----------:|----------:|----------:|-----------:|
| traitdd\_int\_host.parasite\_family.Dracunculidae   | Dracunculidae   | -8.420686 | -5.964608 | -3.5224419 | -1.3944216 | -0.9288313 | -0.4372466 | -6.746683 | -4.726265 | -2.7318080 |
| traitdd\_int\_host.parasite\_family.Philometridae   | Philometridae   | -7.327536 | -5.149918 | -3.1626241 | -0.5741048 | -0.2033961 |  0.1560942 | -6.201717 | -4.702409 | -3.1231146 |
| traitdd\_int\_host.parasite\_family.Strongylidae    | Strongylidae    | -7.819005 | -4.642108 | -1.3245736 | -1.6080492 | -0.9030374 | -0.1941519 | -6.497189 | -3.461506 | -0.7247234 |
| traitdd\_int\_host.parasite\_family.Heterakidae     | Heterakidae     | -5.791189 | -3.381446 | -0.6612583 | -1.6471137 | -1.1070707 | -0.5520431 | -4.074175 | -2.116944 |  0.1173581 |
| traitdd\_int\_host.parasite\_family.Syngamidae      | Syngamidae      | -5.832861 | -3.311423 | -1.0154945 | -1.5313419 | -0.9943957 | -0.5212103 | -4.366030 | -2.156637 | -0.2089570 |
| traitdd\_int\_host.parasite\_family.Hymenolepididae | Hymenolepididae | -4.895636 | -3.074290 | -1.1538955 | -0.9151538 | -0.5904948 | -0.2760881 | -3.719566 | -2.361403 | -0.7433914 |
| traitdd\_int\_host.parasite\_family.Micropleuridae  | Micropleuridae  | -5.886106 | -2.858214 |  0.0189205 | -0.7871401 | -0.2194554 |  0.3709408 | -5.011993 | -2.487061 | -0.1310446 |
| traitdd\_int\_host.parasite\_family.Kathlaniidae    | Kathlaniidae    | -5.726481 | -2.787093 |  0.6391877 | -1.2520612 | -0.6181307 | -0.0067502 | -4.462263 | -2.031350 |  0.7845818 |
| traitdd\_int\_host.parasite\_family.Onchobothriidae | Onchobothriidae | -5.820406 | -2.659548 |  0.5743450 | -0.9385447 | -0.4013584 |  0.2078005 | -4.737698 | -2.103465 |  0.5629292 |
| traitdd\_int\_host.parasite\_family.Camallanidae    | Camallanidae    | -4.323285 | -2.465636 | -0.5844169 | -0.4914491 | -0.1299274 |  0.2280662 | -3.706308 | -2.205745 | -0.6835278 |

</div>

Moving on to adult growth, here are the families that grew more as
adults than expected.

<div class="kable-table">

|                                                       | fam               |    re\_lwr |       re |  re\_upr |
|:------------------------------------------------------|:------------------|-----------:|---------:|---------:|
| traitrg\_def\_host.parasite\_family.Philometridae     | Philometridae     |  3.7179925 | 5.520221 | 7.187329 |
| traitrg\_def\_host.parasite\_family.Dracunculidae     | Dracunculidae     |  2.5492587 | 4.848464 | 7.170719 |
| traitrg\_def\_host.parasite\_family.Anoplocephalidae  | Anoplocephalidae  |  2.9414835 | 4.590363 | 6.160978 |
| traitrg\_def\_host.parasite\_family.Strongylidae      | Strongylidae      |  1.3507620 | 4.517640 | 7.708411 |
| traitrg\_def\_host.parasite\_family.Bothriocephalidae | Bothriocephalidae |  0.1229513 | 2.631345 | 5.171433 |
| traitrg\_def\_host.parasite\_family.Diplotriaenidae   | Diplotriaenidae   |  0.9512895 | 2.573244 | 4.150519 |
| traitrg\_def\_host.parasite\_family.Syngamidae        | Syngamidae        |  0.0677853 | 2.399301 | 4.799656 |
| traitrg\_def\_host.parasite\_family.Cystoopsidae      | Cystoopsidae      | -0.6844500 | 2.369390 | 5.385679 |
| traitrg\_def\_host.parasite\_family.Micropleuridae    | Micropleuridae    | -0.7614129 | 2.212303 | 5.151429 |
| traitrg\_def\_host.parasite\_family.Linstowiidae      | Linstowiidae      | -0.5491361 | 1.912210 | 4.446810 |

</div>

Here are the families that grew less as adults than expected.

<div class="kable-table">

|                                                       | fam               |   re\_lwr |        re |    re\_upr |
|:------------------------------------------------------|:------------------|----------:|----------:|-----------:|
| traitrg\_def\_host.parasite\_family.Cystidicolidae    | Cystidicolidae    | -4.783605 | -3.257260 | -1.6574972 |
| traitrg\_def\_host.parasite\_family.Habronematidae    | Habronematidae    | -4.905733 | -3.121596 | -1.5715652 |
| traitrg\_def\_host.parasite\_family.Hedruridae        | Hedruridae        | -5.143625 | -3.087984 | -0.8400945 |
| traitrg\_def\_host.parasite\_family.Schistotaeniidae  | Schistotaeniidae  | -5.054982 | -2.852750 | -0.6327679 |
| traitrg\_def\_host.parasite\_family.Taeniidae         | Taeniidae         | -4.670157 | -2.509534 | -0.5639718 |
| traitrg\_def\_host.parasite\_family.Acrobothriidae    | Acrobothriidae    | -5.093483 | -2.431409 |  0.4149883 |
| traitrg\_def\_host.parasite\_family.Protostrongylidae | Protostrongylidae | -4.247623 | -2.428877 | -0.8165936 |
| traitrg\_def\_host.parasite\_family.Illiosentidae     | Illiosentidae     | -4.816911 | -2.244836 |  0.0515639 |
| traitrg\_def\_host.parasite\_family.Thelaziidae       | Thelaziidae       | -4.466551 | -2.214257 |  0.2191891 |
| traitrg\_def\_host.parasite\_family.Hartertiidae      | Hartertiidae      | -4.655172 | -2.136393 |  0.0954736 |

</div>

Here are the families that had longer prepatent periods than expected.

<div class="kable-table">

|                                                      | fam              |    re\_lwr |        re |   re\_upr |
|:-----------------------------------------------------|:-----------------|-----------:|----------:|----------:|
| traitdd\_def\_host.parasite\_family.Strongylidae     | Strongylidae     |  0.7762370 | 1.3515080 | 1.9800585 |
| traitdd\_def\_host.parasite\_family.Trichosomoididae | Trichosomoididae |  0.1455467 | 0.7883555 | 1.4329727 |
| traitdd\_def\_host.parasite\_family.Taeniidae        | Taeniidae        |  0.3689436 | 0.7617736 | 1.1672795 |
| traitdd\_def\_host.parasite\_family.Dracunculidae    | Dracunculidae    |  0.2716049 | 0.6765590 | 1.1158293 |
| traitdd\_def\_host.parasite\_family.Anoplocephalidae | Anoplocephalidae |  0.3404113 | 0.6675059 | 0.9962387 |
| traitdd\_def\_host.parasite\_family.Ophidascaridae   | Ophidascaridae   |  0.2647525 | 0.6514530 | 1.0334019 |
| traitdd\_def\_host.parasite\_family.Diplotriaenidae  | Diplotriaenidae  |  0.2874070 | 0.5871114 | 0.8938272 |
| traitdd\_def\_host.parasite\_family.Philometridae    | Philometridae    |  0.1848023 | 0.5004886 | 0.8178478 |
| traitdd\_def\_host.parasite\_family.Amphilinidae     | Amphilinidae     | -0.1388080 | 0.4603054 | 1.0405150 |
| traitdd\_def\_host.parasite\_family.Gnathostomatidae | Gnathostomatidae | -0.0569869 | 0.3732066 | 0.8066279 |

</div>

Here are the families that had shorter prepatent periods than expected.

<div class="kable-table">

|                                                      | fam              |    re\_lwr |         re |    re\_upr |
|:-----------------------------------------------------|:-----------------|-----------:|-----------:|-----------:|
| traitdd\_def\_host.parasite\_family.Syngamidae       | Syngamidae       | -1.1393835 | -0.6947678 | -0.2365107 |
| traitdd\_def\_host.parasite\_family.Amabiliidae      | Amabiliidae      | -0.9311708 | -0.5273938 | -0.1122495 |
| traitdd\_def\_host.parasite\_family.Filaroididae     | Filaroididae     | -1.0131866 | -0.5096268 | -0.0238753 |
| traitdd\_def\_host.parasite\_family.Capillariidae    | Capillariidae    | -0.9504257 | -0.4292553 |  0.0424987 |
| traitdd\_def\_host.parasite\_family.Echinobothriidae | Echinobothriidae | -0.9106126 | -0.4203768 |  0.1193498 |
| traitdd\_def\_host.parasite\_family.Cystidicolidae   | Cystidicolidae   | -0.7094874 | -0.4195596 | -0.1193317 |
| traitdd\_def\_host.parasite\_family.Hymenolepididae  | Hymenolepididae  | -0.7158104 | -0.4082113 | -0.1102936 |
| traitdd\_def\_host.parasite\_family.Rhabdochonidae   | Rhabdochonidae   | -0.6618348 | -0.4003792 | -0.1491364 |
| traitdd\_def\_host.parasite\_family.Echinorhynchidae | Echinorhynchidae | -0.7802291 | -0.3941904 | -0.0007311 |
| traitdd\_def\_host.parasite\_family.Crenosomatidae   | Crenosomatidae   | -0.8176908 | -0.3648025 |  0.0431816 |

</div>

Let’s combine adult growth/development into a single metric. We
standardize the random effects for adult growth and development, then we
average them. Positive values are families that grew more/longer than
expected. Here are those families:

<div class="kable-table">

|                                                       | fam               |    re\_lwr |       re |   re\_upr |    t1\_lwr |         t1 |   t1\_upr |    t2\_lwr |       t2 |  t2\_upr |
|:------------------------------------------------------|:------------------|-----------:|---------:|----------:|-----------:|-----------:|----------:|-----------:|---------:|---------:|
| traitdd\_def\_host.parasite\_family.Philometridae     | Philometridae     |  4.7996698 | 7.172398 |  9.890518 |  0.1848023 |  0.5004886 | 0.8178478 |  3.7179925 | 5.520221 | 7.187329 |
| traitdd\_def\_host.parasite\_family.Strongylidae      | Strongylidae      |  2.9652072 | 7.015274 | 11.060323 |  0.7762370 |  1.3515080 | 1.9800585 |  1.3507620 | 4.517640 | 7.708411 |
| traitdd\_def\_host.parasite\_family.Dracunculidae     | Dracunculidae     |  3.6739802 | 6.602155 |  9.736704 |  0.2716049 |  0.6765590 | 1.1158293 |  2.5492587 | 4.848464 | 7.170719 |
| traitdd\_def\_host.parasite\_family.Anoplocephalidae  | Anoplocephalidae  |  4.1108757 | 6.320353 |  8.710248 |  0.3404113 |  0.6675059 | 0.9962387 |  2.9414835 | 4.590363 | 6.160978 |
| traitdd\_def\_host.parasite\_family.Diplotriaenidae   | Diplotriaenidae   |  1.6996467 | 3.780804 |  5.940548 |  0.2874070 |  0.5871114 | 0.8938272 |  0.9512895 | 2.573244 | 4.150519 |
| traitdd\_def\_host.parasite\_family.Bothriocephalidae | Bothriocephalidae |  0.1834969 | 3.509511 |  6.890408 | -0.2323565 |  0.3088728 | 0.8975128 |  0.1229513 | 2.631345 | 5.171433 |
| traitdd\_def\_host.parasite\_family.Proteocephalidae  | Proteocephalidae  | -0.4894315 | 2.669188 |  5.479186 | -0.2343612 |  0.2952591 | 0.8453365 | -0.5254294 | 1.895163 | 4.059917 |
| traitdd\_def\_host.parasite\_family.Micropleuridae    | Micropleuridae    | -1.2376833 | 2.579935 |  6.678378 | -0.5763670 | -0.0101814 | 0.5524892 | -0.7614129 | 2.212303 | 5.151429 |
| traitdd\_def\_host.parasite\_family.Linstowiidae      | Linstowiidae      | -0.8573859 | 2.474044 |  5.665775 | -0.3623550 |  0.1555682 | 0.6912757 | -0.5491361 | 1.912210 | 4.446810 |
| traitdd\_def\_host.parasite\_family.Cystoopsidae      | Cystoopsidae      | -1.6092077 | 2.435698 |  6.536485 | -0.9607383 | -0.3241321 | 0.3103160 | -0.6844500 | 2.369390 | 5.385679 |

</div>

And here are the families that grew less than expected as adults:

<div class="kable-table">

|                                                         | fam                 |   re\_lwr |        re |    re\_upr |    t1\_lwr |         t1 |    t1\_upr |   t2\_lwr |        t2 |    t2\_upr |
|:--------------------------------------------------------|:--------------------|----------:|----------:|-----------:|-----------:|-----------:|-----------:|----------:|----------:|-----------:|
| traitdd\_def\_host.parasite\_family.Cystidicolidae      | Cystidicolidae      | -6.715455 | -4.320058 | -2.2799391 | -0.7094874 | -0.4195596 | -0.1193317 | -4.783605 | -3.257260 | -1.6574972 |
| traitdd\_def\_host.parasite\_family.Habronematidae      | Habronematidae      | -6.574394 | -4.150776 | -2.1513902 | -0.6448571 | -0.3602769 | -0.0560702 | -4.905733 | -3.121596 | -1.5715652 |
| traitdd\_def\_host.parasite\_family.Hedruridae          | Hedruridae          | -6.606382 | -3.777496 | -0.8517576 | -0.4128678 | -0.0391356 |  0.3094419 | -5.143625 | -3.087984 | -0.8400945 |
| traitdd\_def\_host.parasite\_family.Schistotaeniidae    | Schistotaeniidae    | -6.333619 | -3.540677 | -0.6426610 | -0.4642065 | -0.0711851 |  0.3277226 | -5.054982 | -2.852750 | -0.6327679 |
| traitdd\_def\_host.parasite\_family.Acrobothriidae      | Acrobothriidae      | -6.775710 | -3.347602 |  0.2522300 | -0.8972231 | -0.3282293 |  0.1959337 | -5.093483 | -2.431409 |  0.4149883 |
| traitdd\_def\_host.parasite\_family.Nematoparataeniidae | Nematoparataeniidae | -6.818772 | -2.862830 |  0.9497216 | -0.8363903 | -0.2965229 |  0.3517961 | -5.108948 | -2.112567 |  0.7282008 |
| traitdd\_def\_host.parasite\_family.Illiosentidae       | Illiosentidae       | -6.131931 | -2.809016 |  0.2146915 | -0.5272391 | -0.0640530 |  0.3943975 | -4.816911 | -2.244836 |  0.0515639 |
| traitdd\_def\_host.parasite\_family.Echinobothriidae    | Echinobothriidae    | -5.906561 | -2.795205 |  0.2578491 | -0.9106126 | -0.4203768 |  0.1193498 | -4.332267 | -1.866643 |  0.4955580 |
| traitdd\_def\_host.parasite\_family.Thelaziidae         | Thelaziidae         | -5.803362 | -2.714354 |  0.5221728 | -0.4973896 | -0.0479974 |  0.4189850 | -4.466551 | -2.214257 |  0.2191891 |
| traitdd\_def\_host.parasite\_family.Dioctophymidae      | Dioctophymidae      | -7.139260 | -2.624710 |  1.7077787 | -0.9811394 | -0.2431763 |  0.4848869 | -5.381888 | -1.996044 |  1.4506560 |

</div>

These also tend to be the families that attain larger sizes and ages at
maturity. Here are the families that are older/larger adults, relative
to expectations:

<div class="kable-table">

|                                                       | fam               |    re\_lwr |       re |  re\_upr |    t1\_lwr |        t1 |   t1\_upr |    t2\_lwr |       t2 |  t2\_upr |
|:------------------------------------------------------|:------------------|-----------:|---------:|---------:|-----------:|----------:|----------:|-----------:|---------:|---------:|
| traitag\_def\_host.parasite\_family.Ophidascaridae    | Ophidascaridae    |  3.1803282 | 5.459599 | 7.960514 |  0.3814511 | 0.7111565 | 1.0563255 |  1.9210855 | 3.500108 | 5.243773 |
| traitag\_def\_host.parasite\_family.Taeniidae         | Taeniidae         |  2.8390097 | 5.289559 | 7.713742 |  0.4763005 | 0.8483626 | 1.1996870 |  1.5694380 | 3.266591 | 4.876741 |
| traitag\_def\_host.parasite\_family.Strongylidae      | Strongylidae      |  1.6352762 | 5.022248 | 8.688091 |  0.7822766 | 1.2900318 | 1.8292890 |  0.1614887 | 2.609035 | 5.291690 |
| traitag\_def\_host.parasite\_family.Anoplocephalidae  | Anoplocephalidae  |  2.1687973 | 4.149077 | 6.094719 |  0.3780173 | 0.6644179 | 0.9362608 |  1.2302967 | 2.560776 | 3.814234 |
| traitag\_def\_host.parasite\_family.Dracunculidae     | Dracunculidae     |  0.6034453 | 3.253577 | 6.021083 |  0.1954768 | 0.5586805 | 0.9430807 |  0.1239858 | 1.955053 | 3.756873 |
| traitag\_def\_host.parasite\_family.Philometridae     | Philometridae     |  1.1255969 | 3.199019 | 5.195594 |  0.1484630 | 0.4155271 | 0.6831205 |  0.6405658 | 2.061426 | 3.465895 |
| traitag\_def\_host.parasite\_family.Ascarididae       | Ascarididae       |  1.0327002 | 3.196169 | 5.474739 | -0.2249850 | 0.0973158 | 0.4113640 |  0.9118620 | 2.408695 | 3.852288 |
| traitag\_def\_host.parasite\_family.Diplotriaenidae   | Diplotriaenidae   |  1.1098405 | 3.073018 | 5.101008 |  0.1871007 | 0.4697537 | 0.7242411 |  0.5516772 | 1.892184 | 3.253822 |
| traitag\_def\_host.parasite\_family.Bothriocephalidae | Bothriocephalidae | -0.2399350 | 2.934709 | 6.074382 | -0.3098349 | 0.1975962 | 0.7307368 | -0.1002458 | 2.077780 | 3.996347 |
| traitag\_def\_host.parasite\_family.Toxocaridae       | Toxocaridae       |  0.5149761 | 2.517765 | 4.953059 | -0.1845541 | 0.1547071 | 0.4743523 |  0.3923986 | 1.808234 | 3.386809 |

</div>

And here are the families that mature as small/young adults:

<div class="kable-table">

|                                                         | fam                 |   re\_lwr |        re |    re\_upr |    t1\_lwr |         t1 |    t1\_upr |   t2\_lwr |        t2 |    t2\_upr |
|:--------------------------------------------------------|:--------------------|----------:|----------:|-----------:|-----------:|-----------:|-----------:|----------:|----------:|-----------:|
| traitag\_def\_host.parasite\_family.Amabiliidae         | Amabiliidae         | -6.020415 | -3.663578 | -1.1762086 | -0.7388265 | -0.3860901 | -0.0284551 | -4.048135 | -2.474254 | -0.7945405 |
| traitag\_def\_host.parasite\_family.Progynotaeniidae    | Progynotaeniidae    | -7.465008 | -3.602305 | -0.1840704 | -0.6581640 | -0.2219620 |  0.2402790 | -5.060006 | -2.559689 | -0.1545810 |
| traitag\_def\_host.parasite\_family.Rhabdochonidae      | Rhabdochonidae      | -5.315584 | -3.480622 | -1.8376006 | -0.6146386 | -0.3812169 | -0.1312234 | -3.399929 | -2.321707 | -1.2090232 |
| traitag\_def\_host.parasite\_family.Capillariidae       | Capillariidae       | -6.148606 | -3.423567 | -0.3963070 | -0.9031176 | -0.4224691 |  0.0228801 | -4.154220 | -2.231956 | -0.1617124 |
| traitag\_def\_host.parasite\_family.Filaroididae        | Filaroididae        | -6.544907 | -3.353749 | -0.2345463 | -0.8171429 | -0.3724103 |  0.0387465 | -4.462446 | -2.221349 | -0.0305620 |
| traitag\_def\_host.parasite\_family.Echinobothriidae    | Echinobothriidae    | -6.294380 | -3.350347 | -0.2155656 | -0.8506567 | -0.3392651 |  0.1724120 | -4.175385 | -2.247961 | -0.0871988 |
| traitag\_def\_host.parasite\_family.Acuariidae          | Acuariidae          | -4.967966 | -3.136692 | -1.3432263 | -0.5761232 | -0.3121313 | -0.0758999 | -3.276969 | -2.087489 | -0.8699261 |
| traitag\_def\_host.parasite\_family.Nematoparataeniidae | Nematoparataeniidae | -6.699049 | -3.117267 |  0.4839123 | -0.7982991 | -0.2508341 |  0.3797609 | -4.624070 | -2.138642 |  0.3126299 |
| traitag\_def\_host.parasite\_family.Camallanidae        | Camallanidae        | -5.025157 | -2.898284 | -0.7933708 | -0.5294820 | -0.2524523 |  0.0317247 | -3.391154 | -1.992924 | -0.5533954 |
| traitag\_def\_host.parasite\_family.Nippotaeniidae      | Nippotaeniidae      | -6.627243 | -2.847880 |  1.0468621 | -0.8866563 | -0.2903264 |  0.3347961 | -4.480067 | -1.908303 |  0.7446944 |

</div>

Now let’s plot the covariance matrices. Above we plotted trait
covariance without taxonomic effects - the species that grew more or
less than expected from just the fixed effects (marginal residuals).
Now, we divide this covariance by taxonomic levels.

The taxonomic covariances estimated by the model can be better
understood by plotting *conditional* residuals. In other, words, we take
the residuals accounting for fixed effects (host mass etc.) and
taxonomy. The conditional residuals represent high (or low) growth,
given host mass and taxonomy. Since we fit nested models (i.e. first
order, then add family, then add genus), we can look at conditional
residuals after controlling for higher level taxonomy. For instance, the
conditional residuals at the family level represent families that grow
more (or less) than expected given fixed effects like host mass but also
relative to the mean growth for their order.

### Correlations within stages

Let’s look at the correlations using conditional residuals, starting
within stages. The positive correlation between growth and developmental
time within stages is driven by family-level covariation in both
intermediate and definitive hosts. However, for adult parasites, there
is also a stronger genus-level correlation, because adult life history
varied more at the genus-level than larval life history.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-188-1.png)<!-- -->
Since “order” explained little variance for any trait, and since there
is little covariance left at the “species/residual” level after
accounting for higher taxonomy, let’s remove those panels. We’ll also
separate the raw, uncorrected correlation out to show how it is reduced
by accounting for host masses and taxonomy. The correlation between
larval growth and development is caused by host masses more than adult
growth and development. Even after accounting for host masses, though,
some taxa, mainly families, grow more and longer than expected.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-189-1.png)<!-- -->

Let’s also plot which families drive the relationships. Here are the
estimated random effects for the families with long/short larval growth
and development.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-191-1.png)<!-- -->

And here are the families that grew long/short as adults.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-192-1.png)<!-- -->

The relationship between size and age at maturity is clearest across
families and genera.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-193-1.png)<!-- -->
The relationship between size and age at maturity is also not clearly
removed by controlling host mass. Rather, it is strengthened. Also, some
taxa are just bigger/older than others.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-194-1.png)<!-- -->

Here are the families driving the size-age relationship:

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-195-1.png)<!-- -->
At the family level, a 10% increase in age at maturity was associated
with a 20% increase in reproductive size.

    ## 
    ## Iterations = 1:99901
    ## Thinning interval = 100 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##       0.288598       0.072228       0.002284       0.002149 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.1542 0.2400 0.2874 0.3322 0.4320

The slope is basically the same among species after accounting for fixed
effects, though the CI is smaller.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.2114753      0.0253260      0.0008009      0.0021201 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##   2.5%    25%    50%    75%  97.5% 
    ## 0.1617 0.1945 0.2129 0.2286 0.2581

### Correlations across stages

Now let’s make the same plots across stages.

#### Larval growth vs adult traits

We start by looking at the relationship between larval and adult growth.
Larval and adult growth were negatively correlated and this relationship
was seen at the family, genus, and species level. The correlation
weakened after we accounted for host traits, suggesting some of the
overall correlation was driven by host traits. If a e.g. 100% increase
in larval growth results in a 50% decrease in adult growth, then the
slope of the correlation should be -1. The dotted diagonal line has this
slope. The observed correlation is flatter than this until we account
for higher taxonomy. Once we account for class and order, then we see
close adherence to the line. Thus, species or genera that increase
growth by X%, relative to expectations, tend to see a corresponding
decrease in adult growth.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-198-1.png)<!-- -->

For each of these panels, we can look at the slope and its CI in each
panel (the slope is calculated as the larval-adult covariance divided by
the variance in larval growth; cov(x,y)/var(x) ). The overall slope
(i.e. for the black ellipse) was greater than -1, suggesting that
species with more larval growth also had less than proportionate
decreases in adult growth:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##     -0.6488916      0.0303821      0.0009608      0.0013990 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## -0.7111 -0.6688 -0.6483 -0.6289 -0.5911

It was a bit lower, but still greater than -1 after we accounted for
host traits:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      -0.659446       0.040371       0.001277       0.002429 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## -0.7403 -0.6861 -0.6608 -0.6318 -0.5827

With this slope, a doubling of larval growth was not quite associated
with a corresponding 50% decrease in adult growth.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##     -0.3666310      0.0177173      0.0005603      0.0010682 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## -0.4014 -0.3785 -0.3675 -0.3546 -0.3323

It got much closer to -1 after accounting for class and order. Here is
the slope at the family level:

    ## 
    ## Iterations = 1:99901
    ## Thinning interval = 100 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##       -0.71354        0.12300        0.00389        0.00389 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## -0.9535 -0.7961 -0.7078 -0.6282 -0.4709

At the genus level:

    ## 
    ## Iterations = 1:99901
    ## Thinning interval = 100 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      -0.884698       0.147151       0.004653       0.004653 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## -1.1828 -0.9830 -0.8850 -0.7873 -0.5977

And within genera (among species):

    ## 
    ## Iterations = 1:99901
    ## Thinning interval = 100 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      -0.731680       0.061081       0.001932       0.001932 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## -0.8471 -0.7738 -0.7344 -0.6876 -0.6143

We can also plot the families that tended to grow more/less at both life
stages.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-205-1.png)<!-- -->

Moving on to the relationship between larval growth and adult
development (prepatent period). More larval growth tended to reduce
adult prepatent period, but this was mainly observed among genera not
families. There is thus a mismatch in the levels at which these traits
vary: larval growth varies mostly among families. By contrast, adult
development varies more among genera.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-206-1.png)<!-- -->

Because adult growth decreased more with larval growth than adult
development, there was a tendency for adult growth *rates* to be slower
for species/taxa that grew more as larvae. As explored above, this trend
is somewhat related to slowing growth rates with larger sizes.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-207-1.png)<!-- -->

Here are the Pearson correlations associated with the plot above.

<div class="kable-table">

| level   |    cor.lwr |        cor |    cor.upr | pval |
|:--------|-----------:|-----------:|-----------:|-----:|
| raw     | -0.4105558 | -0.3415633 | -0.2686822 |    0 |
| fixed   | -0.5615704 | -0.5040387 | -0.4416569 |    0 |
| order   | -0.8659818 | -0.7109412 | -0.4312125 |    0 |
| family  | -0.6098393 | -0.4570148 | -0.2714212 |    0 |
| genus   | -0.4172737 | -0.3120677 | -0.1986077 |    0 |
| species | -0.5775993 | -0.5215265 | -0.4605554 |    0 |

</div>

Now let’s examine how larval growth affects size at maturity. Worms that
grow more as larvae do not achieve larger-than-expected adult sizes.
This seems to be true across taxonomic stages.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-209-1.png)<!-- -->

Finally, there was very little relationship between larval growth and
age at maturity. Growing more (or less) than expected is not associated
with later (or earlier) reproductive ages.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-211-1.png)<!-- -->

#### Larval development vs adult traits

Now we move on from larval growth to larval developmental times. We
start by examining how larval development affects adult growth. Species
that develop longer tended to grow less as adults. However, this
relationship disappeared after accounting for fixed effects. Families,
genera, and species tended to grow less as adults when they developed
longer, but the patterns were not significant.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-212-1.png)<!-- -->

If spending more time in the intermediate host reduces the time needed
in the definitive host, then developmental times in the two hosts should
be negatively correlated, especially after accounting for fixed effects.
However, spending more time in the intermediate hosts was associated
with spending more time in the definitive hosts, suggesting that
developmental rates are species traits. Perhaps they are better
considered family traits, since the positive correlation was clearest at
the level.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-213-1.png)<!-- -->

After accounting for fixed effects, here is how much a 10% increase in
larval developmental time increases adult developmental time:

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.0201956      0.0057637      0.0001823      0.0004533 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##     2.5%      25%      50%      75%    97.5% 
    ## 0.009509 0.016198 0.020185 0.023907 0.031825

The family level correlation was similar in magnitude, though with much
more uncertainty.

    ## 
    ## Iterations = 1:99901
    ## Thinning interval = 100 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.0079909      0.0136019      0.0004301      0.0004097 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##      2.5%       25%       50%       75%     97.5% 
    ## -0.017772 -0.001087  0.007608  0.017222  0.034655

Here are the parasite families characterized by longer (or shorter)
development than expected at both stages.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-216-1.png)<!-- -->

We can also put the slow developers (both stages) in a table:

<div class="kable-table">

| fam               |   n |    re\_lwr |        re |  re\_upr |
|:------------------|----:|-----------:|----------:|---------:|
| Taeniidae         |  24 |  1.1593493 | 1.8427517 | 2.589933 |
| Ophidascaridae    |   7 |  1.1148066 | 1.7477533 | 2.420878 |
| Anoplocephalidae  |  30 |  0.8202955 | 1.3423125 | 1.891066 |
| Gnathostomatidae  |   4 |  0.1913455 | 0.8762242 | 1.569585 |
| Protostrongylidae |  26 |  0.1415009 | 0.8009509 | 1.400273 |
| Hedruridae        |   4 |  0.1794062 | 0.7715601 | 1.392146 |
| Hartertiidae      |   2 | -0.0293733 | 0.7414397 | 1.495735 |
| Anisakidae        |   2 | -0.2229771 | 0.6364197 | 1.430930 |
| Physalopteridae   |  11 |  0.1356968 | 0.6159019 | 1.081457 |
| Amphilinidae      |   2 | -0.4921206 | 0.5381963 | 1.520977 |

</div>

And here are the fast developers:

<div class="kable-table">

| fam               |   n |   re\_lwr |         re |    re\_upr |
|:------------------|----:|----------:|-----------:|-----------:|
| Syngamidae        |   3 | -2.562639 | -1.7758907 | -1.0368071 |
| Heterakidae       |   2 | -2.040155 | -1.2660374 | -0.4152418 |
| Hymenolepididae   |  93 | -1.570048 | -1.0528880 | -0.5159980 |
| Amabiliidae       |   4 | -1.461708 | -0.8284546 | -0.1928643 |
| Onchobothriidae   |   2 | -1.520489 | -0.6966574 |  0.2739372 |
| Serendipidae      |   1 | -1.688346 | -0.6531020 |  0.3292220 |
| Crenosomatidae    |   3 | -1.339516 | -0.6371628 |  0.0769265 |
| Raphidascarididae |   3 | -1.281565 | -0.5937500 |  0.1282907 |
| Seuratidae        |   3 | -1.269439 | -0.5932991 |  0.1315935 |
| Rhabdochonidae    |  16 | -1.046883 | -0.5791137 | -0.1375380 |

</div>

Since slow larval development was associated with slow adult development
and only marginally less growth, there was a tendency for adult growth
rates to decrease with larval development at most taxonomic levels.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-219-1.png)<!-- -->
Here are the Pearson correlations associated with the plot above:

<div class="kable-table">

| level   |    cor.lwr |        cor |    cor.upr |  pval |
|:--------|-----------:|-----------:|-----------:|------:|
| raw     | -0.3980571 | -0.3282983 | -0.2547646 | 0.000 |
| fixed   | -0.6011744 | -0.5473332 | -0.4885452 | 0.000 |
| order   | -0.7235381 | -0.4520960 | -0.0595618 | 0.027 |
| family  | -0.5284939 | -0.3565423 | -0.1564885 | 0.001 |
| genus   | -0.4067262 | -0.3005557 | -0.1863745 | 0.000 |
| species | -0.2862807 | -0.2108798 | -0.1328831 | 0.000 |

</div>

Despite the slower adult growth rates, parasites with slow larval (and
adult) development tended to mature at larger adult sizes. The trend was
clearest among families.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-221-1.png)<!-- -->

A 10% increase in larval developmental time, beyond expectations from
host traits, was associated with a 12% increase in maturation size.

    ## 
    ## Iterations = 1:49951
    ## Thinning interval = 50 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##      0.0596361      0.0182400      0.0005768      0.0009704 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##    2.5%     25%     50%     75%   97.5% 
    ## 0.02531 0.04791 0.05941 0.07213 0.09526

The family level correlation was similar in magnitude, though with much
more uncertainty.

    ## 
    ## Iterations = 1:99901
    ## Thinning interval = 100 
    ## Number of chains = 1 
    ## Sample size per chain = 1000 
    ## 
    ## 1. Empirical mean and standard deviation for each variable,
    ##    plus standard error of the mean:
    ## 
    ##           Mean             SD       Naive SE Time-series SE 
    ##       0.064825       0.062992       0.001992       0.001887 
    ## 
    ## 2. Quantiles for each variable:
    ## 
    ##     2.5%      25%      50%      75%    97.5% 
    ## -0.05486  0.02151  0.06045  0.10504  0.19975

Here are the families characterized by long larval development and large
reproductive sizes (or vice versa).

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-224-1.png)<!-- -->
Here are the slow-larvae, large-adult families in a table:

<div class="kable-table">

| fam               |   n |    re\_lwr |       re |  re\_upr |
|:------------------|----:|-----------:|---------:|---------:|
| Ophidascaridae    |   7 |  2.9078899 | 4.755618 | 6.853073 |
| Taeniidae         |  24 |  2.4636711 | 4.434453 | 6.406838 |
| Anoplocephalidae  |  30 |  1.7881741 | 3.303982 | 4.888800 |
| Ascarididae       |  10 |  1.1164196 | 2.853548 | 4.595631 |
| Hartertiidae      |   2 | -0.2338027 | 2.065371 | 4.239389 |
| Gnathostomatidae  |   4 | -0.1402646 | 2.026912 | 4.158728 |
| Toxocaridae       |   6 |  0.4127962 | 2.019003 | 3.923910 |
| Philometridae     |  14 |  0.3537725 | 1.956487 | 3.634940 |
| Cystoopsidae      |   1 | -1.2068618 | 1.887984 | 4.921288 |
| Bothriocephalidae |   7 | -0.7046300 | 1.882639 | 4.484045 |

</div>

Here are the fast-larvae, small-adult families in a table:

<div class="kable-table">

| fam                 |   n |   re\_lwr |        re |    re\_upr |
|:--------------------|----:|----------:|----------:|-----------:|
| Progynotaeniidae    |   1 | -5.851423 | -2.960041 | -0.3149372 |
| Amabiliidae         |   4 | -4.789139 | -2.829088 | -0.9352179 |
| Heterakidae         |   2 | -5.068318 | -2.700003 | -0.3019403 |
| Rhabdochonidae      |  16 | -4.034646 | -2.588950 | -1.2512012 |
| Trichosomoididae    |   1 | -5.714495 | -2.434243 |  0.7201907 |
| Echinobothriidae    |   6 | -4.911406 | -2.424171 |  0.2093798 |
| Capillariidae       |  15 | -4.643567 | -2.395714 |  0.0192219 |
| Acuariidae          |  13 | -3.896805 | -2.380897 | -1.0186164 |
| Seuratidae          |   3 | -4.446683 | -2.361750 | -0.3638995 |
| Nematoparataeniidae |   2 | -5.379814 | -2.269416 |  0.7739174 |

</div>

Longer larval development increased age at maturity, as expected.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-228-1.png)<!-- -->

#### Growth rates in the two hosts

They were uncorrelated across hosts.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-229-1.png)<!-- -->

Since growth rates were not explicitly modeled, there was not covariance
returned by the model. Thus, here are the pearson correlations for the
plot above.

<div class="kable-table">

| level   |    cor.lwr |        cor |    cor.upr |      pval |
|:--------|-----------:|-----------:|-----------:|----------:|
| raw     | -0.0034591 |  0.0768076 |  0.1560910 | 0.0607207 |
| fixed   | -0.0200022 |  0.0603401 |  0.1399080 | 0.1408655 |
| order   | -0.6497873 | -0.3339179 |  0.0802946 | 0.1107813 |
| family  | -0.3183621 | -0.1141891 |  0.1001082 | 0.2951550 |
| genus   | -0.1123824 |  0.0086925 |  0.1295130 | 0.8884235 |
| species | -0.2289565 | -0.1514945 | -0.0721260 | 0.0002030 |

</div>

#### Size and age at maturity - determined by larval or adult traits?

Larvae that grew more did not have larger adult sizes or younger ages,
although genera that grew relatively large had shorter prepatent
periods. Species that have longer larval development have older age at
maturity. This trend was mostly due to variation within genera. Families
that developed longer as larvae tended to be larger adults, but only
weakly.

Here are the plots of adult growth and development vs size and age at
maturity.

Species that grew more as adults tended to have bigger maturation sizes
at the family, genus, and species levels. Age at maturity was also
correlated with adult growth, but not within genera.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-233-1.png)<!-- -->
Size and age at maturity also increased with adult development, but not
within genera for development.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-234-1.png)<!-- -->

Rapid adult growth is associated with a younger age at maturity but not
a larger size at maturity.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-235-1.png)<!-- -->
Slow larval growth, though, tends to be associated with larger sizes and
older ages at maturity.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-236-1.png)<!-- -->

Since parasites grow more and longer as adults, it is not surprising
that size and age at maturity is primarily determined by adult
strategies.

Since correlations among orders, among genera, and within-genera usually
did not diverge from family-level correlations, let’s simplify the
plots. Also, we can pick out a couple families to show how they achieved
large sizes - through more growth or faster growth, and at what stage?

On this plot 4 families with different growth strategies are
highlighted: 1) Anoplocephalidae (more adult growth than expected, also
relative to larval size), 2) Taeniidae (more larval growth than
expected, and proprtionally more adult growth), 3) Acuariidae (a little
less growth than expected in both hosts), 4) Cystidicolidae (more larval
growth than expected, but much less adult growth).

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-240-1.png)<!-- -->
These differences are reflected in developmental times. Longer
development is associated with proportionally more growth.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-241-1.png)<!-- -->
If we look at the growth rates of these families, we see that they are
not consistently faster or slower than expected. Thus, their position on
the size-age continuum is mainly due to variation in developmental time,
not growth rate.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-242-1.png)<!-- -->

Overall, these patterns result in a continuum of size-age at maturity.
![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-243-1.png)<!-- -->

Instead of plotting species values and family average, we can also plot
the family-level random effects from the mixed model.

Here is how random effects for development look. Some families with long
larval development also have long adult development.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-245-1.png)<!-- -->

Here are the random effects for growth showing which families grow a bit
more as larvae and adults than expected.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-246-1.png)<!-- -->

Combining growth and development, we see which parasite families are
characterized by large sizes and long lives.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-247-1.png)<!-- -->

Maybe forest plots might be a better way to show this. This way the CIs
can also be shown.

![](life_history_stragies_rg_imp_files/figure-gfm/unnamed-chunk-253-1.png)<!-- -->

# Conclusions

Some changes in life history are consistent with theoretical
expectations. Others are not. Overperformance as larvae is not
associated with over or under-performance as adults, suggestive of
decoupling.
