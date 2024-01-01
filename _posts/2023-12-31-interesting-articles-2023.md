---
layout: post_top
title: Interesting Articles I've Read in 2023
categories: Review
mathjax: true
---
Below is a collection of interesting articles I've read in 2023. Several papers focus on foundations or methodology ranging from [mathematical logic](#what-do-we-want-a-foundation-to-do-comparing-set-theoretic-category-theoretic-and-univalent-approaches) and [history](#clues-margins-and-monads-the-micro-macro-link-in-historical-research) to [causal inference](#identification-and-estimation-of-local-average-treatment-effects). Two papers look like [jokes](#can-a-good-philosophical-contribution-be-made-just-by-asking-a-question) or [hoaxes](#every-author-as-first-author) but are insightful in the end. We consider the history of [women in analytic philosophy](#analytic-women-the-lost-women-of-early-analytic-philosophy) and the [first law and economics](#the-first-great-law--economics-movement) program from the early 20th century. There is a primer on [synthetic data for policymakers](#synthetic-data-and-public-policy-supporting-real-world-policymakers-with-algorithmically-generated-data) and a short look at working with the [pseudoinverse for highly structured matrices](#particular-formulae-for-the-moorepenrose-inverse-of-a-columnwise-partitioned-matrix). Finally, we survey a [scuffle between internet subcultures](#rational-magic) and consider [income inequality globally](#the-great-convergence-global-equality-and-its-discontents).

If you have some thoughts on my list or would like to share yours, send me an email at brettcmullins(at)gmail.com. Enjoy the list!

<!-- 

## title
______

Author: 

Publication: 

Published: 

Link: 

-->

## What do we want a foundation to do? Comparing set-theoretic, category-theoretic, and univalent approaches
______

Author: [Penelope Maddy](https://en.wikipedia.org/wiki/Penelope_Maddy)

In the collection [Reflections on the Foundations of Mathematics: Univalent Foundations, Set Theory and General Thoughts](https://link.springer.com/book/10.1007/978-3-030-15655-8)

Published: 2019

Link: [Springer](https://link.springer.com/chapter/10.1007/978-3-030-15655-8_13)

[Set theory](https://plato.stanford.edu/entries/set-theory/) is the usual foundation for mathematics. It fills this role since most of mathematics is formalizable in the language of sets and it provides enough structure to reason about metamathematical propositions. In the latter half of the 20th century, [category theory](https://plato.stanford.edu/entries/category-theory/) emerged as a possible competitor and, in the 2010s, [homotopy type theory](https://en.wikipedia.org/wiki/Homotopy_type_theory) entered the fray. This article discusses the notion of a foundation for mathematics and what sort of things we expect a foundation to do. Maddy argues that the three candidate notions satisfy different foundational virtues but should be understood more as differing perspectives rather than direct rivals. 

<a href = "http://settheory.net"> <img style="float: right; display: inline-block; margin: 10px 10px 10px 10px" width="40%" height="40%" src="http://settheory.net/foundingcycle.png"> </a>

Set theory satisfies several foundational virtues. Set theory is a generous arena by being flexible enough to express most of mathematics. Similarly, it acts as a shared standard, since we can import results from one area of mathematics to another without too much worry. Finally, it acts as a metamathematical corral by being expressive enough to allow for metamathematical analysis. For instance, using [large cardinal axioms](https://en.wikipedia.org/wiki/Large_cardinal) of increasing strength, we can measure the [relative consistency](https://en.wikipedia.org/wiki/Equiconsistency) of a theory to assess risk of inconsistency.

Category theory developed in the 1940s from work in algebraic geometry and algebraic topology, and, in the 1960s, some viewed category theory as a [plausible alternative foundation](https://plato.stanford.edu/entries/category-theory/#BrieHistSket) to set theory. Maddy dismisses the notion that category theory can fill the same roles as set theory; however, category theory does have the benefit of providing essential guidance for practitioners. Whereas set theory can be overly expressive with models containing useless constructions, category theory provides a framework to better guide the practitioner in algebraic fields. Interestingly, the virtue of essential guidance seems to conflict with generous arena. 

Homotopy type theory or univalent foundations emerged from homotopy theory and type theory in the 2010s. Maddy argues that it's not clear which of the roles homotopy type theory satisfies other than a new role: proof checking. Homotopy type theory is set up to be integrated with [formal verification](https://en.wikipedia.org/wiki/Formal_verification) software such as [Coq](https://en.wikipedia.org/wiki/Coq_(software)). Providing essential guidance and proof checking are helpful properties that will benefit mathematicians alongside the roles filled by set theory. Maddy closes with 

>"there’s no conflict between set theory continuing to do its traditional foundational jobs while these newer theories explore the possibility of doing others."

## Clues, Margins, and Monads: The Micro-Macro Link in Historical Research
______

Author: [Matti Peltonen](http://microhistory.eu/members/matti_peltonen.html)

Publication: [History and Theory](https://en.wikipedia.org/wiki/History_and_Theory)

Published: 2001

Link: [JSTOR](https://www.jstor.org/stable/2677970)

[Microhistory](https://en.wikipedia.org/wiki/Microhistory) emerged in the 1970s with case studies such as [Carlo Ginzburg's](https://en.wikipedia.org/wiki/Carlo_Ginzburg) [The Cheese and the Worms: The Cosmos of a Sixteenth-Century Miller](https://en.wikipedia.org/wiki/The_Cheese_and_the_Worms) (1975). The idea of this approach was not just to zoom in on an unusual and interesting region, quarrel, or figure, but to use this instance to infer unacknowledged or unrecorded events or trends. The Cheese and the Worms follows the exploits of a heretical sixteenth century Italian miller called [Menocchio](https://en.wikipedia.org/wiki/Menocchio) who argued for his unorthodox views in the ecclesiastical courts only to face the wrath of the counter-reformation. Ginzburg takes Menocchio's beliefs as evidence of a deeply-held peasant religion that had not been well-recorded. 

<img style="float: right; display: inline-block; margin: 0px 0px 0px 10px" width="25%" height="25%" src="https://upload.wikimedia.org/wikipedia/en/7/7a/The_Cheese_and_the_Worms.jpg">

This approach to history seeks to identify these "clues" which are "taken as a sign of a larger, but hidden or unknown, structure. A strange detail is made to represent a wider totality." In this way, observation of the micro leads to inferences about the macro. Peltonen surveys similar approaches to Ginzburg including [Giovanni Levi's](https://en.wikipedia.org/wiki/Giovanni_Levi) approach to clues, [Walter Benjamin's](https://en.wikipedia.org/wiki/Walter_Benjamin) monads, and [Michel de Certeau's](https://en.wikipedia.org/wiki/Michel_de_Certeau) margins among others. 

Peltonen contrasts microhistory with the adoption of [microfoundations](https://en.wikipedia.org/wiki/Microfoundations) in social science models in the 1970s, best exemplified by the [Lucas critique](https://en.wikipedia.org/wiki/Lucas_critique). Echoing a common critique of microfoundations, Peltonen notes that such models reduce all macroeconomic behavior to the interaction of microeconomic agents without inferring back to the macro state.  

## Particular formulae for the Moore–Penrose inverse of a columnwise partitioned matrix
______

Authors: [Jerzy K. Baksalary](https://en.wikipedia.org/wiki/Jerzy_Baksalary) and [Oskar Maria Baksalary](https://dblp.org/pid/85/7316.html)

Publication: [Linear Algebra and Its Applications](https://en.wikipedia.org/wiki/Linear_Algebra_and_Its_Applications)

Published: 2007

Link: [Click here](https://www.sciencedirect.com/science/article/pii/S0024379506001959)

This paper proves results for computing the [Moore-Penrose pseudoinverse](https://en.wikipedia.org/wiki/Moore–Penrose_inverse) of horizontal [block matrices](https://en.wikipedia.org/wiki/Block_matrix) i.e. matrices of the form $A = [A_1 \ A_2]$. In the general case, computing the pseudoinverse of $A$, denoted $A^+$, doesn't take advantage of $A$'s block structure. The authors prove useful results to utilize this structure.

The most useful result shows that the pseudoinverse distributes over the blocks when the blocks are [orthogonal](https://textbooks.math.gatech.edu/ila/projections.html). That is $A^+ = [A_1^+ \ A_2^+]^T$. The intuition is that mutually orthogonal matrices express different information. This result is similar to reasoning about the probability of independent events. To calculate the probability of two coin flips landing heads, you only need to know the probability that each lands heads. Similarly, to compute the pseudoinverse of a horizontal block matrix of mutually orthogonal blocks, you only need to know the pseudoinverses of the individual blocks.

## Every Author as First Author
______

Authors: [Erik D. Demaine](https://en.wikipedia.org/wiki/Erik_Demaine) and [Martin L. Demaine](https://en.wikipedia.org/wiki/Martin_Demaine)

Publication: [Proceedings of SIGTBD](http://sigtbd.csail.mit.edu/#home)

Published: 2023

Link: [arXiv](https://arxiv.org/abs/2304.01393)

I've always held that the best spoofs are also effective entries in their respective genre. For instance, [Scream](https://en.wikipedia.org/wiki/Scream_(1996_film)) is not just [Wes Craven](https://en.wikipedia.org/wiki/Wes_Craven) poking fun at tropes of the slasher film; it is itself an effective slasher! 

<img style="float: right; display: inline-block; margin: 20px 0px 10px 10px" width="45%" height="45%" src="/images/blog/interesting_articles_2023/names.png">

This paper proposes a scheme for fairly listing author names when citing papers by overlaying all of the names (pictured to the right), simultaneously addressing several issues that creep up in research. At first glance, this is just an amusing joke in a joke paper at a joke conference. On second thought, there's some depth here. This is a well organized paper. The authors implemented their proposal in $\LaTeX$ and sketched out a solution for HTML. They even anticipate a challenge I had to the fairness of their solution in the conclusion. Bravo!

## The First Great Law & Economics Movement
______

Author: [Herbert Hovenkamp](https://en.wikipedia.org/wiki/Herbert_Hovenkamp)

Publication: [Stanford Law Review](https://www.jstor.org/journal/stanlawrevi)

Published: 1990

Link: [JSTOR](https://www.jstor.org/stable/1228909)

Hearing of the [law and economics program](https://en.wikipedia.org/wiki/Law_and_economics), one immediately thinks of the University of Chicago with [Friedrich von Hayek](https://www.hetwebsite.net/het/profiles/hayek.htm), [Milton Friedman](https://www.hetwebsite.net/het/profiles/friedman.htm), and others as discussed, for instance, in [Rationalizing Capitalist Democracy]({{ site.baseurl }}{% link _posts/2021-12-31-top-books-2021.md %}#rationalizing-capitalist-democracy-the-cold-war-origins-of-rational-choice-liberalism) from my book list for 2021. This paper surveys a prior law and economics movement which stretched from the anti-trust era and the marginal revolution in the 1880s to the rise of ordinal utility theory in the 1920s and 1930s. 

Much of this first movement sought to use material or other objective measures of welfare (even if imperfect) to reason about policy. There are certainly parallels between this and what [John Rawls](https://plato.stanford.edu/entries/rawls/) was up to in [A Theory of Justice](https://en.wikipedia.org/wiki/A_Theory_of_Justice). Over time, this strategy increasingly informed public policy and judicial reasoning; however, it fell out of favor in the academic literature by the ordinalist movement, which argued against interpersonal comparisons of utility. 


## Analytic women: The lost women of early Analytic philosophy
______

Authors: [Jeanne Peijnenburg](https://aeon.co/users/jeanne-peijnenburg) and [Sander Verhaegh](https://aeon.co/users/sander-verhaegh)

Publication: [Aeon](https://aeon.co)

Published: 2023

Link: [Click here](https://aeon.co/essays/the-lost-women-of-early-analytic-philosophy)

The vast majority of scholars become forgotten to history. Two pathways to being forgotten are the historical and the historiographical. The former is when one's work is not appreciated by their contemporaries; the latter when one's work is excluded from the canon. Peijnenburg and Verhaegh survey interesting examples of each pathway from [Analytic philosophy](https://iep.utm.edu/analytic-philosophy/) in the late nineteenth and early twentieth century. 

<img style="float: right; display: inline-block; margin: 0px 0px 10px 15px" width="23%" height="23%" src="/images/blog/interesting_articles_2023/philosophyinanewkey_langer.webp">

An example of the historiographical pathway is [Susanne Langer](https://en.wikipedia.org/wiki/Susanne_Langer), who studied under [Alfred North Whitehead](https://plato.stanford.edu/entries/whitehead/) at Harvard and became a proponent of [logical atomism](https://en.wikipedia.org/wiki/Logical_atomism) in the US. Her work was widely regarded and discussed, for instance, by the [Vienna Circle](https://plato.stanford.edu/entries/vienna-circle/) in the early 1930s. Her 1942 book, [Philosophy in a New Key](https://en.wikipedia.org/wiki/Philosophy_in_a_New_Key), sought to apply logical methods to the arts. As she drifted close to the humanities, she subsequently fell out of the account of analytic philosophy in the US and elsewhere. Langer, however, remained relevant in the [philosophy of art](https://www.britannica.com/topic/philosophy-of-art). 

An example of the historical pathway is [E. E. Constance Jones](https://plato.stanford.edu/entries/emily-elizabeth-constance-jones/), a professor at Cambridge alongside [Bertrand Russell](https://plato.stanford.edu/entries/russell/) and [G. E. Moore](https://plato.stanford.edu/entries/moore/). Jones offered a solution to a version of [Frege's Puzzle](https://en.wikipedia.org/wiki/Frege%27s_puzzles) in 1890, two years before Frege's [On Sense and Reference](https://en.wikipedia.org/wiki/Sense_and_reference). Her work was largely ignored by her contemporaries being considered too _Victorian_ since it worked within the [Aristotelian logic](https://plato.stanford.edu/entries/aristotle-logic/) tradition.

## Synthetic Data and Public Policy: supporting real-world policymakers with algorithmically generated data
______

Author: [Kevin Jenkins](https://www.martinjenkins.co.nz/about-us/board/kevin-jenkins/)

Publication: [Policy Quarterly](https://ojs.victoria.ac.nz/pq/about)

Published: 2023

Link: [Click here](https://ojs.victoria.ac.nz/pq/article/view/8234)

This article is an informal survey of synthetic data with a dash of privacy aimed at policymakers. The opening does an excellent job explaining synthetic data at a lay-level. Particularly, that "synthetic data is generated to preserve the statistical relationships and patterns of the original real-world dataset" rather than just mimic its database structure. For generating synthetic data, Jenkins mentions [GANs](https://en.wikipedia.org/wiki/Generative_adversarial_network) and [VAEs](https://en.wikipedia.org/wiki/Variational_autoencoder). Regarding statistical relationships, a synthetic dataset is condsidered "lo-fi" if only one-way marginals are preserved and "hi-fi" if higher-order marginals are preserved. Lo-fi synthetic data preserves the distribution of each attribute but no correlations between attributes. 

<figure style="display: block; margin: 0px 0px 0px 0px">
  <img style="display: block; margin: 0px 0px 0px 0px" src="https://dataingovernment.blog.gov.uk/wp-content/uploads/sites/46/2020/08/synthetic_data_image-620x290.png">
</figure>

A good bit of space is devoted to privacy matters and - I'm happy to see - [differential privacy](https://en.wikipedia.org/wiki/Differential_privacy) is discussed. The challenge of privacy researchers is to find "the balance between fidelity and mitigating the risk of re-identification" in synthetic data generation. The [general strategy](https://differentialprivacy.org/synth-data-1/) for doing this with differential privacy is to privately choose a set of strongly-correlated higher-order marginals to preserve and make assumptions on the distribution of unmeasured attributes. [This paper of mine]({{ site.baseurl }}{% link _posts/2022-03-20-aim-synthetic-data.md %}) introduces an algorithm called AIM for privately generating synthetic data for high-dimensional discrete datasets.

## Identification and Estimation of Local Average Treatment Effects
______

Authors: [Guido Imbens](https://en.wikipedia.org/wiki/Guido_Imbens) and [Joshua Angrist](https://en.wikipedia.org/wiki/Joshua_Angrist) 

Publication: [American Economic Review](https://en.wikipedia.org/wiki/American_Economic_Review)

Published: 1994

Link: [JSTOR](https://www.jstor.org/stable/2951620)

Causal inference is a powerful method in the arsenal of modern empirical social science researchers. This includes more than randomized experiments, since social scientists often want to learn causal effects from observational data. With experimental data under ideal conditions, causal effects are simple to estimate and interpret. For example, for an ideal simple experiment measuring the effect of binary treatment $D$ on outcome $Y$, the [average treatment effect (ATE)](https://en.wikipedia.org/wiki/Average_treatment_effect) is estimated as the average outcome for units receiving the treatment minus the average outcome for units without treatment. We can interpret this effect counterfactually as the average change in $Y$ if treatment is received compared to no treatment over the whole study population.

<img style="float: right; display: inline-block; margin: 20px 0px 10px 10px" width="45%" height="45%" src="https://mixtape.scunning.com/07-Instrumental_Variables_files/figure-html/iv_dag1-1.png">

For complex causal models such as those using observational data, we may not be able to obtain causal effect estimates that apply as generally. This short but insightful paper proves identification results within the [potential outcomes framework](https://en.wikipedia.org/wiki/Rubin_causal_model) for the [instrumental variables (IV)](https://en.wikipedia.org/wiki/Instrumental_variables_estimation) causal model where the estimated effect can be interpreted as the [local average treatment effect (LATE)](https://en.wikipedia.org/wiki/Local_average_treatment_effect). To illustrate this, suppose the instrument $Z$ indicates whether one is assigned the treatment and $D$ indicates whether one actually receives the treatment. The LATE estimate is the ATE for the population of *compliers* that receive the treatment if assigned but not otherwise.

For a well-known and early example of this approach, see Angrist's [Lifetime Earnings and the Vietnam Era Draft Lottery](https://www.jstor.org/stable/2006669) (1990). This paper estimates the effect of veteran status during the Vietnam war on earnings using birthday as an instrument to get at the causal effect of the draft. This paper was part of the citations for Angrist and Imbens' share of the [Nobel Prize in Economics in 2021](https://www.nobelprize.org/uploads/2021/10/popular-economicsciencesprize2021-3.pdf).

## Rational Magic
______

Author: [Tara Isabella Burton](http://www.taraisabellaburton.com)

Publication: [The New Atlantis](https://en.wikipedia.org/wiki/The_New_Atlantis_(journal))

Published: 2023

Link: [Click here](https://www.thenewatlantis.com/publications/rational-magic)

The [rationalist community](https://en.wikipedia.org/wiki/LessWrong) is a collection of blogs and websites that formed in the late 2000s to discuss cognitive biases, utilitarian decision-making, AI, etc. This community is largely siloed but has gotten press over the years by overlapping with better-known ideas/causes such as [effective altruism](https://en.wikipedia.org/wiki/Effective_altruism), [longtermism](https://en.wikipedia.org/wiki/Longtermism), and [AI safety](https://en.wikipedia.org/wiki/AI_safety). 

In recent years, some in this community have grown disillusioned by the perceived parochial thought and methods of the rationalists such as focusing exclusively on narrow quantifiable metrics to measure the efficiency of charitable donations. The disaffected have embraced different sorts of experiences and ways of interacting and finding meaning with the world such as through traditional religion or even the occult. Rational Magic surveys the rise of the [postrationalists](https://postrationalism.org) in recent years and provides a helpful narrative connecting these internet subcultures to broader ideas and figures. 

Burton offers the following contrast:
>The rationalists dreamed of overcoming bias and annihilating death; the postrats are more likely to dream of integrating our shadow-selves or experiencing oneness.

While Burton's narrative is often sympathetic to both groups, I can't but read this contrast as a caricature of the [divide between logical empiricism and existentialism](https://www.jstor.org/stable/20026868) in the mid-20th century or between [analytic and continental philosophy](https://philosophynow.org/issues/74/Analytic_versus_Continental_Philosophy) more generally. Much like [cryptocurrency and blockchain enthusiasts]({{ site.baseurl }}{% link _posts/2020-12-29-interesting-research-2010s.md %}#blockchains-and-cryptocurrencies) and other insular online communities, the level of discourse with both rationalists and postrationalists is often amateurish and peppered with in-group references. It is interesting, however, when their ideas spill out into the mainstream. Unlike Burton (and perhaps [David Brooks](https://www.nytimes.com/2023/12/28/opinion/sidney-awards-essays-magazines.html)), though, I find the ideas and approaches of both groups suspect at best.

## Can a good philosophical contribution be made just by asking a question?
______

Authors: [Joshua Habgood-Coote](https://ahc.leeds.ac.uk/philosophy/staff/3396/dr-joshua-habgood-coote), [Lani Watson](https://www.philosophy.ox.ac.uk/people/lani-watson), and [Dennis Whitcomb](https://philpeople.org/profiles/dennis-whitcomb)

Publication: [Metaphilosophy](https://en.wikipedia.org/wiki/Metaphilosophy_(journal))

Published: 2022

Link: [Paper](https://onlinelibrary.wiley.com/doi/10.1111/meta.12599) - [Commentary](https://onlinelibrary.wiley.com/doi/10.1111/meta.12600)

This paper asks a single question in its title and leaves the response to the reader. Is it a hoax? Likely not, since it makes an interesting point that's certainly relevant to [metaphilosophy](https://iep.utm.edu/con-meta/). Is it the [shortest legitimate paper](https://scientistseessquirrel.wordpress.com/2015/06/10/can-a-scientific-paper-be-too-short-part-ii/) ever published? Technically yes, but not quite; the journal editor published a letter from the authors as commentary on the idea of the paper. The commentary has enough whimsey to appear sincere and enough heft to be taken seriously. 

<img style="float: right; display: inline-block; margin: 25px 0px 25px 10px" width="50%" height="50%" src="/images/blog/interesting_articles_2023/paper.png">

The authors compare their paper to [embodied art](https://users.rowan.edu/~clowney/Aesthetics/philos_artists_onart/danto.htm) insofar as the question in the title contains or expresses the content of the paper such as [Duchamp's sculpture Fountain](https://en.wikipedia.org/wiki/Fountain_%28Duchamp%29). A more interesting comparison is with [speech acts](https://plato.stanford.edu/entries/speech-acts/) i.e. utterances that are made true or come to pass by the act of uttering them. For instance, "I have typed this" and "you are reading this" are both performative analogues of the speech act. Notice that these cases are [self-referential](https://www.colinmcginn.net/performatives-and-self-reference/) in the same way that asking the paper's question answers itself.

## The Great Convergence: Global Equality and Its Discontents
______

Author: [Branko Milanovic](https://en.wikipedia.org/wiki/Branko_Milanović)

Publication: [Foreign Affairs](https://en.wikipedia.org/wiki/Foreign_Affairs)

Published: 2023

Link: [Click here](https://www.foreignaffairs.com/world/great-convergence-equality-branko-milanovic)

Rising income and wealth inequality is a [commonplace narrative](https://www.brookings.edu/articles/rising-inequality-a-major-issue-of-our-time/) for explaining, among other things, the increase in social strife within liberal democratic countries. Note though that narrative has come under fire a bit in the US due to Gerry Auten and David Splinter's [recent paper](https://www.journals.uchicago.edu/doi/10.1086/728741). 

In this article, Milanovic argues that the income inequality narrative is turned on its head when viewed globally. In the 30 year period from 1988 to 2018, Western countries saw the lower end of earners fall in the global distribution of income while the upper end remained relatively unchanged. This is due to rising incomes among middle- and high-earners in Asia, particularly in China and India. 

This finding suggests a secondary source for economic discontent: 

>Western countries are increasingly composed of people who belong to very different parts of the global income distribution.

Uncertainty in the international relations landscape from Ukraine to Israel and elsewhere make it difficult to predict how global incomes will shape out in the coming years. Nevertheless, this is an interesting observation and a [stylized fact]({{ site.baseurl }}{% link _posts/2022-12-19-interesting-articles-2022.md %}#stylized-facts-in-the-social-sciences) worth explaining. 

