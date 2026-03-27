---
layout: post
title: New Paper - Fast Private Adaptive Query Answering for Large Data Domains
categories: DifferentialPrivacy NewPaper
---

I have a new paper out with my colleagues from UMass Amherst and Penn State: [Fast Private Adaptive Query Answering for Large Data Domains](https://arxiv.org/abs/2602.05674). Marginals [are statistics](https://en.wikipedia.org/wiki/Marginal_distribution) that capture low-dimensional structure and correlations among sets of attributes in a dataset and are an important building block for [differentially private](https://en.wikipedia.org/wiki/Differential_privacy) algorithms. In this paper, we focus on answering large workloads of marginals for discrete tabular datasets over large data domains (i.e., many attributes), which is a computational bottleneck for state-of-the-art query answering and synthetic data mechanisms such as [AIM]({{ site.baseurl }}{% link _posts/2022-03-20-aim-synthetic-data.md %}). We introduce a new query answering mechanism called AIM+GReM that integrates our [GReM-MLE]({{ site.baseurl }}{% link _posts/2024-10-04-gremlnn.md %}) (Gaussian Residual-to-Marginals) reconstruction method with AIM, which yields improved scalability and competitive error on large datasets. 

Abstract:
>Privately releasing marginals of a tabular dataset is a foundational problem in differential privacy. However, state-of-the-art mechanisms suffer from a computational bottleneck when marginal estimates are reconstructed from noisy measurements. Recently, residual queries were introduced and shown to lead to highly efficient reconstruction in the batch query answering setting. We introduce new techniques to integrate residual queries into state-of-the-art adaptive mechanisms such as AIM. Our contributions include a novel conceptual framework for residual queries using multi-dimensional arrays, lazy updating strategies, and adaptive optimization of the per-round privacy budget allocation. Together these contributions reduce error, improve speed, and simplify residual query operations. We integrate these innovations into a new mechanism (AIM+GReM), which improves AIM by using fast residual-based reconstruction instead of a graphical model approach. Our mechanism is orders of magnitude faster than the original framework and demonstrates competitive error and greatly improved scalability.


Click [here for the preprint](https://arxiv.org/abs/2602.05674). This paper will appear at AISTATS 2026.

<figure style="display: block; margin-left: auto; margin-right: auto; width: 50%">
  <img src="/images/blog/fast-adaptive-private-queries/wunderwald.jpeg">
  <figcaption style="text-align: center">Die Fabrik von Loewe & Co (1926) by <a href="https://en.wikipedia.org/wiki/Gustav_Wunderwald">Gustav Wunderwald</a></figcaption>
</figure>