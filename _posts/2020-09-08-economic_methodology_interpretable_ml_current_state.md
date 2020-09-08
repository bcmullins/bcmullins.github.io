---
layout: post_emiml
title: Economic Methodology Meets Interpretable Machine Learning - Part IV - Current State of Economic Methodology
categories: PhilScience
mathjax: true
---

This post looks at the current state of economic methodology with respect to the realistic assumptions debate. After briefly surveying the history of economic methodology, we'll walk through two recent arguments in the realistic assumptions debate: one in favor of instrumentalism as a theoretical ideal and the other favoring a limited form of realism in practice. In light of these arguments, I'll argue that practitioners can still adopt some form of limited realism in practice if such an approach is a expedient guide to creating models with desirable properties.

## The Recent History of Economic Methodology
The Philosophy of Economics and Economic Methodology have received excellent, approachable historical surveys from [Dan Hausman](http://revue-philosophie-economique.com/num/2017-2-vol-18-varia/philosophy-of-economics-a-retrospective-reflection/) and [Wade Hands](https://www.cairn-int.info/journal-revue-de-philosophie-economique-2019-2-page-221.htm) in recent years. Since its modern inception in the mid-1970s, Economic Methodology has been influenced by trends in, unsurprisingly, both economics and philosophy. In the latter half of the twentieth century, methodology was greatly influenced by the [logical empiricism](https://plato.stanford.edu/entries/logical-empiricism/) program in the Philosophy of Science which was interested in formal theories of language, induction, and scientific laws. Hands uses the phrase "the shelf of scientific philosophy" to describe the early approach to economic methodology. In these cases, perspectives from philosophy of science, such as [Popper's falsificationism](https://plato.stanford.edu/entries/scientific-method/#PopFal), [Lakatos' research programmes](https://plato.stanford.edu/entries/lakatos/#ImprPoppScie), and so forth, were directly applied to economics in more-or-less a cookie cutter fashion. In a later, more mature phase, philosophers of economics would recognize properties of economics that differentiate it from the physical sciences.

Moving into the early twenty-first century, methodology becomes influenced by the [empirical turn in economics](https://www.aeaweb.org/research/charts/an-empirical-turn-in-economics-research). To illustrate this turn, the graph below summarizes results from [a paper by Joshua Angrist et al.](https://pubs.aeaweb.org/doi/pdfplus/10.1257/aer.p20171117#page=4) which attempts to classify publications in economics as either theory or empirical by subfield. The authors find the share of empirical papers to be substantially increasing over time nearly across the board during this time frame.

<img style="margin-left: auto; margin-right: auto; margin: 0px 0px 10px 10px" src="https://www.aeaweb.org/content/file?id=4757">

Hands suggests that the empirical turn is part of a broadening of the set of methods available to the economist:
>The Walrasian and econometric normal science that characterized the second half of the twentieth century gave way to a much more diverse set of scientific practices in recent years: game theory, behavioral economics, behavioral welfare economics, new empirical techniques and evidence-based economics of various forms, agent-based and complexity economics, and others.

Hausman notes that, while the economic methodology in the past focused on scientific laws, today's methodological work focuses on causality and estimation. Note, though, that the concept of constructing models has always been central (see Mary Morgan's [The World in the Model](https://www.cambridge.org/core/books/world-in-the-model/6FD82E4D498F94CBE5F56078FD007729)); it's only what is meant by model that has shifted and broadened over time. One issue that continues to rear its head in Economic Methodology is the realistic assumptions debate. Hands refers to this debate as "the issue of false assumptions and highly idealized models" and describes it as "one of the longest-running debates in economic methodology". In the past decade, several new arguments have appeared lending fresh perspectives to this debate. Below, we consider two such arguments that I find particularly convincing.

## Reiss Cheers for Instrumentalism

In [Idealization and the Aims of Economics](https://www.cambridge.org/core/journals/economics-and-philosophy/article/idealization-and-the-aims-of-economics-three-cheers-for-instrumentalism/07E3296CC23CD12444C39901783C79AF), Julian Reiss argues in favor of instrumentalism in economics since practitioners care about the results of true/causal assumptions rather than caring intrinsically about truth and causation. Reiss holds that this is the case even if we take full or strong realism as naive and adopt a limited or causal realism where only the relevant causal mechanism is accurately captured in the assumptions.

One feature we expect of a good model is to give accurate predictions of relevant phenomena in the world. Reiss offers us the following argument:  

>Suppose, then, a new model can be built that has just the same degree of significance along one dimension as the old model – the same degree of predictive accuracy, say – but it has the additional virtue of being true. There are now two possibilities. Either the true model brings with it some additional significance (along some other dimension). In this case nothing is lost by demanding significance alone, as the instrumentalist does. Or the model brings no additional significance. But if this is the case, it is very hard to see what that additional value should be.

We see a similar argument regarding causal mechanisms:

>why seek to discover underlying causal structure? The classical answer is that knowing causal structure has a number of cognitive and practical virtues. We know now that causal knowledge has these virtues at best contingently but not necessarily. It is other features that realize the cognitive and practical virtues we seek,and causality may or may not co-occur with these other features. But then to the extent that we do want the virtues, we should seek the relevant features and not causality.

>...building causal models has enormous informational requirements. The probabilistic theory of causation proves this point. In one formulation this theory says that to learn a new causal law ‘C causes E’ from probabilistic dependencies, one has to stratify with respect to all other causes of E(Cartwright 1979). That is, only when the probabilistic dependence of E on C persists conditional on all other causes of E, the probabilistic dependence is indicative of a causal relation. But when are we ever in the fortuitous position to know all but one causes of an outcome of interest?

Reiss' conclusion is that practitioners ought to focus on the predictive accuracy and robustness of their models rather realistic assumptions or underlying causal mechanisms, since we ultimately care about the former and not latter.  

## Causal Mechanisms in Practice

[Economic Modelling as Robustness Analysis](https://academic.oup.com/bjps/article-abstract/61/3/541/1395474) argues that the practice of establishing derivational robustness in economics provides epistemic support for economic theories in lieu of empirical evidence.

The authors (Jaakko Kuorikoski, Aki Lehtinen, and Caterina Marchionni) divide model assumptions into three categories: substantial assumptions, Galilean assumptions, and tractability assumptions. Substantial assumptions "identify a set of causal factors that in interaction make up the causal mechanism about which the modeller endeavours to make important claims". These are the claims we expect to be veridical. Galilean assumptions act to isolate the causal mechanism modeled by the Substantial assumptions. Tractability assumptions simply the problem, e.g. assuming some function is linear or simple and so forth.

The act of establishing derivational robustness involves proving that the result attained from the Substantial assumptions holds under a variety of Galilean and Tractability assumptions. The authors provide an example from Geographical Economics whereby a [model is constructed by Paul Krugman](https://www.journals.uchicago.edu/doi/abs/10.1086/261763) showing geographic concentration under particular conditions. Further research has extended Krugman's results to show that they hold under more general Galilean and Tractability assumptions. This lends credence that the models' Substantial core captures the essential mechanisms involved in this economic process.

On the one hand, this argument is a rational reconstruction for a widespread practice among economists: attempting to establish robustness of the core mechanisms of a model against varying auxiliary assumptions. On the other, this is a sort of middle position of limited realism or at least a way to put a form of limited realism into practice. Note that realism is limited since only the Substantial assumptions are taken to be true.

## Having it both ways?

Though there is an apparent conflict between the above arguments for instrumentalism and limited realism, we may resolve it by considering the perspective of the practitioner while still accepting both arguments.

Let's begin with the observation that at the level of the practitioner, it doesn't matter what the ultimate justification for a method or methodology is. All that matters to the practitioner (on an optimistic interpretation) is whether or not a method or methodology sufficiently achieves the practitioner's goals, e.g. predictive accuracy, robustness, etc. Moreover, practitioners are under no obligation to use optimal methods.

The practitioner may concede to Reiss that the ultimate justification of their methods is not truth, causation, etc. but to attain models with other desirable properties. This does not rule out, however, that practitioners may employ methods or methodologies which rely on true assumptions or causal mechanisms if they sufficiently achieve a practitioner's goals. In this sense, we can read Reiss as not arguing against methods or methodologies that rely on veridical or causal assumptions but against the necessity of such assumptions.

This leaves us with the amusing (meta)-methodological principle to use methods or methodologies that produce _good_ models.
