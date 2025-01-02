---
layout: post_top
title: Interesting Articles I've Read in 2024
categories: Review
mathjax: true
---

Below is a collection of interesting articles I've read in 2024. Three papers are on differential privacy and adjacent topics. There's a recent method for [differentially private SGD](#improved-differential-privacy-for-sgd-via-optimal-private-linear-operators-on-adaptive-streams) utilizing methods from private query answering, an intuitive [watermarking scheme](#a-watermark-for-large-language-models) for language models, and a paper from 1986 that [proposed $k$-anonymity](#finding-a-needle-in-a-haystack-or-identifying-anonymous-census-records) before it was formalized as a criterion for de-identification. Several papers are on the history of ideas ranging from [early twentieth century pragmatism](#taking-pragmatism-seriously-enough-toward-a-deeper-understanding-of-the-british-debate-over-pragmatism-ca-1900-1910), the synergies and antagonisms between [poetry and philosophy](#poetry-and-philosophy), and the relation between [periodicals and intellectual progress](#on-the-reciprocal-influence-of-the-periodical-publications-and-the-intellectual-progress-of-this-country) to the deaths of [Analytical Marxism](#john-rawls-and-the-death-of-western-marxism) and [Effective Altruism](#the-deaths-of-effective-altruism).

Two papers concern mathematical logic. One from 1924 [reduces quantified formulas to functions](#on-the-building-blocks-of-mathematical-logic) and is foundational for functional programming. Another [explores the continuum hypothesis](#how-the-continuum-hypothesis-could-have-been-a-fundamental-axiom) as an axiom of set theory. Finally, there's a look at the [early history of cocaine and culture](#cocaine-a-cultural-history-from-medical-wonder-to-illicit-drug), a nineteenth century legal battle between [evolutionary theory and spiritualism](#charles-darwin-and-associates-ghostbusters), and reflections on the [generational dominance of US politics](#one-generation-has-dominated-american-politics-for-over-30-years). If you have some thoughts on my list or would like to share yours, send me an email at brettcmullins(at)gmail.com. Enjoy the list!

<!-- 

## title
______

Author: 

Publication: 

Published: 

Link: 

-->

## Finding a needle in a haystack or identifying anonymous census records
______

Author: [Tore Dalenius](https://www.genealogy.math.ndsu.nodak.edu/id.php?id=129065)

Publication: [Journal of Official Statistics](https://en.wikipedia.org/wiki/Journal_of_Official_Statistics)

Published: 1986

Link: [Click Here](https://www.scb.se/contentassets/ca21efb41fee47d293bbee5bf7be7fb3/finding-a-needle-in-a-haystack-or-identifying-anonymous-census-records.pdf)

Lately, I've been reading papers in the [statistical disclosure](https://en.wikipedia.org/wiki/Statistical_disclosure_control) literature before [differential privacy](https://en.wikipedia.org/wiki/Differential_privacy) i.e. before 2006. This short paper introduces what would later be called [$k$-anonymity](https://en.wikipedia.org/wiki/K-anonymity), a criterion of privacy that was/is widely applied especially to government datasets. $k$-anonymity would be formalized in a [series of papers](https://dataprivacylab.org/dataprivacy/projects/kanonymity/kanonymity.html) by [Latanya Sweeney](https://en.wikipedia.org/wiki/Latanya_Sweeney) and others in the late 1990s and early 2000s. 

For a dataset containing sensitive information about individuals such as [Census data](https://data.census.gov), a notion of privacy called [de-identification](https://en.wikipedia.org/wiki/De-identification) seeks to make it impossible to link a record in the dataset with an individual. Removing [personally-identifiable information](https://en.wikipedia.org/wiki/Personal_data) (PII) from the data may not be sufficient to prevent [re-identification](https://en.wikipedia.org/wiki/Data_re-identification), since some records may still be unique or only appear a few times. 

<figure style="float: right; display: inline-block; margin: 0px 0px 0px 15px">
    <img width="275" height="250" src="/images/blog/interesting_articles_2024/aliceBob.png">
    <figcaption style="text-align: center; font-size: 12px;">Alice de-anonymizing Bob</figcaption>
</figure>

For example, if Alice knows Bob's age and zip code, she may be able to identify him in a dataset even if his name has been removed. If Bob's age and zip code combination is unique, then Bob would be the only 45 year old living in downtown Chicago and Alice could identify him perfectly. If, however, there are only a few people that share Bob's age and zip code, Alice could still identify Bob with high probability. In the latter case, age and zip code are [quasi-identifiers](https://en.wikipedia.org/wiki/Quasi-identifier), which Dalenius coins in this paper.

Dalenius sketches a few ways to check if $k$-anonymity is satisfied and considers what to do if it's not. A dataset is said to be $k$-anonymous for a set of attributes if, for every record in the dataset, there are at least $k-1$ other records that share the same values on the given attributes. In the example above, if the dataset is 2-anonymous, then Bob would not be perfectly identifiable because there would be at least one other record that shares his age and zip code.

If anonymity is not satisfied and privacy is potentially compromised, what should we do with the data? We could throw the records away, but that could have unpredictable downstream effects. We could suppress quasi-identifier attributes in the records. Not only does this inherit the former issue, but [imputation](https://en.wikipedia.org/wiki/Imputation_(statistics)) could be used to recover the suppressed data. We could "perturb the data", by which he means something like [generating synthetic data](https://differentialprivacy.org/synth-data-0/). Finally, we could implement an encrypted computation scheme such as [homomorphic encryption](https://en.wikipedia.org/wiki/Homomorphic_encryption) to compute statistics while not directly exposing the data. Unsurprisingly, these latter two options also run into privacy issues of their own. 

## One generation has dominated American politics for over 30 years
______

Publication: [The Economist](https://en.wikipedia.org/wiki/The_Economist)

Published: 2024

Link: [The Economist](https://www.economist.com/briefing/2024/07/04/one-generation-has-dominated-american-politics-for-over-30-years)

This article is an interesting time capsule. Published on July 4th of this year, Biden had yet to withdraw from the Presidential race and the attempted assassination of Trump was a week or so away. At the time, Biden and Trump were [historically unpopular candidates](https://www.nybooks.com/online/2024/07/02/savior-complex-biden/). 

<figure style="float: right; display: inline-block; margin: 0px 10px 0px 10px">
    <img width="225" height="250" src="/images/blog/interesting_articles_2024/age.png">
    <figcaption style="text-align: center; font-size: 12px;">Credit: The Economist</figcaption>
</figure>

The pair also have in common their decade of birth, the 1940s, one which has dominated US politics over the past thirty years. With the exception of Obama, every president from Clinton onward - as well as many challengers on the opposing ticket - were born in the 1940s. The article points to this generation's hold on power as a source of political disfunction, rehashing the rhetoric and disputes of the tumultuous late 1960s. 

As this generation aged, so did the average age of politicians in the US. While US presidents are getting older on average each election over the past fifty years, the trend for OECD political leaders is slightly downward sloping. Moreover, of these countries, the US has the oldest legislature on average in both upper and lower houses. The Economist explores this in depth with their recent podcast [Boom!](https://www.economist.com/audio/podcasts/boom); however, I haven't had a chance to listen yet. 

## Taking Pragmatism Seriously Enough: Toward a Deeper Understanding of the British Debate over Pragmatism, ca. 1900-1910
______

Author: [Ymko Braaksma](https://scholar.google.com/citations?user=Lo15zhMAAAAJ&hl=nl)

Publication: [Journal of the History of Ideas](https://www.wikipedia.org/wiki/Journal_of_the_History_of_Ideas)

Published: 2024

Link: [Click Here](https://muse.jhu.edu/article/917116)

In the early twentieth century, a leading Idealist philosopher in Britain, [F. H. Bradley](https://plato.stanford.edu/entries/bradley/), posited that he may be a [pragmatist](https://plato.stanford.edu/entries/pragmatism/) after all. Roughly speaking, [idealism](https://en.wikipedia.org/wiki/Idealism) is a speculative approach to philosophy that studies reality as a whole and often in a top-down fashion. Bradley's idealism sets such a high bar for knowledge and truth that he thinks it practically unattainable. Rather than give in to skepticism, [Bradley adopts a pragmatic view](https://www.jstor.org/stable/2248158) as the best one can do. 

<figure style="float: right; display: inline-block; margin: 0px 10px 0px 10px">
    <img width="200" height="200" src="/images/blog/interesting_articles_2024/schiller.jpg">
    <figcaption style="text-align: center; font-size: 12px;">F. C. S. Schiller</figcaption>
</figure>

Braaksma argues that [F. C. S. Schiller's response](https://www.jstor.org/stable/2248541) is instructive for understanding pragmatic thought. [Schiller](https://en.wikipedia.org/wiki/F._C._S._Schiller) denies that Bradley is a pragmatist because Bradley's account of truth and knowledge still aims to attain absolute certainty. The pragmatism of Schiller, [John Dewey](https://plato.stanford.edu/entries/dewey/), and [William James](https://plato.stanford.edu/entries/james/) conceives the aim of thought through an evolutionary and psychological frame "whose main function is helping an organism live". On this account, pragmatism is less about ends and more about the means of one's theories of truth and knowledge.

Recent work by [Cheryl Misak](https://en.wikipedia.org/wiki/Cheryl_Misak) and others has [sought to reexamine](https://aeon.co/essays/pragmatism-is-one-of-the-most-successful-idioms-in-philosophy) or perhaps [revive pragmatism]({{ site.baseurl }}{% link _posts/2021-05-18-frank_ramsey_bio.md %}) along the lines of [C. S. Peirce's](https://plato.stanford.edu/entries/peirce/) program. Braaksma contends that Schiller's program is likewise worthy of reexamination. 

## Improved Differential Privacy for SGD via Optimal Private Linear Operators on Adaptive Streams
______

Authors: [Sergey Denisov](https://scholar.google.com/citations?user=xiiiSa8AAAAJ&hl=en), [Brendan McMahan](https://scholar.google.com/citations?user=iKPWydkAAAAJ&hl=en), [Keith Rush](https://scholar.google.com/citations?user=OrUyRAcAAAAJ&hl=en), [Adam Smith](https://scholar.google.com/citations?user=fkGi-JMAAAAJ&hl=en), and [Abhradeep Guha Thakurta](https://athakurta.squarespace.com)

Publication: [NeurIPS Proceedings](https://en.wikipedia.org/wiki/Conference_on_Neural_Information_Processing_Systems)

Published: 2022

Link: [arXiv](https://arxiv.org/abs/2202.08312)

The predominant method for [privately training](https://spkreddy.org/ppmlfall2024.html) a machine learning model is [differentially private stochastic gradient descent](https://arxiv.org/abs/1607.00133) (DP-SGD). This method adds Gaussian noise to the bounded gradient at each step with noise calibrated to one's privacy budget (as well as the bounding details), viewing each gradient measurement as a separate query. 

<figure style="display: block; margin: 0px 0px 0px 0px">
  <img style="display: block; margin: 0px 10px 10px 0px" src="/images/blog/interesting_articles_2024/training.gif">
  <figcaption style="text-align: center; font-size: 12px;">From <a href="https://research.google/blog/making-ml-models-differentially-private-best-practices-and-open-challenges/">this primer on private ML</a> from Google; see <a href="https://arxiv.org/abs/2303.00654">How to DP-fy ML A Practical Guide to Machine Learning with Differential Privacy</a></figcaption>
</figure>

This paper introduces a new method for differentially private SGD that treats gradient measurement as a prefix query on the sequence of gradients. The key observation is that the gradient at each step is a sum of prior gradients. To optimally add noise to the gradient, the authors use a variant of the [matrix mechanism](https://dl.acm.org/doi/10.1007/s00778-015-0398-x), a method for optimally answering linear queries under differential privacy. The matrix mechanism utilizes [factorization](https://en.wikipedia.org/wiki/Matrix_decomposition) to allow one to answer a workload of queries with low sensitivity and reconstruct answers to the desired workload with minimal noise. 

This approach to differentially private SGD is now called DP-MF for matrix factorization. In addition to vanilla SGD, this framework can accommodate [SGD with momentum](https://en.wikipedia.org/wiki/Stochastic_gradient_descent#Momentum) or any extension that uses a linear function of the gradients. Empirically, this approach to noise addition yields significantly higher accuracy on the test set compared to existing methods.

This is a really cool paper because it shows how improvements in fundamental tasks such as private query answering ([which is what I work on]({{ site.baseurl }}{% link research.md %}#differentially-private-synthetic-data)) can be applied to make non-trivial advances in other areas.

## Cocaine: a cultural history from medical wonder to illicit drug
______

Author: [Douglas R. J. Small](https://www.edgehill.ac.uk/person/dr-douglas-small/staff/)

Publication: [Aeon](https://aeon.co/)

Published: 2024

Link: [Click Here](https://aeon.co/essays/cocaine-a-cultural-history-from-medical-wonder-to-illicit-drug)

During the forty year period from 1880 to 1920, [cocaine](https://en.wikipedia.org/wiki/Cocaine) went from an obscure compound to a wonder drug, then, to a controlled substance and the attributed cause of social ills. While cocaine was known as a painkiller and stimulant, [Karl Koller](https://en.wikipedia.org/wiki/Karl_Koller_(ophthalmologist)), an ophthalmologist and colleague of [Sigmund Freud](https://en.wikipedia.org/wiki/Sigmund_Freud) in Vienna, [discovered its properties](https://pubmed.ncbi.nlm.nih.gov/22531385/) as a local anesthetic in 1884. This finding changed how some surgeries were practiced, since patients were no longer required to be fully sedated. 

<figure style="float: right; display: inline-block; margin: 0px 10px 0px 10px">
    <img width="200" height="250" src="/images/blog/interesting_articles_2024/homes_cocaine.jpeg"/>
    <figcaption style="text-align: center; font-size: 12px;"><a href="https://books.google.com/books?id=Nte_tAEACAAJ&dq=subcutaneously+my+dear+watson&hl=en&newbks=1&newbks_redir=0&sa=X&ved=2ahUKEwjxtOXc5s-KAxVUrYkEHbwJIgYQ6AF6BAgEEAE">Subcutaneously, My Dear Watson</a> (1978)<br/>by Jack Tracy and Jim Berkey</figcaption>
</figure>

Cocaine quickly grew in popularity. In [Arthur Conan Doyle's](https://en.wikipedia.org/wiki/Arthur_Conan_Doyle) [The Sign of the Four](https://en.wikipedia.org/wiki/The_Sign_of_the_Four) (1890), [Sherlock Holmes'](https://en.wikipedia.org/wiki/Sherlock_Holmes) use of cocaine intravenously was meant to depict him as a modern man informed by late Victorian science. By 1904, however, [Watson](https://en.wikipedia.org/wiki/Dr._Watson) recounts in the short story [The Missing Three-Quarter](https://en.wikipedia.org/wiki/The_Adventure_of_the_Missing_Three-Quarter) that Holmes had to be weaned off of cocaine due to dependence. This illustrates how quickly the worm turned on this panacea. Over the next two decades, the sale of cocaine would be [restricted to medical professionals](https://en.wikipedia.org/wiki/Cocaine#Popularization) in many countries and [alternative local anesthetics](https://en.wikipedia.org/wiki/Local_anesthetic#History) would be introduced.

This article is a pitch for the author's recent book [Cocaine, Literature, and Culture, 1876-1930](https://www.bloomsbury.com/us/cocaine-literature-and-culture-18761930-9781350400092/) (2024). In many ways, it feels like I'm the target audience by connecting an interesting topic with the history of science and Sherlock Holmes. This article is doubly fitting given that I read Benjamin Blood's [reflections on philosophical reasoning under anesthesia]({{ site.baseurl }}{% link _posts/2024-11-22-research-from-1874.md %}#the-anaesthetic-revelation-and-the-gist-of-philosophy) from 1874 this year.

## On the building blocks of mathematical logic
______

Author: [Moses Schönfinkel](https://en.wikipedia.org/wiki/Moses_Schönfinkel)

Original Title: Über die Bausteine der mathematischen Logik

Publication: [Mathematische Annalen](https://en.wikipedia.org/wiki/Mathematische_Annalen)

Published: 1924

Translated in _From Frege to Gödel: A Source Book in Mathematical Logic_, edited by [Jean van Heijenoort](https://en.wikipedia.org/wiki/Jean_van_Heijenoort) and introduced by [W. V. O. Quine](https://plato.stanford.edu/entries/quine/)

Link: [Internet Archive](https://archive.org/details/fromfregetogodel0000vanh/page/n5/mode/2up)

A typical exercise in a first course in mathematical logic is to prove that [propositional logic](https://iep.utm.edu/propositional-logic-sentential-logic/) can be expressed using only two of the typical operators such as $\neg, \lor$ i.e. _not_ and _or_. In 1913, [Henry Sheffer](https://en.wikipedia.org/wiki/Henry_M._Sheffer) proved that there is a single operator — now called [NAND](https://mathworld.wolfram.com/NAND.html) — capable of expressing all of propositional logic given by $A \mid B = \neg A \lor \neg B$ for propositions $A, B$. 

In this paper, Schönfinkel proves a similar but deeper result for [first-order logic](https://en.wikipedia.org/wiki/First-order_logic) that reduces quantification, variables, and predicates to functions. In this setting, first-order logic can be expressed using three functions: a constant function $K$, a substitution function $S$, and a version of NAND $U$ for quantified predicates. Schönfinkel's presentation is elegant, powerful, and philosophically reflective.

If the idea of building up formulas from functions sounds familiar, it is the basis for [functional programming](https://en.wikipedia.org/wiki/Functional_programming). In 1927, [Haskell Curry](https://en.wikipedia.org/wiki/Haskell_Curry) discovered Schönfinkel's paper and began developing [combinatory logic](https://plato.stanford.edu/entries/logic-combinatory/), where these sorts of reducing functions are called combinators. [Stephen Wolfram](https://en.wikipedia.org/wiki/Stephen_Wolfram) has written an [interesting history of Schönfinkel](https://writings.stephenwolfram.com/2020/12/where-did-combinators-come-from-hunting-the-story-of-moses-schonfinkel/) centered around this paper. I discuss Schönfinkel's paper in my [survey of research from 1924]({{ site.baseurl }}{% link _posts/2024-07-07-research-from-1924.md %}). 

## John Rawls and the death of Western Marxism
______

Author: [Joseph Heath](https://en.wikipedia.org/wiki/Joseph_Heath)

Publication: [In Due Course](https://josephheath.substack.com)

Published: 2024

Link: [Substack](https://josephheath.substack.com/p/john-rawls-and-the-death-of-western)

In the midst of Cold War Rationality in the late 1970s and 1980s, [Marxism](https://en.wikipedia.org/wiki/Marxism) saw a resurgence in the form of [analytical Marxism](https://plato.stanford.edu/entries/marxism-analytical/). This approach offered a critique of capitalism largely grounded in the notion of exploitation with the rigor and toolset of analytic philosophy and microeconomic theory. The problem is that the [approach didn't pan out](https://en.wikipedia.org/wiki/Analytical_Marxism#Criticism): results were unconvincing and internal coherence was lacking.

Heath offers a amusing history (and lament) of this Marxist wave. He attributes the hastening of the crash to the competing [Rawlsian program](https://plato.stanford.edu/entries/rawls/#JusFaiJusWitLibSoc). While [A Theory of Justice](https://en.wikipedia.org/wiki/A_Theory_of_Justice) (1971) may seem boring in contrast to the high theory of Marxism, it offered a critique of unfettered capitalism from a liberal direction.

>What Rawls had provided, through his effort to “generalize and carry to a higher level of abstraction the familiar theory of the social contract,” was a natural way to derive the commitment to equality, as a normative principle governing the basic institutions of society. Rawlsianism therefore gave frustrated Marxists an opportunity to cut the Gordian knot, by providing them with a normative framework in which they could state directly their critique of capitalism, focusing on the parts that they found most objectionable, without requiring any entanglement in the complex apparatus of Marxist theory.

For more on Cold War Rationality, see S. M. Amadae's [Rationalizing Capitalist Democracy: The Cold War Origins of Rational Choice Liberalism]({{ site.baseurl }}{% link _posts/2021-12-31-top-books-2021.md %}#rationalizing-capitalist-democracy-the-cold-war-origins-of-rational-choice-liberalism) (2003), which made my books list in 2021.

## How the continuum hypothesis could have been a fundamental axiom
______

Author: [Joel David Hamkins](https://jdh.hamkins.org/)

Publication: [Journal for the Philosophy of Mathematics](https://riviste.fupress.net/index.php/jpm)

Published: 2024

Link: [arXiv](https://arxiv.org/abs/2407.02463)

The philosopher [Penelope Maddy](https://en.wikipedia.org/wiki/Penelope_Maddy) has argued that the axioms of set theory are in some sense [historically contingent]({{ site.baseurl }}{% link _posts/2021-12-15-top-articles-2021.md %}#believing-the-axioms-i). Hamkins builds on this line of thought by considering a plausible alternative history of calculus, where the continuum hypothesis is taken as an axiom. The [continuum hypothesis](https://en.wikipedia.org/wiki/Continuum_hypothesis) (CH) states that there is no set whose [cardinality](https://en.wikipedia.org/wiki/Cardinality) (or size) is strictly between that of the integers and the real numbers. 

From the standard [axioms of set theory (ZFC)](https://en.wikipedia.org/wiki/Zermelo–Fraenkel_set_theory), CH is independent, meaning that it can be neither proven nor disproven. The consistency of ZFC with CH was [proven by Kurt Gödel](https://plato.stanford.edu/entries/goedel/#ConConHypAxiCho) in 1938, and the consistency of ZFC with $\neg$CH was [proven by Paul Cohen](https://en.wikipedia.org/wiki/Paul_Cohen#Continuum_hypothesis) in 1963, inventing the technique of [forcing](https://en.wikipedia.org/wiki/Forcing_(mathematics)) along the way. While CH is formally independent of set theory, some hold that [it is nonetheless true](https://en.wikipedia.org/wiki/Continuum_hypothesis#Arguments_for_and_against_the_continuum_hypothesis) or that we should reason about a [multiverse](https://en.wikipedia.org/wiki/Multiverse_(set_theory)) of set theories.

<figure style="float: right; display: inline-block; margin: 10px 0px 0px 10px">
    <img width="250" height="250" src="/images/blog/interesting_articles_2024/newtonLeibniz.png"/>
    <figcaption style="text-align: center; font-size: 12px;">Newton and Leibniz settling their differences<br/>Credit: Joel David Hamkins</figcaption>
</figure>

The proposed alternate history begins with the development of [infinitesimal calculus](https://en.wikipedia.org/wiki/Calculus#Limits_and_infinitesimals) in the 17th century. Mathematicians were able to develop a rigorous foundation for this calculus in terms of [hyperreal numbers](https://en.wikipedia.org/wiki/Hyperreal_number). The hyperreals are an extension of the real numbers that include infinitesimals, numbers that are smaller than any positive real number but not zero and fill "every conceivable gap in the numbers". How does CH enter the picture? In ZFC, the hyperreals are underspecified; however, ZFC+CH implies a unique characterization of the hyperreals. Hamkins argues that this development could have led to the acceptance of CH as a fundamental axiom of set theory. 

A general worry about this sort of paper being simultaneously a high-level thought experiment and in the weeds of set theory is that subtly unsound reasoning may sneak in unnoticed. As someone familiar with these topics but not a set theorist, it took some time to digest this paper and verify results that were casually mentioned. 

## Charles Darwin and Associates, Ghostbusters
______

Author: [Richard Milner](https://en.wikipedia.org/wiki/Richard_Milner_(historian))

Publication: [Scientific American](https://en.wikipedia.org/wiki/Scientific_American)

Published: 1996

Link: [JSTOR](https://www.jstor.org/stable/24993409)

In the late nineteenth century, [spiritualism](https://en.wikipedia.org/wiki/Spiritualism_(movement)) was having a cultural moment, partly as a reaction to rapid progress in the sciences. As part of this progress, [evolutionary theory](https://en.wikipedia.org/wiki/History_of_evolutionary_thought) generated much controversy with its (largely) [materialist account of life and change]({{ site.baseurl }}{% link _posts/2024-11-22-research-from-1874.md %}#address-delivered-before-the-british-association-assembled-at-belfast). This short article describes an episode in the history of science when evolutionary theory collided with spiritualism in "one of the strangest courtroom cases in Victorian England."

<figure style="float: right; display: inline-block; margin: 0px 10px 0px 10px">
    <img width="200" height="200" src="/images/blog/interesting_articles_2024/seance.jpeg"/>
</figure>

In 1876, [Ray Lankester](https://en.wikipedia.org/wiki/Ray_Lankester), [Thomas Huxley's](https://en.wikipedia.org/wiki/Thomas_Henry_Huxley) lab assistant and a junior member of [Charles Darwin's](https://en.wikipedia.org/wiki/Charles_Darwin) circle, sought to debunk a purported psychic. Partly, this was to win the elder Darwin's favor as Darwin's brother-in-law, [Hensleigh Wedgwood](https://en.wikipedia.org/wiki/Hensleigh_Wedgwood), had recently been swept up in the seance fervor. Lankester and a friend confronted the American psychic [Henry Slade](https://en.wikipedia.org/wiki/Henry_Slade_(medium)) during a London event and later brought a complaint against him under "an old law intended to protect the public from traveling palm readers and sleight-of-hand artists." 

The trial was sensational. Lankester nearly botched the debunking by neglecting to identify Slade's slight-of-hand, provide any substantial evidence, or even consistent testimony. In addition, the proceedings featured a stage magician who demonstrated how Slade could have deceived his audience and testimony on the character of Slade from [Alfred Russel Wallace](https://en.wikipedia.org/wiki/Alfred_Russel_Wallace), an avowed spiritualist who also formulated natural selection independently of Darwin in the 1850s. The judgement went against Slade but would later be overturned. 

## A Watermark for Large Language Models
______

Author: [John Kirchenbauer](https://scholar.google.com/citations?user=48GJrbsAAAAJ&hl=en), [Jonas Geiping](https://scholar.google.de/citations?user=206vNCEAAAAJ&hl=de), [Yuxin Wen](https://scholar.google.com/citations?user=oUYfjg0AAAAJ&hl=en), [Jonathan Katz](https://en.wikipedia.org/wiki/Jonathan_Katz_(computer_scientist)), [Ian Miers](https://scholar.google.com/citations?user=21kN_WsAAAAJ&hl=en), and [Tom Goldstein](https://scholar.google.com/citations?user=KmSuVtgAAAAJ&hl=en)

Publication: [ICML Proceedings](https://en.wikipedia.org/wiki/International_Conference_on_Machine_Learning)

Published: 2023

Link: [arXiv](https://arxiv.org/abs/2301.10226)

The [idea of watermarking](https://en.wikipedia.org/wiki/Watermark) a physical image or document to prevent forgery has been around for centuries. For generating watermarked images from a model, this looks something like slightly perturbing the image in a way that's imperceptible to the human eye but detectable by the model owner. Doing something similar for language models poses a challenge because predicting the next word in a sentence offers dramatically less information to work with than all the pixels across channels in an image. 

<figure style="float: right; display: inline-block; margin: 10px 0px 0px 10px">
    <img width="300" height="225" src="/images/blog/neurips2024/watermark.png">
    <figcaption style="text-align: center; font-size: 12px;">"A Watermark for Large Language Models" <br/> Kirchenbauer et al. (2023)</figcaption>
</figure>

Over the past three years, several approaches to watermarking language models have been proposed. This paper introduces Green-Red Watermarking, where you randomly divide all tokens in the model's vocabulary into two sets: green and red. During inference, you slightly increase the probability of choosing a green token. The result is text that's detectible by the model owner by looking at the ratio of green to red tokens. Other approaches offer different trade-offs between the security of the watermark and the effect on the model's utility, including using [ideas from differential privacy](https://arxiv.org/abs/2402.05864). 

## On the reciprocal influence of the periodical publications, and the intellectual progress of this country
______

Author: [William Stevenson](https://en.wikipedia.org/wiki/William_Stevenson_(writer))

Publication: [Blackwood's Magazine](https://en.wikipedia.org/wiki/Blackwood%27s_Magazine)

Published: 1824

Link: [Google Books](https://www.google.com/books/edition/Blackwood_s_Edinburgh_Magazine/nuc6AQAAMAAJ?q=&gbpv=1#f=false)

One way to measure how the intellect of a country changes over time is to look at what's published in its periodicals. By intellect, Stevenson is not as much talking about scientific advancements as the overall quality of discourse. Looking back at the literature from the 1770s, Stevenson observed a dramatic rise in the quality of articles published in [London periodicals](https://en.wikipedia.org/wiki/List_of_18th-century_British_periodicals) over the fifty year period. Is published writing merely a reflection of changing intellect, or does causation go both ways? 

<figure style="float: right; display: inline-block; margin: 0px 0px 0px 15px">
    <img width="300" height="250" src="/images/blog/look_back/1824/eruption.jpeg">
    <figcaption style="text-align: center; font-size: 12px;"><a href="https://en.wikipedia.org/wiki/The_Eruption_of_Vesuvius">The Eruption of Vesuvius</a> (1821)<br/>by <a href="https://en.wikipedia.org/wiki/Johan_Christian_Dahl">Johan Christian Dahl</a> </figcaption>
</figure>

Stevenson finds the literature from fifty years prior to be a bit pedestrian with respect to both topics and quality relative to the writing of his day. One driver of this is the notion of a [moral convulsion](https://www.theatlantic.com/ideas/archive/2020/10/collapsing-levels-trust-are-devastating-america/616581/). This is an event that causes radical social upheaval and a reevaluation of one's moral landscape, which Stevenson compares to a volcano erupting and leaving fertile soil in its wake. During the time period in question, a moral convulsion was brought on by the [French Revolution](https://en.wikipedia.org/wiki/French_Revolution) and the resulting turmoil. 

How might periodicals influence the public intellect? Unlike books, periodicals often expose the reader to a variety of topics and the occasional gem of an article that might not have been sought out otherwise. In this way, ideas can diffuse through society. There are other avenues as well. As the number of published articles grew, [outlets specialized](https://en.wikipedia.org/wiki/List_of_19th-century_British_periodicals) to differentiate their collections and capture a specific audience. The resulting exclusivity increased both the prestige and utility of publishing one's writing in this format, leading brighter minds to contribute to periodicals. 

On this latter point, I couldn't help but think that today we've seen some harmful effects emerge from this process of specialization insofar as the public intellect becomes fractured into [echo chambers](https://aeon.co/essays/why-its-as-hard-to-escape-an-echo-chamber-as-it-is-to-flee-a-cult), [cognitive islands](https://www.foreignaffairs.com/world/spirals-delusion-artificial-intelligence-decision-making), and [epistemic bubbles](https://www.cambridge.org/core/journals/episteme/article/abs/echo-chambers-and-epistemic-bubbles/5D4AC3A808C538E17C50A7C09EC706F0). Regardless, this article lays out a strong case for why one should read periodicals, both then and now, and especially broader interest magazines such as [The Atlantic](https://en.wikipedia.org/wiki/The_Atlantic) and [Harper's](https://en.wikipedia.org/wiki/Harper's_Magazine).

## The Deaths of Effective Altruism
______

Author: [Leif Wenar](https://en.wikipedia.org/wiki/Leif_Wenar)

Publication: [Wired](https://en.wikipedia.org/wiki/Wired_(magazine))

Published: 2024

Link: [Click Here](https://www.wired.com/story/deaths-of-effective-altruism/)

This article chronicles the rise of [effective altruism](https://en.wikipedia.org/wiki/Effective_altruism) from the perspective of a philosopher who had similar aspirations in the 1990s. The cinematic synopsis:

>The EA saga is not just a modern fable of corruption by money and fame, told in exaflops of computing power. This is a stranger story of how some small-time philosophers captured some big-bet billionaires, who in turn captured the philosophers—and how the two groups spun themselves into an opulent vortex that has sucked up thousands of bright minds worldwide.

Effective altruism began with the combination of [Peter Singer's](https://en.wikipedia.org/wiki/Peter_Singer) [shallow pond argument](https://en.wikipedia.org/wiki/Famine,_Affluence,_and_Morality) and quantified analyses of the effectiveness of charities in saving lives. [Toby Ord](https://en.wikipedia.org/wiki/Toby_Ord) is a philosopher who pushed in this direction in the 2000s. In the 2010s came [William MacAskill](https://en.wikipedia.org/wiki/William_MacAskill), who was more pitchman than philosopher. An amusing passage:

>Let me give a sense of how bad MacAskill’s philosophizing is. Words are the tools of the trade for philosophers, and we’re pretty obsessive about defining them. So you might think that the philosopher of effective altruism could tell us what "altruism" is. MacAskill says, "I want to be clear on what "altruism" means. As I use the term, _altruism_ simply means improving the lives of others." No competent philosopher could have written that sentence. Their flesh would have melted off and the bones dissolved before their fingers hit the keyboard.

Effective altruism mingled with other [pseudointellectual online communities]({{ site.baseurl }}{% link _posts/2023-12-31-interesting-articles-2023.md %}#rational-magic) and exhibited similar poor reasoning:

>Strong hyping of precise numbers based on weak evidence and lots of hedging and fudging. EAs appoint themselves experts on everything based on a sophomore’s understanding of rationality and the world. And the way they test their reasoning—debating other EAs via blog posts and chatboards—often makes it worse. Here, the basic laws of sociology kick in. With so little feedback from outside, the views that prevail in-group are typically the views that are stated the most confidently by the EA with higher status. EAs rediscovered groupthink.

By the late 2010s, effective altruism adopted parts of [longtermism](https://aeon.co/essays/why-longtermism-is-the-worlds-most-dangerous-secular-credo). In some sense, longtermism is EA's final form:

>Longtermism lays bare that the EAs’ method is really a way to maximize on looking clever while minimizing on expertise and accountability.

Importantly, Wenar is not claiming that charity is not effective. Rather, the point is that any sort of intervention has both positive and negative effects. A better approach to charitable giving would be to be as transparent as possible about all known effects. 

## Poetry and Philosophy
______

Author: [Arthur Cecil Pigou](https://en.wikipedia.org/wiki/Arthur_Cecil_Pigou)

Publication: [The Contemporary Review](https://en.wikipedia.org/wiki/The_Contemporary_Review)

Published: 1924

Link: [Google Books](https://www.google.com/books/edition/The_Contemporary_Review/GTkeAQAAIAAJ?hl=en&gbpv=1&pg=PA735&printsec=frontcover)

There is an apparent tension between philosophical and poetic attitudes: philosophy prizes truth to the detriment of beauty, while poetry seeks to stir emotion without regard for reason. This article reflects on the degree to which the poetic strays one from the truth. 

<figure style="float: right; display: inline-block; margin: 10px 0px 0px 15px">
    <img width="225" height="225" src="/images/blog/interesting_articles_2024/pigou.png">
    <figcaption style="text-align: center; font-size: 12px;">An ink portrait of Pigou<br/> from the Online Library of Liberty</figcaption>
</figure>

While poetry cannot do all of the heavy lifting of philosophy, Pigou finds a place for poetry in his view of [the epistemic regress](https://iep.utm.edu/epi-just/#SH1a). Being a strong [foundationalist](https://iep.utm.edu/foundationalism-in-epistemology/) (as was common at the time), Pigou holds that there are two sorts of beliefs or propositions: those inferentially justified and those immediately justified. The former are the stuff of philosophy, logic, mathematics, and the sciences: the *this* in this follows from that. The latter can be more ephemeral and is the stuff of metaphysics, foundations, methodology, and moral philosophy. 

The poetic mode can provide data to support or frame which beliefs are justified immediately. Another place for poetry concerns how hypotheses or positions are discovered rather than their ultimate logical justification. Philosophers of science refer to these as the [context of discovery](https://plato.stanford.edu/entries/scientific-discovery/) and the [context of justification](https://link.springer.com/referenceworkentry/10.1007/978-94-007-2150-0_239). 

Poetry and Philosophy is an excellent companion to [C. P. Snow's](https://en.wikipedia.org/wiki/C._P._Snow) [The Two Cultures](https://en.wikipedia.org/wiki/The_Two_Cultures) (1959), since it provides a model of how the humanities and sciences can be complementary endeavors. I discuss Pigou's paper in my [survey of research from 1924]({{ site.baseurl }}{% link _posts/2024-07-07-research-from-1924.md %}). 
