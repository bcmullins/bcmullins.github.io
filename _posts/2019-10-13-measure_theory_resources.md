---
layout: post
title: Resources for Learning Measure Theory
categories: Helpful
mathjax: true
---

When approaching measure theory for the first time, the ideas can seem opaque and unmotivated. This is amplified since many students of measure theory are not coming from a strictly mathematics background and may be approaching the material on their own outside of the classroom. In addition to first-year math graduate students and advanced math undergraduates, students in stats, economics, the hard sciences, etc. will find their way into learning measure theory. This is a guide to resources for learning measure theory that tries to keep in mind that many (myself included) approach the material with an atypical background.

## Background

To work through the material for measure theory, one should be familiar with the concepts and basic results from real analysis (limit, sup/inf, metric, etc.) and have some exposure to general topology (open sets, closed sets, continuity, etc.). While not strictly necessary depending on one's background, it's helpful to have exposure to both the differential calculus and probability to have mental models available to check against these measure-theoretic ideas. Francis Su provides an excellent [set of video lectures](https://analysisyawp.blogspot.com/2013/01/lectures.html) to get one up to speed on real analysis. As for the elements of topology, I suggest taking a look at the book [_Topology without Tears_](http://www.topologywithouttears.net) by Sidney A. Morris, available for free in pdf form.

## Books

I recommend two texts: Richard Bass' _Real Analysis for Graduate Students_ as the primary text and David Bressoud's _A Radical Approach to Lebesgue's Theory of Integration_ as a supplement.

<img style="float: right; display: inline-block; margin: 0px 0px 0px 20px" width="25%" height="25%" src="http://bass.math.uconn.edu/real-cover.jpg">

While there are stacks upon stacks of measure theory texts available, the Bass book combines instructive proofs with an organization that motivates the material and a collection of interesting and (sometimes) difficult exercises. These more difficult exercises will be particularly useful for those studying for Comps/Quals. The selling point is that all versions of the book are available in pdf form on the [author's website](http://bass.math.uconn.edu/real.html).

A typical course in measure theory will take one through chapter fifteen. This starts with the definition of a measure on sets (1-4) to a measure on a function (5) to integration and differentiation of functions (6-14) and, finally, to $\mathcal{L}_p$ spaces of functions (15). The Bass book includes chapters on topology (20) and measure-theoretic probability (21) for foundations and applications, respectively; however, these sections are not as well put-together as the first half of the book. With that being said, this book contains everything one needs to get a handle on measure theory in a reasonably digestible form.

<img style="float: left; display: inline-block; margin: 0px 20px 0px 0px" width="25%" height="25%" src="https://www.macalester.edu/~bressoud/books/ARattleToy.jpg">

While the Bass book contains the meat of a course on measure theory, it often lacks the context one may find in a classroom discussion. Bressoud's [_A Radical Approach to Lebesgue's Theory of Integration_](https://www.cambridge.org/us/academic/subjects/mathematics/abstract-analysis/radical-approach-lebesgues-theory-integration?format=PB&isbn=9780521711838) approaches the Lebesgue integral and measure theory more generally from a historical perspective. This book need not be read cover-to-cover; I've found it is more useful to skip around to relevant sections. I *do* recommend reading chapters three, four, and five on the current conception of $\mathbb{R}$, the problem posed to Riemann integration by nowhere dense sets, and the development of early measure theory.

## Video Lectures

It can often be difficult to learn streamlined material developed for a first-year graduate course outside the context of that course. For some people (myself included), hearing and seeing someone walkthrough an example can be the difference between internalizing the example to build intuition and second-guessing the result each time a similar case comes up.

If this sounds like you, the [collection of measure theory lectures](https://www.youtube.com/playlist?list=PLo4jXE-LdDTQq8ZyA8F8reSQHej3F6RFX) from [Claudio Landim](http://w3.impa.br/~landim/) will be a great help! Landim's lectures provide a comprehensive measure theory course that captures the feel of a classroom with over 30 hours of material. Landim is particularly good with providing insightful examples and helping the viewer focus on the key steps in proofs.

## What's Next?!

Getting a handle on the basics of measure theory allows one pursue numerous areas of mathematics and its applications. Below are some that I find interesting and recommendations for a first dive into each area.

### Measure-theoretic Probability

<img style="float: right; display: inline-block; margin: 0px 0px 0px 20px" width="25%" height="25%" src="http://probability.ca/jeff/grprobcov2.jpg">

Measure theory is the most common foundation for a rigorous treatment of probability. Many of the odd rules one sees in an initial treatment of probability are reduced to questions of measure theory. For instance, rather than having a rule or heuristic saying that the probability of a continuous random variable taking the value of a single point is zero, we can observe that a probability measure with a continuous density function is absolutely continuous to the Lebesgue measure and that a single point is a Lebesgue null or measure zero set.

For this, I recommend Jeffrey Rosenthal's [A First Look at Rigorous Probability Theory](http://probability.ca/jeff/grprobbook.html). This book also opens up paths to explore in financial mathematics, stochastic process models, etc.

### Topology

<img style="float: right; display: inline-block; margin: 0px 0px 0px 20px" width="25%" height="25%" src="https://www.pearsonhighered.com/assets/bigcovers/0/1/3/1/0131816292.jpg">

In typical treatments of measure theory, one begins by working with the Lebesgue measure in euclidean space and then generalizes to measures on other sorts of spaces, e.g., the counting measure on the space formed by subsets of the natural numbers. Though more abstract, these spaces are but one sort of topological space. Point-set topology is the study of properties of and between general topological spaces.

The recommended text in this area is the first half of James Munkres' [_Topology_](https://www.pearson.com/us/higher-education/program/Munkres-Topology-2nd-Edition/PGM56881.html). The second half of this book devoted to Algebraic Topology, a different perspective on studying topological spaces; however, better treatments exist of this latter topic. While Munkres can be terse at times, his dark humor is undeniable: see the exposition beginning Section 33 on the Urysohn Lemma. I read it as humor anyhow.

### Measure Theory meets Topology

<img style="float: right; display: inline-block; margin: 0px 0px 0px 20px" width="25%" height="25%" src="https://images.springer.com/sgw/books/medium/9780387905082.jpg">

In measure theory, we have a notion of small or negligible sets: null sets. A corresponding notion of small or negligible sets in a topological space is that of being [meagre](https://en.wikipedia.org/wiki/Meagre_set), i.e., the countable union of nowhere dense sets. John Oxtoby's [_Measure and Category_](https://www.springer.com/gp/book/9780387905082) studies analogies between these two concepts and proves "duality results" on when we can interchange meagre for null sets (and vice versa) in theorems.

One aspect of meagre sets being negligible is that they contain no non-trivial open subsets. One may be tempted to think that the meagre sets are just the null sets on the reals; however, [this is not the case](https://mathoverflow.net/questions/43478/is-there-a-measure-zero-set-which-isnt-meagre). We can partition $\mathbb{R}$ into a null set and a meagre set of low Borel rank.

### Descriptive Set Theory

Descriptive set theory studies the structure and properties of "well-behaved" subsets of the reals and similar but more general spaces called [polish spaces](https://en.wikipedia.org/wiki/Polish_space). One starting place is the structure of the Borel sets, i.e., the closure of the open sets by repeated application of countable union, countable intersection, and complementation. An introduction in this direction is S. M. Srivastava's [_A Course on Borel Sets_](https://www.springer.com/gp/book/9780387984124). I will also point to a set of accessible [lecture notes](http://www.personal.psu.edu/jsr25/Spring_11/574_Sp11_Syllabus.html) by Jan Reimann.

This area forms the foundation for one of my primary interests: topological learning theory (link coming soon).

### History of Measure Theory

<img style="float: right; display: inline-block; margin: 0px 0px 0px 20px" width="25%" height="25%" src="https://www.maa.org/sites/default/files/HawkinsLebesque.jpg">

If you've read Bressoud's text that I offer as a supplement above, then you'll be familiar with Thomas Hawkins' [_Lebesgue's Theory of Integration: Its Origins and Developments_](https://bookstore.ams.org/chel-282/). Hawkins' book seems to be _the_ comprehensive account of the early history of the Lebesgue integral and the abstract measure theory that developed from it. I've not yet made it all the way through this one; it is on my list through!
