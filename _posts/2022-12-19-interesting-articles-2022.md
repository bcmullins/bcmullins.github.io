---
layout: post_top
title: Interesting Articles I've Read in 2022
categories: Review
mathjax: true
---

Below is a collection of interesting articles I've read in 2022. There are two papers in differential privacy: [A Better Privacy Analysis of the Exponential Mechanism](#a-better-privacy-analysis-of-the-exponential-mechanism) and [Differentially Private Approximate Quantiles](#differentially-private-approximate-quantiles). There's an article in the history of mathematical philosophy and a survey introduction to an area of logic: [The introduction of topology into analytic philosophy](#the-introduction-of-topology-into-analytic-philosophy-two-movements-and-a-coda) and [Incomplete and Utter Introduction to Modal Logic](#incomplete-and-utter-introduction-to-modal-logic). Two papers border on the practical side of the philosophy of science: [Stylized Facts in the Social Sciences](#stylized-facts-in-the-social-sciences) for social science research and [Does Academic Research Destroy Stock Return Predictability?](#does-academic-research-destroy-stock-return-predictability) for finance.[The World Putin Wants](#the-world-putin-wants-how-distortions-about-the-past-feed-delusions-about-the-future) discusses Russia's rhetoric from the war in Ukraine. To round out the collection, we explore the influence of a wayward early 20th century archaeologist, build a simple mathematical model of tennis, ponder whether NLP models have intentional states, and consider the role of private property among early humans.



## Stylized Facts in the Social Sciences
______

Author: Daniel Hirschman

Publication: [Sociological Science](https://sociologicalscience.com/)

Published: 2016

Link: [Click here](https://sociologicalscience.com/articles-v3-26-604/)

Stylized facts are "empirical regularities in search of theoretical, causal explanations." Hirschman presents a model of social science research where empirical researchers produce stylized facts that then become the data to which theoreticians model, thereby filling the role of phenomena and [crucial experiments](https://en.wikipedia.org/wiki/Experimentum_crucis) in the natural or experimental sciences. Some prominent examples of stylized facts include
>["Democracies rarely go to war with each other"](https://www.cambridge.org/core/journals/american-political-science-review/article/abs/no-rest-for-the-democratic-peace/0E76DD4F5B7C36779473C211D29826FE); <br/>
["The share of income going to the top 1 percent in the United States doubled since 1980"](https://academic.oup.com/qje/article-abstract/118/1/1/1917000?redirectedFrom=fulltext); <br/>
["Nations with debt-to-GDP ratios in excess of 90 percent experience lower GDP growth."](https://www.aeaweb.org/articles?id=10.1257/aer.100.2.573)

Hirschman identifies four fundamental properties of stylized facts: they make ontological claims about the social world; they are often presented both in technical and lay terms; they frequently posit non-robust or associational relationships; and they serve as normative claims on how best to summarize the findings of a data analysis or to contribute to such-and-such debate. As the above examples illustrate, stylized facts need not be true (or general) and are often used (and abused) in policy debates.

In my view, this an exemplary philosophy of science paper which sheds light on actual scientific practice. In particular, this paper caused me to reflect my work on [measuring income mobility]({{ site.baseurl }}{% link research.md %}#earnings-mobility-and-snap-participation-in-georgia). For instance, one way to frame the analysis in [Earnings Mobility and the Great Recession](http://127.0.0.1:4000/earnings-mobility-great-recession/) is that we proffer the stylized fact that "among low-wage workers, earnings mobility increased following the Great Recession" and our follow-up analysis attempts to explain this finding.

## The World Putin Wants: How Distortions About the Past Feed Delusions About the Future
______

Authors: Fiona Hill and Angela Stent

Publication: [Foreign Affairs](https://www.foreignaffairs.com/)

Published: 2022

Link: [Click here](https://www.foreignaffairs.com/russian-federation/world-putin-wants-fiona-hill-angela-stent)

In July 2021, Vladimir Putin [published an essay](https://en.wikipedia.org/wiki/On_the_Historical_Unity_of_Russians_and_Ukrainians) presenting a suspect history of Russian relations with Ukraine as well as questioning Ukrainian sovereignty, which [some analysts](https://www.theguardian.com/world/2021/dec/07/putins-ukraine-rhetoric-driven-by-distorted-view-of-neighbour) took as a pretext for an invasion. [Such an invasion](https://en.wikipedia.org/wiki/2022_Russian_invasion_of_Ukraine) came in February 2022 and is ongoing at the time of writing. This article analyzes Russia's rhetoric and strategy in the context of Putin's essay and his other writings and speeches. The thrust of the argument is that "Putin seeks to build his version of a Russian empire."

<img style="float: right; margin: 0px 0px 5px 5px;" src="https://cdn-live.foreignaffairs.com/sites/default/files/styles/_webp_large_1x/public/images/2022/09/02/Snyder_art2_0.jpg.webp?itok=qn21-Fmu" width="350" height="250">

While I've seen several interesting articles on Ukraine, including much great reporting, I found that Hill and Stent's article best explains the rhetorical grounds for the invasion. Here is a [conversation between the authors](https://www.brookings.edu/essay/putins-war-in-ukraine-a-conversation-with-fiona-hill-and-angela-stent/) from the Brookings Institute. Two other articles in a similar vein are Timothy Snyder's [Ukraine Holds the Future](https://www.foreignaffairs.com/ukraine/ukraine-war-democracy-nihilism-timothy-snyder) in Foreign Affairs and [Russia's Pseudo-Intellectuals](https://www.americanpurpose.com/articles/russias-pseudo-intellectuals/) in Francis Fukuyama's American Purpose.

This article appeared in the centennial issue of Foreign Affairs. Earlier this year, I looked back at [the magazine's first issue]({{ site.baseurl }}{% link _posts/2022-08-15-foreign-affairs-100.md %}) from Fall 1922.

## A Better Privacy Analysis of the Exponential Mechanism
______

Authors: Ryan Rogers and Thomas Steinke

Publication: [DifferentialPrivacy.org](https://differentialprivacy.org)

Published: 2021

Link: [Click here](https://differentialprivacy.org/exponential-mechanism-bounded-range/)

Private selection is a fundamental task in [differential privacy](https://en.wikipedia.org/wiki/Differential_privacy) where, given a collection of options and a score for each option calculated on a dataset, one chooses the approximately best option while limiting [disclosure risk](http://www.ihsn.org/anonymization-risk-measure) for records in the dataset.

This blog post summarizes recent research on the [Exponential mechanism](https://en.wikipedia.org/wiki/Exponential_mechanism) - the most common algorithm for private selection - and conversions between [DP variants](https://programming-dp.com/ch8.html). A common workflow for designing complex differentially private algorithms is to first prove that the simple component algorithms satisfy a common DP variant with nice properties for one's application such as [Concentrated Differential Privacy](https://programming-dp.com/ch8.html#zero-concentrated-differential-privacy), then convert the combined algorithm to a more interpretable and prevalent DP notion such as [Approximate Differential Privacy](https://programming-dp.com/ch6.html).  

The primary result discussed is an efficient conversion of Exponential mechanism to Concentrated Differential Privacy that improves on the best known result by a factor of 4. This is significant, since it allows for more accurate results while providing the same privacy guarantee. This result is used in my recent work designing [differentially private synthetic data algorithms]({{ site.baseurl }}{% link _posts/2022-03-20-aim-synthetic-data.md %}).

## The introduction of topology into analytic philosophy: two movements and a coda
______

Authors: Samuel C. Fletcher and Nathan Lackey

Publication: [Synthese](https://en.wikipedia.org/wiki/Synthese)

Published: 2022

Link: [Click here](https://link.springer.com/article/10.1007/s11229-022-03689-9)

During the 20th century two distinct conceptions of topology found their way into philosophical discourse: geometric and algebraic.

<img style="float: right; margin: 0px 0px 5px 10px" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/Highest_resolution_image_of_the_1919_solar_eclipse.tif/lossy-page1-1920px-Highest_resolution_image_of_the_1919_solar_eclipse.tif.jpg" width="300" height="200">

The geometric conception is largely concerned with defining notions of points, events, and basic observations in space-time given the backdrop of [relativity theory](https://en.wikipedia.org/wiki/Theory_of_relativity) and [logical atomism](https://en.wikipedia.org/wiki/Logical_atomism). The authors contend that the geometric conception entered into philosophy as a reaction to Einstein's theory rising to prominence following the [1919 Eddington experiments](https://en.wikipedia.org/wiki/Eddington_experiment). For instance, in the early 20th century, both [Bertrand Russell](https://plato.stanford.edu/entries/russell/) and [Rudolf Carnap](https://plato.stanford.edu/entries/carnap/) were working on empiricism and the foundations of physics but only employed topological reasoning following the widespread adoption of general relativity. Later, the geometric conception of topology found additional application in [mereology](https://plato.stanford.edu/entries/mereology/), providing a useful language to express [formal ontologies](https://en.wikipedia.org/wiki/Formal_ontology).

The algebraic conception employs the correspondence between topology and logic stemming from results such as [Stone's representation theorem](https://en.wikipedia.org/wiki/Stone%27s_representation_theorem_for_Boolean_algebras). One thread of this conception studies [topological semantics for logics](#incomplete-and-utter-introduction-to-modal-logic) such as modal and intuitionistic logics. A second thread is [topological learning theory]({{ site.baseurl }}{% link _posts/2020-12-29-interesting-research-2010s.md %}#topological-learning-theory) which studies the learnability of hypotheses where the difficulty (or simplicity) of learning a hypothesis corresponds to the topological complexity of the hypothesis over the space of possible observation histories.

## A Geometric Series from Tennis
______

Author: Michael K. Kinyon

Publication: [The College Mathematics Journal](https://en.wikipedia.org/wiki/The_College_Mathematics_Journal)

Published: 2005

Link: [Click here](https://fermatslibrary.com/s/a-geometric-series-from-tennis)

This is a short, fun article exploring the probability of winning a game in tennis if the probability $p$ of winning a point is known. After a bit of reflection and combinatorics, this probability can be represented as a [geometric series](https://en.wikipedia.org/wiki/Geometric_series) to account for indefinite deuce/advantage point pairs. Solving for this probability is an excellent application of geometric series to everyday life.

The author takes the analysis an additional step by observing that this probability is non-linear and symmetric about $0.5$ as a function of $p$. Since $0.5$ is an [inflection point](https://en.wikipedia.org/wiki/Inflection_point), the gains in the probability of winning a game are much higher when improving against an evenly matched opponent than against a much better or much worse opponent.

In reading this, I am reminded of [Pick the Largest Number]({{ site.baseurl }}{% link _posts/2018-12-16-Top-Articles-2018.md %}#pick-the-largest-number), both of which were featured in [Fermat's Library Journal Club](https://fermatslibrary.com/journal_club).

## Does Academic Research Destroy Stock Return Predictability?
______

Authors: R. David McLean and Jeffrey Pointiff

Publication: [The Journal of Finance](https://en.wikipedia.org/wiki/The_Journal_of_Finance)

Published: 2016

Link: [Click here](https://onlinelibrary.wiley.com/doi/abs/10.1111/jofi.12365)

This paper estimates the effect of publishing investing strategies in academic papers on the performance of those strategies. The authors limit the study to [long-short equity strategies](https://en.wikipedia.org/wiki/Long/short_equity) that only use publicly available cross-sectional data i.e. observe prices at time $t$ to predict prices at time $t+1$. Data is gathered by reimplementing nearly one hundred proposed strategies and generating performance of the strategy within the initial sample period (in-sample), out of sample but prior to publication (out-sample), and post-publication. Note though that not all strategies could be implemented as originally described due to vagaries, changes to publicly available data, etc.

The idea is that the in-sample performance can be decomposed into generalization error (the paper calls this statistical bias), post-publication performance, and the effect of other traders using the same strategy post publication.
>"We estimate the effect of statistical bias to be about 26%. This is an upper bound, because some investors could learn about a predictor while the study is still a working paper. The average predictor’s return declines by 58% post-publication. We attribute this post-publication effect both to statistical biases and to the price impact of sophisticated traders. Combining this finding with an estimated statistical bias of 26% implies a publication effect of 32%."

An excellent complement to this paper is [An Engine, Not a Camera](https://mitpress.mit.edu/9780262633673/an-engine-not-a-camera/). Also, the authors should be commended for the tremendous amount of work that must have went into this paper.

## Witches and Aliens: How an Archaeologist Inspired Two New Religious Movements
______

Author: Jeb J. Card

Publication: [Nova Religio: The Journal of Alternative and Emergent Religions](https://online.ucpress.edu/nr)

Published: 2019

Link: [Click here](https://online.ucpress.edu/nr/article-abstract/22/4/44/71226/Witches-and-AliensHow-an-Archaeologist-Inspired)

The late-19th/early-20th century archaeologist [Margaret Murray](https://en.wikipedia.org/wiki/Margaret_Murray) greatly influenced both fringe religious movements and science fiction. Murry was a prominent [Egyptologist](https://en.wikipedia.org/wiki/Egyptology) at University College London and was key in training a generation of Egyptologists.

Beginning with [The Witch-Cult in Western Europe](https://en.wikipedia.org/wiki/The_Witch-Cult_in_Western_Europe) in 1921, Murry turned her attention to developing and popularizing the idea that "historical and folkloric accounts of witches are memories of an ancient persecuted religion, the Old Religion, dating back to the Pleistocene period." The so-called ["Witch-Cult hypothesis"](https://en.wikipedia.org/wiki/Witch-cult_hypothesis) had antecedents such as with the statistician [Karl Pearson](https://en.wikipedia.org/wiki/Witch-cult_hypothesis#Michelet,_Gage,_and_Leland); however, its cultural influence greatly grew with Murry. Unfortunately, much of Murry's evidence consists of a [tortured interpretation of the witch trials](https://en.wikipedia.org/wiki/The_Witch-Cult_in_Western_Europe#Interpretation_of_witch_trial_evidence) in Europe in the late Middle Ages with a dash of [alternative archaeology](https://en.wikipedia.org/wiki/Pseudoarchaeology).

Murry's later writing claimed that secret Old Religion cults were still in practice which directly influenced the founding of [Gardnerian Wicca](https://en.wikipedia.org/wiki/Wicca#%22Witchcraft%22_and_%22Wicca%22). This, in turn, lead to the spread of Wicca groups and the Neo-pagan movement which is still alive today.

A second thread of influence came through the science fiction writer [H.P. Lovecraft](https://en.wikipedia.org/wiki/H._P._Lovecraft) whose writing incorporated themes of secret cults and such following reading Murry in 1923. Lovecraft explicitly mentions Murry's "Witch-Cult" in both [The Horror at Red Hook](https://en.wikipedia.org/wiki/The_Horror_at_Red_Hook) and [The Call of Cthulhu](https://en.wikipedia.org/wiki/The_Call_of_Cthulhu).

## Talking About Large Language Models
______

Authors: Murray Shanahan

Published: 2022

Link: [Click here](https://arxiv.org/abs/2212.03551)

Fall 2022 saw an increase in public interest in the latest round of [generative NLP models](https://en.wikipedia.org/wiki/Language_model) often called large language models (LLMs). This timely article argues that researchers and practitioners ought to be cautious when assigning [intentional states]((https://plato.stanford.edu/entries/intentionality/)) such as knowledge and belief to LLMs. Shanahan's observation is not novel but is worth considering: while LLMs can have really impressive performance for some tasks, they "simply generate sequences of words that are statistically likely follow-ons from a given prompt." So LLMs don't reason like humans and, therefore, cannot be ascribed intentional states.

<img style="float: right; margin: 0px 0px 5px 5px;" src="https://upload.wikimedia.org/wikipedia/en/d/db/Clippy-letter.PNG
" width="125" height="250">

Assigning intentional states as shorthand is a common practice across many fields. For instance, ask any logician to read "$\mathcal{M} \models \varphi$" and they'll likely say "$\mathcal{M}$ thinks $\varphi$". Yet I venture that not many think that a model of arithmetic actually thinks. Matters are more tricky for NLP models and systems, since they are meant to mimic a human mode of communication. The difficulties with anthropomorphizing models can vary by domain as well. For instance, it seems much more reasonable to say that a [bounding-box computer vision model]({{ site.baseurl }}{% link _posts/2020-12-29-interesting-research-2010s.md %}#image-recognition-and-object-detection) "looks" than that [ChatGPT](https://openai.com/blog/chatgpt/) "thinks".

## Incomplete and Utter Introduction to Modal Logic
______

Author: Danya Rogozin

Published: 2019/2020

Link: [Click here](https://serokell.io/blog/incomplete-and-utter-introduction-to-modal-logic)

A [modal logic](https://plato.stanford.edu/archives/sum2021/entries/logic-modal/) is a formal system modeling deduction for modal expressions i.e. expressions that include truth value qualifiers. For instance, in standard propositional logic, sentences are formed by combining propositional variables $P, Q, R, \ldots$ with operators $\lor, \land, \neg, \rightarrow$ representing or, and, negation, and the [material conditional](https://en.wikipedia.org/wiki/Material_conditional). A modal propositional logic adds additional operators representing truth qualifiers such as "it is necessary that...", "it is possible that...", "it will be the case that...", "it is permissible that...", and so on.

Rogozin's article is an ambitious introduction to modal propositional logic in two parts. After a brief history and mathematical background, the first part develops the syntax and typical semantics ([Kripke semantics](https://en.wikipedia.org/wiki/Kripke_semantics)) for propositional modal logics. Whereas the first part surveys basic ideas in modal logic, the sequel dives into applications. The one I find most interesting is an alternative semantics (topological semantics) which interprets formulas in a modal logic in terms of the open and closed sets of a [topological space](https://en.wikipedia.org/wiki/Topological_space). Moreover, imposing various structure on topological spaces corresponds to changing the expressivity of the logic. An open area of research involves identifying which structural properties correspond to which modal logics. See [this paper](http://individual.utoronto.ca/philipkremer/onlinepapers/QS4rationals.pdf) for an example.

The prospective reader should note that the article contains quite a few typos and formatting errors. While it is rough around the edges, it reads as a labor of love that's well informed and bursting with enthusiasm.

## Primitive Communism: The idea of primitive communism is as seductive as it is wrong
______

Author: Manvir Singh

Publication: [Aeon](https://en.wikipedia.org/wiki/Aeon_(magazine))

Published: 2022

Link: [Click here](https://aeon.co/essays/the-idea-of-primitive-communism-is-as-seductive-as-it-is-wrong)

This article argues against [primitive communism](https://en.wikipedia.org/wiki/Primitive_communism): that early human tribes didn't have private property. This view can be found in many classical economists [in some form](https://en.wikipedia.org/wiki/Noble_savage) and is most closely associated with [Karl Marx](https://plato.stanford.edu/entries/marx/) from his posthumous [The Origin of the Family, Private Property and the State](https://en.wikipedia.org/wiki/The_Origin_of_the_Family,_Private_Property_and_the_State).  Singh describes Marx's book as an early entry in [big history](https://en.wikipedia.org/wiki/Big_History). Much field work in anthropology demonstrates that there's a wide range of behaviors in primitive societies and some form of private property is almost always present. The [Open Society & Its Complexities]({{ site.baseurl }}{% link _posts/2021-12-31-top-books-2021.md %}#the-open-society-and-its-complexities) - from last year's book list - covers similar ground in great detail.

The author leaves us with the following quote:
>"The popularity of the idea of primitive communism, especially in the face of contradictory evidence, tells us something important about why narratives succeed. Primitive communism may misrepresent forager societies. But it is simple, and it accords with widespread beliefs about the arc of human history. If we assume that societies went from small to big, or from egalitarian to despotic, then it makes sense that they transitioned from property-less harmony to selfish competition, too. Even if the facts of primitive communism are off, the story feels right...By drawing a contrast between an angelic past and our greedy present, primitive communism blinds us to the true determinants of trust, freedom and equity. If we want to build better societies, the way forward is neither to live as hunter-gatherers nor to bang the drum of a make-believe state of nature. Rather, it is to work with humans as they are, warts and all."

## Differentially Private Approximate Quantiles
______

Authors: Haim Kaplan, Shachar Schnapp, and Uri Stemmer

Publication: [Proceedings of the 39th International Conference on Machine Learning](https://proceedings.mlr.press/v162/)

Published: 2021

Link: [Click here](https://arxiv.org/abs/2110.05429#)

This paper presents a recursive schema for computing multiple [differentially private](https://en.wikipedia.org/wiki/Differential_privacy) quantile estimates. Given an ordered list of [quantiles](https://en.wikipedia.org/wiki/Quantile) and a differentially private mechanism for computing a single quantile (they use [this one from Adam Smith (2011)](https://dl.acm.org/doi/abs/10.1145/1993636.1993743) based on the [exponential mechanism](https://en.wikipedia.org/wiki/Exponential_mechanism_(differential_privacy))), this schema proceeds by first computing the middle quantile, then splitting the data domain into two sub-problems based on the middle quantile estimate, and repeating until all quantiles estimates are computed.

<img style="float: right;" src="/images/blog/interesting_articles_2022/dp_approx_quantiles.png" width="350" height="250">

With differential privacy, each time an algorithm accesses the data to compute a value, measure error, and so forth, it incurs a [privacy cost](https://www.johndcook.com/blog/2019/10/14/privacy-budget/). An interesting property of differential privacy called [parallel composition](https://programming-dp.com/notebooks/ch4.html#parallel-composition) says that if an algorithm does the same operation on each member of a partitioned dataset, it only incurs the privacy cost once. So this schema only pays the privacy cost once each round.

Computationally, differentially private quantile algorithms typically scale with the size of the dataset. Since the data domain gets progressively divied up with each round, the quantile algorithms speed up each round.
