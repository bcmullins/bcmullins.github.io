---
layout: post
title: Resources for Learning Computational Complexity Theory
categories: Helpful
mathjax: true
---

[Computational complexity theory](https://en.wikipedia.org/wiki/Computational_complexity_theory) studies the feasibility of solving and resources required to solve computational problems and is useful to any field that thinks about the analysis and design of algorithms (which is much more broad than one may first think). While there are a good bit of notes and lectures available online, these are scattered across university course pages, YouTube, etc. This guide aims to bring this material together for learning computational complexity theory at the introductory graduate level, especially for those without a formal CS background.

## Background Material

Computational complexity is a topic that goes as mathematically deep as one wants to go. At the edge of the shallow end, it's helpful to be familiar with basic proof writing techniques and discrete math concepts. This is usually the prerequisite for a first undergraduate course in complexity theory and is often covered in appendices or chapter zero of introductory texts. Going a bit deeper to the graduate level, one will want some exposure to rigorous discrete math, particularly graphs and combinatorics with probability, as well as computability and models of computation.

For an introduction to discrete math, check out the relevant chapters from [these lecture notes by James Aspnes](https://www.cs.yale.edu/homes/aspnes/classes/202/notes.pdf). For a more indepth treatment of graph theory, see [Reinhard Diestel's _Graph Theory_ text](http://diestel-graph-theory.com/).

[Harry Porter](http://web.cecs.pdx.edu/~harry/) has an excellent [set of video lectures](https://www.youtube.com/playlist?list=PLbtzT1TYeoMjNOGEiaRmm_vMIwUAidnQz) on theoretical computer science. The first half begins with finite state machines and works up to Turing machines providing a thorough introduction to models of computation. The second half introduces computability theory as well as useful concepts used throughout theoretical computer science such as reduction.

## Books

<img style="float: right; display: inline-block; margin: 0px 0px 0px 20px" width="20%" height="25%" src="https://theory.cs.princeton.edu/complexity/cover.jpg">

The [question of which books to read](https://cstheory.stackexchange.com/questions/3253/what-books-should-everyone-read) has received a lot of attention online. I recommend Arora and Barak's [_Computational Complexity: A Modern Approach_](https://theory.cs.princeton.edu/complexity/) and Part 3 of Sipser's [_Introduction to the Theory of Computation_](http://math.mit.edu/~sipser/book.html). Arora and Barak seems to be the consensus recommendation and offers clear, concise presentations of time and space complexity, hierarchy theorems, and circuit complexity as well as coverage of a wide variety of additional topics. Even better, there's a pdf draft of Arora and Barak available on the book's website.

<img style="float: left; display: inline-block; margin: 0px 20px 0px 0px" width="20%" height="20%" src="https://www.cengage.com/covers/imageServlet?image_type=LRGFC&catalog=cengage&epi=73522117645109331720200508205447742">

While Part 3 of Sipser covers fewer topics (it is just one part of a more comprehensive text), it contains more exposition on early topics than Arora and Barak. For instance, the Sipser text prefaces many proofs with the "proof idea" which provides helpful commentary on the proof strategy and techniques used. These are the sort of helpful comments that would be provided during a lecture but are often missing from the experience of working through a text independently. This makes Sipser a good secondary text even though it only covers the core material.

<!-- <img style="float: right; display: inline-block; margin: 0px 0px 0px 20px" width="20%" height="20%" src="https://assets.cambridge.org/97805218/84730/cover/9780521884730.jpg"> -->

An alternative secondary text is Goldreich's [_Computational Complexity: a Conceptual Perspective_](http://www.wisdom.weizmann.ac.il/~oded/cc-drafts.html). Much like Sipser, Goldreich provides interesting and helpful exposition in places where Arora and Barak fall a bit short. On the book's website, you can find a pdf draft (with only a few formatting issues).  

## Video Lectures

For some people (myself included), hearing and seeing someone walk through an example can be the difference between internalizing the example to build intuition and second-guessing the result each time a similar case comes up. The best comprehensive set of video lectures I've found is a mix from [Ryan O'Donnell's](http://www.cs.cmu.edu/~odonnell/) [undergraduate](https://www.youtube.com/playlist?list=PLm3J0oaFux3YL5vLXpzOyJiLtqLp6dCW2) and [graduate](https://www.youtube.com/playlist?list=PLm3J0oaFux3b8Gg1DdaJOzYNsaXYLAOKH) computational complexity courses at CMU. As a rough guide, consider looking at the second half of the undergraduate course and the first half of the graduate course.

## What's Next?!

Getting a handle on the basics of rigorous computational complexity theory allows one to pursue numerous other areas of computer science, mathematics, and beyond. Below are some that I find interesting and recommendations for a first dive into each area.

### Computational Learning Theory

<img style="float: right; display: inline-block; margin: 0px 0px 0px 20px" width="20%" height="20%" src="/images/blog/complexityTheory/uml.jpg">

[Computational Learning Theory](https://en.wikipedia.org/wiki/Computational_learning_theory) studies machine learning (usually supervised learning) using models and tools from theoretical computer science. Given a well-defined task and framework, this theory seeks to prove general statements along the lines of such-and-such a model class (e.g. linear classifiers) can solve the given task computationally feasibly (usually meaning polynomial time) with reasonable error. A good place to start is with the first half of [_Understanding Machine Learning_](https://www.cs.huji.ac.il/~shais/UnderstandingMachineLearning/). The second half (which is also worth reading) covers applications and advanced topics.

### Cryptography

[Cryptography](https://en.wikipedia.org/wiki/Cryptography#Modern_cryptography) is the mathematical study of secure communication. While there are various notions of security in cryptographic models, security is often defined as the absence of an adversary with such-and-such resources (usually restricted to polynomial time) that can learn such-and-such information.

A good reference here is Boneh and Shoup's [_A Graduate Course in Applied Cryptography_](https://toc.cryptobook.us/). Do note that this book can be quite terse and difficult. Consider [_The Joy of Cryptography_](https://web.engr.oregonstate.edu/~rosulekm/crypto/) for a more gentle introduction. Both books are available in pdf form on their respective websites.

### Computability Theory

<img style="float: right; display: inline-block; margin: 0px 0px 0px 20px" width="20%" height="20%" src="https://media.springernature.com/w153/springer-static/cover/book/9783662624210.jpg">

Whereas complexity theory categorizes computational problems by the resources required to solve them, one way to view computability theory (or recursion theory) is as categorizing computational problems by their [degree of unsolvability](https://en.wikipedia.org/wiki/Turing_degree).

There are several classic texts on computability theory such as [Cutland's _Computability_](https://www.cambridge.org/highereducation/books/computability/E8F085FDBECB8280F7723D71C1D2EE1C#overview); however, the first book that I enjoyed working through was [_The Foundations of Computability Theory_](https://www.springer.com/us/book/9783662624203) by Borut Robič. This book provides a gentle introduction to computability along with a good deal of historical context and an introduction to the [philosophy of mathematics](https://plato.stanford.edu/entries/philosophy-mathematics/).

### Descriptive Complexity

[Descriptive Complexity](https://en.wikipedia.org/wiki/Descriptive_complexity_theory) looks at correspondences between complexity classes and definability in [logics over finite structures](https://courses.engr.illinois.edu/cs498mv/fa2018/FMT.pdf). These results provide an alternative perspective on the relative difficulty of complexity classes as the expressivity required to define particular subsets of a finite structure. In this way, descriptive complexity is analogous to [descriptive set theory](https://en.wikipedia.org/wiki/Descriptive_set_theory) or [effective descriptive set theory](https://en.wikipedia.org/wiki/Effective_descriptive_set_theory). The typical reference for descriptive complexity is Neil Immerman's [_Descriptive Complexity_](https://people.cs.umass.edu/~immerman/book/descriptiveComplexity.html).


### Mathematical Philosophy

Mathematical philosophy (also called formal philosophy or [exact philosophy](http://meta.phil.ufl.edu/host/sep/index.html)) considers philosophical questions by applying concepts and tools from mathematics and logic. The most popular area of formal philosophy at the moment is [formal epistemology](https://plato.stanford.edu/entries/formal-epistemology/) which - among other things - studies probabilistic and logical models of belief and decision.

In a wide-ranging survey article, [Scott Aaronson](https://scottaaronson.com/) makes the case that philosophy - and mathematical philosophy in particular - [would benefit from considering matters of computational complexity in addition to computability](https://www.scottaaronson.com/papers/philos.pdf). Aaronson speculates that philosophers grapple with computability rather than complexity since the former shares intellectual roots with interwar analytic philosophy and workings in the foundations of mathematics while the latter was developed later by computer scientists after the two diverged in interests.
