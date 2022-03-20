---
layout: post
title: New Paper - AIM&#58; An Adaptive and Iterative Mechanism for Differentially Private Synthetic Data
categories: DifferentialPrivacy NewPaper
---

I have a new paper out on arXiv with my colleagues at UMass Amherst (Ryan McKenna, Daniel Sheldon, and Gerome Miklau). This paper proposes a new method for generating differentially private synthetic data that's tailored to one's use case by only capturing information from the desired marginal distributions. This approach builds on prior work on generating private synthetic data by representing a data distribution as a probabilistic graphical model. See [this post](https://differentialprivacy.org/synth-data-1/) for a summary of current techniques.

Abstract:
> We propose AIM, a novel algorithm for differentially private synthetic data generation. AIM is a workload-adaptive algorithm, within the paradigm of algorithms that first selects a set of queries, then privately measures those queries, and finally generates synthetic data from the noisy measurements. It uses a set of innovative features to iteratively select the most useful measurements, reflecting both their relevance to the workload and their value in approximating the input data. We also provide analytic expressions to bound per-query error with high probability, which can be used to construct confidence intervals and inform users about the accuracy of generated data. We show empirically that AIM consistently outperforms a wide variety of existing mechanisms across a variety of experimental settings.

The preprint is available [here](https://arxiv.org/abs/2201.12677).

<figure style="display: block; margin-left: auto; margin-right: auto; width: 50%">
  <img src="https://media.nga.gov/iiif/5a14c7d2-7aea-4f1b-a1b9-dae2ae1298c5__640/full/!588,600/0/default.jpg">
  <figcaption style="text-align: center"><a href="https://www.nga.gov/collection/art-object-page.69392.html">Classic Landscape (1931) by Charles Sheeler</a></figcaption>
</figure>
