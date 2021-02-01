---
layout: post
title: Introducing mobilityIndexR
categories: IncomeMobility
mathjax: true
---

**mobilityIndexR** is an R package for calculating transition matrices and indices to measure mobility within a sample. For instance, tracking the income of a cohort over some period of time allows one to measure the [economic mobility](https://en.wikipedia.org/wiki/Economic_mobility) of that cohort, and tracking the grades of students in a class allows one to measure grade mobility. This post is an invitation to the package and an introduction to the ideas it implements. For a general introduction to economic mobility, see [Further Reading](#further-reading) at the bottom of the post.

You can find the latest release of mobilityIndexR on [CRAN](https://cran.r-project.org/web/packages/mobilityIndexR/index.html) and the development version on [Github](https://github.com/bcmullins/mobilityIndexR).

## What is a transition matrix?

An (unconditional) _transition matrix_ is a table of estimated probabilities or proportions summarizing change in qualitative states between two points in time. A simple example is with the weather from one day to next where the qualitative states are sunny, cloudy, and precipitation. The entry in this transition matrix (sunny, cloudy) is the proportion of observations that were sunny on the first day and cloudy on the second. One may interpret this as the estimated unconditional probability that a sunny day occurs followed by a cloudy day. The more traditional conditional transition matrix can be obtained by normalizing each row in the unconditional matrix by its sum.

<img style="display:block; margin-left: auto; margin-right: auto;" width="50%" height="70%" src="/images/blog/mobilityIndexR/transitionMatrix.png">

Quantitative values of interest such as income or numerical grade must be discretized before constructing a transition matrix. Typically, the value of interest is binned into ranks and these ranks are treated as qualitative states. Types of transition matrices are differentiated by the method of binning used. A _relative transition matrix_ bins values into ranks as quantiles at each point in time. For income mobility research, quintiles and deciles are typically used and these matrices are referred to as dollar-relative. Note that the bounds defining the ranks in a relative transition matrix depend on the distribution of values of interest both points in time.

In contrast, an _absolute transition matrix_ bins values into ranks at each point in time according to an rule independent of the data. This is a natural fit for numerical grades which already have a well defined mapping into qualitative states: letter grades. A third type - a _mixed transition matrix_ - bins the value of interest into quantile ranks at the first point in time and uses the bounds defining these quantiles ranks to bin the value of interest at the second point in time. Notice that the ranks in a mixed transition matrix depend only on the distribution of the value of interest at the first point in time. As with relative matrices, quintiles and deciles are both common in income mobility research, and these matrices are referred to as dollar-absolute.

We implement these three types of transition matrices in **mobilityIndexR** through the `getTMatrix` function. In the examples below, we use the included dataset `incomeMobility`.

{% highlight r %}
# Relative Transition Matrix with Quintiles
getTMatrix(dat = incomeMobility, col_x = "t0", col_y = "t5",
           type = "relative", num_ranks = 5, probs = TRUE)
#> $tmatrix
#>    
#>         1     2     3     4     5
#>   1 0.152 0.040 0.008 0.000 0.000
#>   2 0.048 0.080 0.048 0.024 0.000
#>   3 0.000 0.048 0.064 0.056 0.032
#>   4 0.000 0.008 0.024 0.120 0.048
#>   5 0.000 0.024 0.056 0.000 0.120
#>
#> $col_x_bounds
#>      0%     20%     40%     60%     80%    100%
#>   462.0 21543.4 42469.8 64061.6 77888.4 99557.0
#>
#> $col_y_bounds
#>          0%         20%         40%         60%         80%        100%
#>    340.2705  18204.9969  39710.3062  58494.6271  78178.6713 262909.3195
{% endhighlight %}

The `getTMatrix` function returns a matrix object and two lists containing the bounds used to bin the values into ranks. The type of transition matrix returned is determined by the `type` argument. Additionally, setting `probs = FALSE` produces the contingency table underlying the transition matrix. For the other types of transition matrices and special cases, see our [introductory vignette](https://cran.r-project.org/web/packages/mobilityIndexR/vignettes/intro-to-mobilityIndexR.html).

## What are mobility indices?

While it is possible to glean information from the transition matrix itself, these objects are often too large and unwieldy for one to assess the mobility of a sample. A _mobility index_ solves this information overload by providing a single numeric value (or vector of values) to describe mobility. Unsurprisingly, there is no single index measuring mobility; rather, there exists a variety of indices that capture various facets of mobility.

One well-studied collection of mobility indices are those that can be calculated from just the transition matrix. In **mobilityIndexR**, we implemented four indices of this sort. The _Prais-Bibby index_ is calculated as one minus the trace (or diagonal) of the transition matrix which is the proportion of records that changed rank. This estimates the probability that a record in the sample experiences mobility, since records on the diagonal have the same rank at both points in time. The _Average Movement index_ is the average change in rank between the two points in time.

The _Weighted-Group Mobility (WGM) index_ is a weighted version of the proportion of records that change rank and is a generalization of the Shorrocks (M-hat) index. Finally, the _Origin Specific index_ is a vector-valued index that looks at movement in the top and bottom ranks. This index estimates the probability that a record in the sample moved up from the bottom rank, moved up at least two ranks from the bottom rank, moved down from the top rank, and moved down at least two ranks from the top rank.

Using the `getMobilityIndices` function, **mobilityIndexR** constructs the desired type of transition matrix and calculates the specified indices (all by default).

{% highlight r %}
getMobilityIndices(dat = incomeMobility, col_x = "t0", col_y = "t5",
                   type = "relative", num_ranks = 5)
#> $average_movement
#> [1] 0.64
#>
#> $os_far_bottom
#> [1] 0.04
#>
#> $os_far_top
#> [1] 0.4
#>
#> $os_total_bottom
#> [1] 0.24
#>
#> $os_total_top
#> [1] 0.4
#>
#> $prais_bibby
#> [1] 0.464
#>
#> $wgm
#> [1] 0.58
{% endhighlight %}

Additionally, setting `intervals = TRUE` returns nonparametric bootstrap confidence intervals with a specified interval size and number of bootstrap iterations. See our [introductory vignette](https://cran.r-project.org/web/packages/mobilityIndexR/vignettes/intro-to-mobilityIndexR.html) for more information on using this feature.

## Comparing Mobility

There are several cases where one may want to compare mobility indices between two samples. Consider the following three use cases. Suppose a dataset contains the incomes of individuals over several years; one can compare the mobility experienced by the sample between two time periods, e.g. $t_0$ to $t_3$ and $t_5$ to $t_8$. Alternatively, one may be interested in comparing mobility of income between two subsets of a sample, e.g. men and women, during the same period of time. Regarding grade data, one may be interested in comparing mobility of grades between two sections of a class.

To compare mobility across samples, we provide a function `getHypothesisTest` to calculate nonparametric one-sided hypothesis tests for each index specified. Below, we provide an example using the first case above.

{% highlight r %}
getHypothesisTest(dat_A = incomeMobility, dat_B = incomeMobility,
                  cols_A = c("t0", "t3"), cols_B = c("t5", "t8"),
                  type = "relative", num_ranks = 5, bootstrap_iter = 100)
#> $prais_bibby
#> [1] 0.38
#>
#> $average_movement
#> [1] 0.6
#>
#> $wgm
#> [1] 0.39
#>
#> $os_total_top
#> [1] 0.51
#>
#> $os_far_top
#> [1] 0.92
#>
#> $os_total_bottom
#> [1] 0.32
#>
#> $os_far_bottom
#> [1] 0.03
{% endhighlight %}

## Further Reading

- [Introduction to mobilityIndexR vignette](https://cran.r-project.org/web/packages/mobilityIndexR/vignettes/intro-to-mobilityIndexR.html)
- [Income Mobility](https://www.iza.org/publications/dp/7730/income-mobility) from the [Handbook of Income Distribution](https://www.sciencedirect.com/handbook/handbook-of-income-distribution)
- [Levels and Trends in the Income Mobility of U.S. Families, 1977–2012](https://www.bostonfed.org/publications/research-department-working-paper/2016/levels-and-trends-in-the-income-mobility-of-us-families-1977-2012.aspx)
