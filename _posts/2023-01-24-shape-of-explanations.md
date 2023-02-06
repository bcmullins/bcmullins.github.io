---
layout: post
title: New Paper - The Shape of Explanations&#58; A Topological Account of Rule-Based Explanations in Machine Learning
categories: ExplainableML NewPaper
mathjax: true
---

I have a new paper out that will be presented at the [AAAI 2023 Workshop on Representation Learning for Responsible Human-Centric AI](https://r2hcai.github.io/AAAI-23/). This paper introduces a formal model to explore [rule-based explanations](https://christophm.github.io/interpretable-ml-book/anchors.html) for classifiers. Explanations of this sort explain a classification by providing a simple sufficiency condition. For example, if an applicant's loan is rejected by a predictive model, a rule-based explanation may be that the application belongs to the group with outstanding debt greater than $X$, missed payments greater than $Y$, etc. and every application (or close to every application) in this group is rejected. The key observation is that this rule completely describes a region in the feature space. One way to think about a [topology](https://ncatlab.org/nlab/show/topological+space) on a space is that it provides a language for describing subsets of the space with some being more descriptively complex than others (which we can describe using known hierarchy results such as the [Borel hierarchy](https://en.wikipedia.org/wiki/Borel_hierarchy)). Using this, we prove that a classifier being explainable is equivalent to the inverse image of each label being the union of a descriptively simple set and a [small set](https://ncatlab.org/nlab/show/sigma-ideal).

Abstract:
> Rule-based explanations provide simple reasons explaining the behavior of machine learning classifiers at given points in the feature space. Several recent methods (Anchors, LORE, etc.) purport to generate rule-based explanations for arbitrary or black-box classifiers. But what makes these methods work in general? We introduce a topological framework for rule-based explanation methods and provide a characterization of explainability in terms of the definability of a classifier relative to an explanation scheme. We employ this framework to consider various explanation schemes and argue that the preferred scheme depends on how much the user knows about the domain and the probability measure over the feature space.

The conference paper is available [here](https://doi.org/10.48550/arXiv.2301.09042). Here's short [pitch video](https://youtu.be/2QXo2ZGZGKs) as well.

<figure style="display: block; margin-left: auto; margin-right: auto; width: 50%">
  <img src="https://media.nga.gov/iiif/276f93dd-fa1c-4f81-94df-1a8e7567b58d/full/!384,384/0/default.jpg">
  <figcaption style="text-align: center"><a href="https://www.nga.gov/collection/art-object-page.52399.html">Winter Valley (1944) by Lamar Dodd</a></figcaption>
</figure>
