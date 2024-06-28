---
layout: page
title: Projects
permalink: /projects/
---

## Differentially Private Synthetic Data

[Synthetic data](https://www.census.gov/about/what/synthetic-data.html) is data that matches the schema and domain of a given dataset as well as some of its statistical properties. This project seeks to advance methods for generating and working with tabular synthetic data under differential privacy. This problem is challenging because satisfying [differential privacy](https://en.wikipedia.org/wiki/Differential_privacy) limits how well the statistical properties of the original dataset are preserved in the synthetic dataset. 

- We [introduced AIM]({{ site.baseurl }}{% link _posts/2022-03-20-aim-synthetic-data.md %}) (VLDB 2022), a mechanism for generating private synthetic data for discrete tabular datasets that's state-of-the-art across several error metrics. 
- We [introduced JAM-PGM]({{ site.baseurl }}{% link _posts/2024-03-21-jam-synthetic-data.md %}) (AISTATS 2024), a private synthetic data mechanism that incorporates public data to reduce error and better utilize the privacy budget.

## Topology and Explainable Machine Learning

<img style="float: right; display: inline-block" width="35%" height="35%"  src="/images/model.png">

Rule-based explanations provide human-interpretable reasons for a classifier's behavior. At the same time, rules are definable regions of the feature space. This project studies connections between the rule-based explanations of classifiers and definability in topology. 

- In Fall 2021, I gave a talk at the [UMass CS Theory Seminar](https://groups.cs.umass.edu/theory/theory-seminar/). 
- In Spring 2023, I presented [a workshop paper]({{ site.baseurl }}{% link _posts/2023-01-24-shape-of-explanations.md %}) developing the cotours of this approach. We prove a result characterizing explainability as a simple topological property similar to the [property of Baire](https://en.wikipedia.org/wiki/Property_of_Baire).

## Utterly Incomplete Look at Research

This project looks at research from years past. I survey a handful of books and articles in a particular year from math, economics, philosophy, international relations, and other interesting topics. 

Current years:
[1823]({{ site.baseurl }}{% link _posts/2023-12-28-research-from-1823.md %}) &#8729;
[1873]({{ site.baseurl }}{% link _posts/2023-11-14-research-from-1873.md %}) &#8729;
[1923]({{ site.baseurl }}{% link _posts/2023-07-21-research-from-1923.md %})

## Infinite Cycles and the Regress Problem

<img style="float: right; display: inline-block" width="25%" height="25%"  src="/images/infinitecycle.png">

This project aims to bring the work of Diestel and collaborators on infinite cycles in graphs to bear on the [program of Atkinson and Peijnenburg]({{ site.baseurl }}{% link _posts/2020-12-29-interesting-research-2010s.md %}#the-graph-theoretic-approach-to-epistemic-justification) in analyzing the justification structure of infinite chains and infinite cycles of reasoning from a probabilistic and epistemological perspective.

I presented a [paper introducing this approach](https://bcmullins.github.io/infinite_cycles/#/) at the [2019 Society for Exact Philosophy conference](http://meta.phil.ufl.edu/host/sep/meeting.html?year=2019). 

# Past Projects

## Earnings Mobility and SNAP Participation in Georgia

This project investigated earnings mobility among [SNAP](https://en.wikipedia.org/wiki/Supplemental_Nutrition_Assistance_Program) participants using linked administrative data from the State of Georgia. Our goal was to better understand the earnings mobility of low-income populations and how participation in government benefits programs affects one's earnings, especially during economic downturns such as the Great Recession.

Results from this project were presented at the [National Tax Association's Annual Conference](https://ntanet.org/event/2014/11/2014-annual-conference-on-taxation/) in 2014, the [Next Generation of Public Finance conference](https://aysps.gsu.edu/files/2016/01/NGPF-Conference-Schedule.pdf) in 2016, the [International Conference on Administrative Data Research](https://ijpds.org/adr2019) in 2019, and [discussed on WABE](https://www.wabe.org/closer-look-stone-mountains-mayor-orlando-and-more/), Atlanta's NPR affiliate, in 2017. [Our findings]({{ site.baseurl }}{% link _posts/2021-10-06-earnings-mobility-great-recession.md %}) were published in [Social Science Quarterly](https://onlinelibrary.wiley.com/doi/abs/10.1111/ssqu.13083), which utilizes an R package we developed called [mobilityIndexR](https://github.com/bcmullins/mobilityIndexR) that can be found on CRAN.

This project was a collaboration with colleagues at the [Fiscal Research Center](https://frc.gsu.edu) at Georgia State University.

___

Updated: 06/24
