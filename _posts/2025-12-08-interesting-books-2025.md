---
layout: post_top
title: Interesting Books I've Read in 2025
categories: Review
mathjax: true
---

Below are some interesting books I've read in 2025. This year's list is topically wide-ranging: from the mathematics of [data privacy](#differential-privacy) and [information theory](#an-introduction-to-information-theory-symbols-signals-and-noise) to the history of [economic thought](#after-adam-smith-a-century-of-transformation-in-politics-and-political-economy), from [early analytic philosophy](#philosophical-analysis-its-development-between-the-two-world-wars) and [contemporary metaphilosophy](#relativism-and-the-foundations-of-philosophy) to [weird fiction](#tales-of-the-weird-an-uncanny-introduction), and even an early nineteenth-century meditation on the [art of eating well](#the-philosopher-in-the-kitchen). If you have some thoughts on my list or would like to share yours, send me an email at brettcmullins(at)gmail.com. Enjoy the list!

<!-- 

## title
______

Author: 

Published: 

content 

-->


## Differential Privacy
______

Author: [Simson Garfinkel](https://en.wikipedia.org/wiki/Simson_Garfinkel)

Published: 2025

Link: [MIT Press](https://direct.mit.edu/books/book/5935/Differential-Privacy)

[Differential privacy](https://en.wikipedia.org/wiki/Differential_privacy) (DP) is a mathematical framework for quantifying privacy risk in data analysis. It provides formal guarantees that any individual's data does not significantly affect the outcome of an analysis, which allows for protecting privacy while still doing useful things. Analyses include calculating means, medians, and other summary statistics, learning data distributions, and training machine learning models. We satisfy differential privacy by injecting randomness into the data analysis such as [adding calibrated noise](https://en.wikipedia.org/wiki/Additive_noise_differential_privacy_mechanisms) from a Gaussian distribution.

<figure style="float: right; display: inline-block; margin: 0px 0px 0px 15px">
    <img width="200" height="300" src="/images/blog/interesting_books_2025/dp.jpeg" alt="Differential Privacy book cover">
</figure>

In 2026, differential privacy [turns twenty](https://link.springer.com/chapter/10.1007/11681878_14). While there are a handful of [monographs](https://www.nowpublishers.com/article/Details/TCS-042), [edited volumes](https://www.nowpublishers.com/Article/BookDetails/9781638284765), and [other sorts of introductions](https://programming-dp.com) to differential privacy, a wide-interest invitation to this adolescent field was lacking. Garfinkel's short book fills this void, being light enough for most to follow but with enough heft to say something interesting.

This book does several things well. It spends a good bit of time developing intuitive examples to describe the sort of privacy protection that DP offers. It provides a history (or mythology) for the field that I haven't seen written elsewhere, beginning with work of [Tore Dalenius](https://en.wikipedia.org/wiki/Tore_Dalenius) on [statistical disclosure limitation]({{ site.baseurl }}{% link _posts/2024-12-31-interesting-articles-2024.md %}#finding-a-needle-in-a-haystack-or-identifying-anonymous-census-records) and [Latanya Sweeney](https://en.wikipedia.org/wiki/Latanya_Sweeney) on [reidentification attacks](https://desfontain.es/blog/k-anonymity.html) before the introduction of DP and culminating with the [2020 US Decennial Census](https://www.census.gov/programs-surveys/decennial-census/decade/2020/planning-management/process/disclosure-avoidance/differential-privacy.html), the largest (and most scrutinized) deployment of DP to date. Finally, there is lengthy but helpful discussion navigating through arguments for and against DP.

While there are some nits I could pick, this is an excellent introduction to differential privacy aimed at a wide audience and one that I've already recommended to students. This book is part of the [Essential Knowledge series](https://mitpress.mit.edu/series/mit-press-essential-knowledge-series/) from MIT Press. Earlier this year, I also enjoyed their introduction to [Cryptography](https://mitpress.mit.edu/9780262549028/cryptography/) (2024). 

## The Philosopher in the Kitchen
______

Author: [Jean Anthelme Brillat-Savarin](https://en.wikipedia.org/wiki/Jean_Anthelme_Brillat-Savarin)

Published: 1825

Translated by Anne Drayton (1970)

French Title: [Physiologie du goût](https://fr.wikipedia.org/wiki/Physiologie_du_goût)

Link: [Internet Archive](https://archive.org/details/philosopherinkit0000bril/page/n3/mode/2up)

<figure style="float: right; display: inline-block; margin: 10px 10px 10px 10px">
    <img width="200" height="300" src="/images/blog/look_back/1825/kitchen.jpeg">
</figure>

Jean Anthelme Brillat-Savarin was a French lawyer, politician, and noted gastronome. His part-memoir part-treatise, Physiologie du goût, is a prolegomenon of sorts to the science of gourmandism. One may be tempted to think that this study of food and culture is merely a guide to gluttony. Brillat-Savarin is careful to dispel such notions. The glutton mindlessly consumes to excess, while the gourmand appreciates and enjoys to satisfaction. Far from a handbook to hedonism, this analysis of the art of the gourmand encompasses gastronomy, physical and mental health, and social interaction.

The book is written in short sections loosely divided into themes, mixing technical discussions of the author's theory of [food chemistry](https://en.wikipedia.org/wiki/Food_chemistry) with recipes and tales from his eventful life. The writing is often witty and the translation by Anne Drayton is a pleasure to read. I was hooked from the beginning by the list of aphorisms that preface the main text; the best of which reads:

>Dessert without cheese is like a pretty woman with only one eye.

In the section on physical and mental health, Brillat-Savarin discusses the importance of diet in maintaining health and longevity. He makes a case for the benefits of a [low-carb diet](https://www.mayoclinic.org/healthy-lifestyle/weight-loss/in-depth/low-carb-diet/art-20045831) for losing excess weight, becoming one of its first proponents.

There's an amusing mention of a correlational health outcomes study by [Louis-René Villermé](https://en.wikipedia.org/wiki/Louis-René_Villermé) from the prior year. This study finds that "good cheer is far from being harmful to health, and that, all things being equal, gourmands live longer than other men." Elaborating on the methods:

>He compared the various classes of society in which good cheer is habitual with those which are poorly fed, covering the entire social scale. He also considered the various quarters of Paris with one another according to their wealth, for it is well known that wide divergencies exist in this respect. 

The most interesting section, however, is the discussion of restaurants near the book's conclusion. Restaurants in the modern sense were a [relatively recent innovation](https://en.wikipedia.org/wiki/Restaurant#Modern_format), appearing in Paris in the latter half of the eighteenth century and quickly spreading throughout Europe and beyond during the French Empire's warring efforts. I read this book as part of my [project looking back at research]({{ site.baseurl }}{% link _posts/2025-04-21-research-from-1825.md %}) from 100, 150, and 200 years ago.

## After Adam Smith: A Century of Transformation in Politics and Political Economy
______

Authors: [Murray Milgate](https://en.wikipedia.org/wiki/Murray_Milgate) and [Shannon G. Stimson](https://en.wikipedia.org/wiki/Shannon_C._Stimson)

Published: 2009

One way to mark the birth of political economy is the publication of Adam Smith's [The Wealth of Nations](https://en.wikipedia.org/wiki/The_Wealth_of_Nations) (1776). When you think of [Smith](https://iep.utm.edu/smith/), several ideas might come to mind: the invisible hand, [laissez faire](https://en.wikipedia.org/wiki/Laissez-faire), pin factories and the division of labor, the [perfectly competitive market](https://en.wikipedia.org/wiki/Perfect_competition), and the butcher, the baker, and the candlestick maker. Though these ideas are often attributed to Smith today, what he meant by them looked rather different in some cases. This book traces the evolution of Smith's ideas and the path of political economy from their introduction to the close of classical period in the 1870s.

<figure style="float: right; display: inline-block; margin: 0px 0px 0px 15px">
    <img width="200" height="300" src="/images/blog/interesting_books_2025/afterAdamSmith.jpeg" alt="After Adam Smith book cover">
</figure>

Today, the [invisible hand](https://en.wikipedia.org/wiki/Invisible_hand) is a metaphor for the market as a self-regulating system and expresses a fundamental principle in modern economics. Smith mentions an invisible hand only once in The Wealth of Nations and once in [The Theory of Moral Sentiments](https://en.wikipedia.org/wiki/The_Theory_of_Moral_Sentiments) (1759) in a sort of throw-away line. The modern incarnation of the idea only gained popularity in the [early twentieth century](https://en.wikipedia.org/wiki/Invisible_hand#The_reinterpretation_by_modern_economists).

In the 1790s, the Scottish philosopher [Dugald Stewart](https://en.wikipedia.org/wiki/Dugald_Stewart) reinterpreted Smith's account of political economy along the lines of a liberal political program. In particular, Stewart argued that The Wealth of Nations "established a science whose laws dictated that in market economies, intervention was not only unnecessary but positively harmful to the wealth of the nation." In doing so, Stewart deemphasized the theoretical contributions of the first two books to focus on political conclusions. Milgate and Stimson hypothesize that this is why no one seriously grappled with the theory of value until [David Ricardo](https://www.hetwebsite.net/het/profiles/ricardo.htm) in the 1810s.

I found this book a challenging but rewarding read. Milgate and Stimson cover a broad range of material but manage to be engaging throughout. I found myself learning something interesting in nearly every section.

## Philosophical Analysis: Its development between the two World Wars
______

Author: [J. O. Urmson](https://en.wikipedia.org/wiki/J._O._Urmson)

Published: 1956

During the second world war, a curious change quietly happened in British philosophy: the [logical approach](https://en.wikipedia.org/wiki/Logical_atomism) to language and metaphysics was supplanted by the [ordinary language](https://en.wikipedia.org/wiki/Ordinary_language_philosophy) approach. This short book surveys the rise and fall of the logical approach and the many developments in-between. While Urmson is firmly rooted in the ordinary language tradition, he offers a clear and reasonable account of how and why the logical approach came to be.

<figure style="float: right; display: inline-block; margin: 0px 0px 0px 15px">
    <img height="300" width="240" src="/images/blog/interesting_books_2025/urmson.jpeg">
</figure>

Idealism dominated [philosophical discourse in Britain]({{ site.baseurl }}{% link _posts/2024-07-07-research-from-1924.md %}#contemporary-british-philosophy-personal-statements-first-series) throughout the late nineteenth and early twentieth centuries. Roughly, [idealism](https://plato.stanford.edu/entries/idealism/) views concepts and reality as an integrated whole, to be studied in a top-down way. The logical approach [flips this](https://plato.stanford.edu/entries/logical-atomism/) by reducing concepts to aggregations of logically simple atomic facts. 

This bottom-up approach built on work formalizing mathematics in a precise logical language such as the typed language of Russell and Whitehead's [Principia Mathematica](https://en.wikipedia.org/wiki/Principia_Mathematica) (1910), the second edition of which appeared in 1925. On this view, atomic facts correspond to [sense data](https://en.wikipedia.org/wiki/Sense_data), and concepts such as a red table and [the present king of France](https://en.wikipedia.org/wiki/Definite_description) are interpreted as expressing statements in a formal language such as [first-order logic](https://en.wikipedia.org/wiki/First-order_logic). Natural language, then, is an imprecise way of describing the world that can be improved using the tools of analysis.

This leaves several questions open such as how exactly do atomic sentences correspond to facts about the world. [Wittgenstein](https://plato.stanford.edu/entries/wittgenstein/) answers that atomic sentences [picture facts](https://en.wikipedia.org/wiki/Picture_theory_of_language) in the world, something akin to illustrating a particular feature of the world, from which they make sense. The upshot of this is that propositions not picturing facts are nonsense. This includes [philosophical propositions](https://plato.stanford.edu/entries/propositions/), which Wittgenstein was well aware of, and has intrigued philosophers [ever since](https://philosophynow.org/issues/33/Wittgensteins_Significance). 

Another approach is to eschew the connection between language and metaphysics and analyze language in a formal context such as scientific reasoning. This is the track taken by [Rudolf Carnap](https://plato.stanford.edu/entries/carnap/) and some members of the [Vienna Circle]({{ site.baseurl }}{% link _posts/2018-12-16-Top-Books-2018.md %}#exact-thinking-in-demented-times), where the meaning of a proposition is determined by the atomic sentences that could [verify it](https://en.wikipedia.org/wiki/Verificationism). This latter view suffered from self-defeating issues as well, since philosophical propositions could not be empirically verified. 

Though I'm familiar with early analytic philosophy, I learned quite a bit from this book. It provides one of the most digestible accounts of Wittgenstein's picture theory. Urmson's style is engaging even if a bit terse. The book concludes by sketching the ordinary language approach, which takes a more expansive view of language and relegates analysis to one tool among many. 

## Tales of the Weird: An Uncanny Introduction
______

Published: 2023

<figure style="float: right; display: inline-block; margin: 0px 0px 0px 15px">
    <img src="/images/blog/interesting_books_2025/talesWeird.jpeg">
</figure>

[Tales of the Weird](https://shop.bl.uk/collections/tales-of-the-weird?srsltid=AfmBOoptVnn_7TJVm63x2Cs1LL6-OQSxNQiTCwnUGkPfn5Pa_nTqLrZk) is a book series from the [British Library](https://en.wikipedia.org/wiki/British_Library) reprinting lesser known novels and themed short story collections from [weird fiction](https://en.wikipedia.org/wiki/Weird_fiction), broadly construed. For instance, [From the Depths and Other Strange Tales of the Sea](http://www.oddlyweirdfiction.com/2019/05/from-depths-and-other-strange-tales-of.html) collects together spooky nautical short stories from the late nineteenth and early twentieth centuries. The current collection is meant to pull from a variety of themes to introduce the reader to the many flavors of weird fiction.

My favorites are [William Hope Hodgson's](https://en.wikipedia.org/wiki/William_Hope_Hodgson) "The Voice in the Night" (1907), [H. P. Lovecraft's](https://en.wikipedia.org/wiki/H._P._Lovecraft) "The Festival" (1925), and [Mary Counselman's](https://en.wikipedia.org/wiki/Mary_Elizabeth_Counselman) "The Three Marked Pennies" (1934). Each of these three stories paints a vivid picture and really stuck in my mind. 

Two complaints are worth noting. The biographical sketches at the beginning of each story are both too brief and frequently spoil crucial elements of the plot. The structure would be better served by putting these after the story. The least interesting of the bunch - [Vernon Lee's](https://en.wikipedia.org/wiki/Vernon_Lee) "Marsyas in Flanders" (1900) - appears first, due to the stories being in chronological order. I recommend any other order than this!

## An Introduction to Information Theory: Symbols, Signals and Noise
______

Author: [John R. Pierce](https://en.wikipedia.org/wiki/John_R._Pierce)

Published: 1980

<figure style="float: right; display: inline-block; margin: 0px 0px 0px 20px">
    <img width="200" height="300" src="/images/blog/interesting_books_2025/infoTheory.jpeg">
</figure>

[Information theory](https://en.wikipedia.org/wiki/Information_theory) is the mathematical study of communication and provides a framework for quantifying information transmission. It has applications all over the place from cryptography to machine learning to [data privacy](#differential-privacy). This book is a highly-readable and wide-ranging introduction to the field. Pierce worked as an engineer at [Bell Labs](https://en.wikipedia.org/wiki/Bell_Labs) with [Claude Shannon](https://en.wikipedia.org/wiki/Claude_Shannon) during the development of information theory in the mid-twentieth century. 

The book begins with an excellent survey of information theory's [early years](https://en.wikipedia.org/wiki/History_of_information_theory#Before_1948) and provides a wealth of citations to interesting papers (enough to fill a backlog). The core chapters develop mathematical ideas such as [source coding](https://en.wikipedia.org/wiki/Shannon%27s_source_coding_theorem) and [channel coding](https://en.wikipedia.org/wiki/Coding_theory) in a semi-formal yet approachable way.  The auxiliary chapters are more topical and lax, ranging from connections between [entropy in communication](https://en.wikipedia.org/wiki/Entropy_(information_theory)) (uncertainty in terms of bits) and [entropy in physics](https://en.wikipedia.org/wiki/Entropy_in_thermodynamics_and_information_theory) (amount of free energy) to speculations on [generative models for music composition](https://en.wikipedia.org/wiki/Algorithmic_composition).

This book feels both ahead of its time and quite dated. I would likely not recommend it as a first stab at information theory; check out David MacKay's [wonderful text](http://www.inference.org.uk/mackay/itila/book.html) instead. This book would be great for someone with some familiarity of these ideas who can appreciate Pierce's historical anecdotes and speculations while reacquainting themselves with the fundamentals. For a taste, here's Pierce on AI and thinking machines:

>Will computers be able to think? This is a meaningless question unless we say what we mean by _to think_. Marvin Minsky, a free wheeling mathematician who is much interested in computers and complex machines, proposed the following fable. A man beats everyone else at chess. People say, "How clever, how intelligent, what a marvelous mind he has, what a superb thinker he is." The man is asked, "How do you play so that you beat everyone?" He says, "I have a set of rules which I use in arriving at my next move." People are indignant and say, "Why that isn't thinking at all; it's just mechanical."
>
>Minsky's conclusion is that people tend to regard as thinking only such things as they don't understand. I go even farther and say that people frequently regard as thinking almost any grammatical jumbling together of "important" words. At times, I'd settle for a useful, problem-solving type of "thinking," even if it was mechanical. In any event, it seems likely that philosophers and humanists will manage to keep the definition of thinking perpetually applicable to human beings and a step ahead of anything a machine ever manages to do. If this makes them happy, it doesn't offend me at all. I do think, however, that it is probably impossible to specify a meaning and explicitly defined goal which a man can attain and a computer cannot even including the "imitation game," proposed by A. M. Turing, a British logician [sic]. 

## Relativism and the Foundations of Philosophy
______

Author: [Steven D. Hales](https://scholar.google.com/citations?user=LJD3OxkAAAAJ&hl=en)

Published: 2006

A philosophical proposition is a statement regarding the fundamental nature of reality, knowledge, or values that cannot be decided empirically. Think of them as the armchair analog to [scientific laws](https://en.wikipedia.org/wiki/Scientific_law). Two examples in different domains are "murder is impermissible" and "the mind survives the body after death".

<figure style="float: right; display: inline-block; margin: 0px 0px 0px 20px">
    <img width="200" height="300" src="/images/blog/interesting_books_2025/relativism.avif">
</figure>

How do we reason about philosophical propositions? With empirical statements, we have observation. In philosophy, however, we often rely on [rational intuition](https://plato.stanford.edu/entries/intuition/). Yet, this is just one method among many that are used to form beliefs about philosophical propositions. Christian revelation or drug-induced mysticism, for instance, may yield radically different beliefs than rational intuition with the above examples.

How are we to decide between these (potentially) conflicting perspectives? This puts us in a pickle, since we cannot rely on rational intuition (or any of the other methods) [without fear](https://plato.stanford.edu/entries/relativism/#NoNeuGro) of circularity or an infinite regress. Hales rescues truth for philosophical propositions by relativizing truth to a perspective. He shows that the relativized notion of truth is consistent and makes it concrete by formalizing it in an [S5 modal logic](https://en.wikipedia.org/wiki/S5_(modal_logic)).

While his overall project is persuasive, it is not clear what this relativized notion of truth actually buys us. Much like [this NDPR reviewer](https://ndpr.nd.edu/reviews/relativism-and-the-foundations-of-philosophy/), I can see what truth relative to a perspective [means for moral propositions](https://en.wikipedia.org/wiki/Moral_relativism) but much less so for metaphysical propositions such as the mind surviving death. Presumably, the mind either survives or does not. The upshot of this project is that it does allow for [legitimate disagreement](https://plato.stanford.edu/entries/disagreement/) on philosophical propositions while not giving in to a [full-blown relativism](https://plato.stanford.edu/entries/relativism/#GloVsLocRel).

I came across this book while browsing the philosophy section at the [Book Mill](https://en.wikipedia.org/wiki/Bookmill) in Montague, Mass. I recognized Hales name from his [excellent blog](https://hilariusbookbinder.substack.com) and gave his book a shot. Who says a blog can't drive readers to one's academic work?!  

