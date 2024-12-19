---
layout: post
title: A coffee tour of downtown Vancouver (and NeurIPS 2024)
categories: Coffee DifferentialPrivacy
mathjax: true
---

This past week, I was in Vancouver for [NeurIPS](https://neurips.cc/Conferences/2024) to present our [latest work]({{ site.baseurl }}{% link _posts/2024-10-04-gremlnn.md %}) on differentially private query answering. Much to my delight, our host city was also a coffee city. Each morning and afternoon, I snuck away to grab a drink or two. Here are some thoughts on coffee and the conference.

## iced drinks

An iced drink isn't likely what comes to mind when thinking about coffee in Canada during December. Hear me out. Not only is Vancouver a bit warmer than my corner of Massachusetts, but the temperature in the conference center wavered between manageable and melting. Coffee with ice was a welcome respite. 

<figure style="float: right; display: inline-block; margin: 0px 0px 0px 10px">
    <img width="180" height="240" src="/images/blog/neurips2024/coldFashioned.jpg">
    <figcaption style="text-align: center; font-size: 12px;">A Cold Fashioned from <a href="https://www.funkcoffeebar.com">FUNK.</a></figcaption>
</figure>

First up is the most interesting drink from the trip: the Cold Fashioned from [FUNK.](https://www.funkcoffeebar.com) This drink is made with cold brew concentrate, maple syrup, bitters, and an orange twist (though I may be forgetting something). I'm generally skeptical about coffee mocktails, since they are frequently refreshing and quick to disappear, far from the usual experience with [an old fashioned](https://www.youtube.com/watch?v=DLk67oMq8Og). This is not the case here: this drink is a sipper. Its bitterness will curl your moustache. It will challenge you to dig in search of more. Then its depth of flavor will bring you back from the brink. This is the proper way to make a coffee mocktail. 

<figure style="float: left; display: inline-block; margin: 10px 15px 0px 0px">
    <img width="225" height="290" src="/images/blog/neurips2024/tonic.jpg">
    <figcaption style="text-align: center; font-size: 12px;">Espresso Tonic from <a href="https://revolvercoffee.ca">Revolver</a></figcaption>
</figure>

Next up is a more approachable and refreshing drink. My appetite for espresso tonics is like the ML community's current appetite for language models: nearly insatiable. This drink usually combines espresso, tonic water, and citrus of some sort, which brings out flavors not present in milk-based drinks. [Revolver's](https://revolvercoffee.ca) version was espresso-forward and centered on the presentation by layering ingredients. This is not merely aesthetic. If you're familiar with this drink, you've probably witnessed the deluge of foam caused by hot espresso rapidly mixed with cold tonic. This version would be improved, however, by the addition of citrus. While lemon is typically used, my favorite espresso tonic, from [Mister Magpie Coffee](https://www.instagram.com/mistermagpiecoffee/?hl=en) in Dublin, uses grapefruit.


## interesting talks

I am usually not very keen on large keynote-style talks. Here are two smaller talks I enjoyed, the latter of which was packed to the rafters. 

The first was a tutorial on [watermarking for language models](https://leililab.github.io/llm_watermark_tutorial/). The [idea of watermarking](https://en.wikipedia.org/wiki/Watermark) a physical image or document to prevent forgery has been around for centuries. For generating watermarked images from a model, this looks something like slightly perturbing the image in a way that's imperceptible to the human eye but detectable by the model owner. Doing something similar for language models poses a challenge because predicting the next word in a sentence offers dramatically less information to work with than all the pixels across channels in an image. 

<figure style="float: right; display: inline-block; margin: 10px 0px 0px 10px">
    <img width="300" height="225" src="/images/blog/neurips2024/watermark.png">
    <figcaption style="text-align: center; font-size: 12px;">"A Watermark for Large Language Models" <br/> Kirchenbauer et al. (2023)</figcaption>
</figure>

Over the past three years, several approaches to watermarking language models have been proposed. For example, with [Green-Red Watermarking](https://arxiv.org/abs/2301.10226), you randomly divide all tokens in the model's vocabulary into two sets: green and red. During inference, you slightly increase the probability of choosing a green token. The result is text that's detectible by the model owner by looking at the ratio of green to red tokens. Other approaches offer different trade-offs between the security of the watermark and the effect on the model's utility, including using [ideas from differential privacy](https://arxiv.org/abs/2402.05864). 

The second talk was a survey on [deep learning for tabular data](https://neurips.cc/Expo/Conferences/2024/talk%20panel/100668). While unstructured data is still all the rage, most applications in industry and elsewhere involve tabular data. The bad news for candidate predictive models in this domain is that they have to compete with [XGBoost and friends](https://towardsdatascience.com/https-medium-com-vishalmorde-xgboost-algorithm-long-she-may-rein-edd9f99be63d). Intuitively, the reason deep neural networks have been less successful on tabular data compared to images and text is that these models are less able to exploit the structure of the data, since various transformations of the columns aren't necessarily meaningful when columns denote different sorts of information (e.g. ordinal, categorical, continuous) in different units. The take away is that using embeddings and other tricks can help [deep learning models to be competitive](https://arxiv.org/abs/2407.00956) with tree-based methods. 

## lattes

When at conferences, I usually go for a latte at breakfast. All three lattes I sampled were excellent. The latte from [Pallet Coffee Roasters](https://palletcoffeeroasters.com) was the best tasting. [Nelson the Seagull Cafe](https://www.nelsontheseagull.com) offered a balanced latte with great presentation (pictured below). [Deville Coffee](https://www.devillecoffee.ca) had the best tasting milk and great seating. 

<figure style="display: block; margin: 0px 0px 25px 0px">
  <img style="display: block; margin: 0px 10px 10px 10px" src="/images/blog/neurips2024/latteSeagull.jpg">
  <figcaption style="text-align: center; font-size: 12px;">A latte and fruit cake from <a href="https://www.nelsontheseagull.com">Nelson the Seagull Cafe</a></figcaption>
</figure>

## conference venue

Last but not least, the Starbucks and [Coal Harbour Cafe](https://www.tripadvisor.com/Restaurant_Review-g154943-d3927379-Reviews-Coal_Harbour_Cafe-Vancouver_British_Columbia.html) at the convention center were more than serviceable and speedy despite being slammed the whole time. 