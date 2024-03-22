---
layout: post
title: New Paper - Joint Selection
categories: DifferentialPrivacy NewPaper
---

I have a new paper out with my colleagues from UMass Amherst: [Joint Selection: Adaptively Incorporating Public Information for Private Synthetic Data](https://arxiv.org/abs/2403.07797). Many data sources that researchers and policy makers are interested are updated through periodic releases ranging from large-scale surveys such as the [Current Population Survey (CPS)](https://www.census.gov/programs-surveys/cps.html) to governmental administrative records. Since these datasets often contain sensitive information, it may be the case that only aggregate statistics are released or, alternatively, a synthetic dataset is constructed and released (either hopefully under differential privacy). We introduce a new method `JAM-PGM` to utilize public data to improve the quality of synthetic data generated under differential privacy. In the case of periodically released datasets, public data could include prior releases. In the paper, we look at cases where the public and private data do not follow the same distribution, which is what one would expect if using such techniques in the wild.

Abstract:
> Mechanisms for generating differentially private synthetic data based on marginals and graphical models have been successful in a wide range of settings. However, one limitation of these methods is their inability to incorporate public data. Initializing a data generating model by pre-training on public data has shown to improve the quality of synthetic data, but this technique is not applicable when model structure is not determined a priori. We develop the mechanism JAM-PGM, which expands the adaptive measurements framework to jointly select between measuring public data and private data. This technique allows for public data to be included in a graphical-model-based mechanism. We show that JAM-PGM is able to outperform both publicly assisted and non publicly assisted synthetic data generation mechanisms even when the public data distribution is biased.

The preprint is available [here](https://arxiv.org/abs/2403.07797). This paper will appear at [AISTATS 2024](https://aistats.org/aistats2024/).

<figure style="display: block; margin-left: auto; margin-right: auto; width: 50%">
  <img src="https://media.nga.gov/iiif/ed0b70d3-a43b-4a00-89ac-657b7e396689/full/!440,400/0/default.jpg">
  <figcaption style="text-align: center"><a href="https://www.nga.gov/collection/art-object-page.52624.html">The Seine (1902) by Henry Ossawa Tanner</a></figcaption>
</figure>
