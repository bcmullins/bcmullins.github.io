---
layout: post
title: New Paper - Private Adaptive Covariance Estimation via Gaussian Graphical Models
categories: DifferentialPrivacy NewPaper
---

I have a [new paper](https://arxiv.org/abs/2605.24295) out with my colleagues from UMass Amherst, which studies the problem of differentially private covariance estimation for continuous data. While many existing private covariance methods measure the full covariance matrix, we propose an iterative and adaptive method focusing on allocating the privacy budget to the most informative entries. The tricky part is that the resulting partial, noisy matrix is not necessarily a valid covariance matrix, i.e., is not PSD in general (or usually). We introduce an optimization routine to reconstruct the maximum entropy covariance matrix from the measured entries. This paper contains a lot of interesting optimization ideas for working with covariance matrices under differential privacy!

Abstract:
>We propose PACE-GGM, a data-adaptive differentially private method for covariance estimation that concentrates its privacy budget on the most informative entries of the empirical covariance matrix, rather than perturbing all entries. This applies in the natural setting where the modeler supplies separate bounds for each variable, so that individual entries can be measured with less noise than the full matrix. In each round, our method selects a poorly approximated entry, measures it using the Gaussian mechanism, and then reconstructs a full covariance matrix using a maximum-entropy reconstruction objective, leading to a Gaussian graphical model structure. Experiments on diverse real-world datasets demonstrate consistent improvements in estimation error with respect to the Gaussian mechanism and other baselines, particularly in high-dimensional and low-to-moderate privacy regimes. 


The preprint is available on [arXiv](https://arxiv.org/abs/2605.24295). 

<figure style="display: block; margin-left: auto; margin-right: auto; width: 50%">
  <img src="/images/blog/fast-adaptive-private-queries/wunderwald.jpeg">
  <figcaption style="text-align: center">Die Fabrik von Loewe & Co (1926) by <a href="https://en.wikipedia.org/wiki/Gustav_Wunderwald">Gustav Wunderwald</a></figcaption>
</figure>