---
layout: post
title: Some Fun with Knights and Knaves
categories: Logic
mathjax: true
---


I'm currently working through Raymond Smullyan's [The Gödelian Puzzle Book](https://store.doverpublications.com/0486497054.html) and came across a fun problem that serves as a good starting point for new readers of Smullyan. Smullyan is well known for (among many other things) producing [several books of logic puzzles](https://en.wikipedia.org/wiki/Raymond_Smullyan#Logic_puzzles) that introduce ideas from mathematical and philosophical logic in an accessible but still technical way. These books are often formatted where each chapter has an introduction to the relevant characters, ideas, and setting, several problems for the reader to work through, and the solutions to the problems.
<img style="float: right; display: inline-block; margin: 10px 0px 0px 20px; width: 200px; height: 300px" src="https://sep.yimg.com/ca/I/yhst-137970348157658_2614_646619657">
I've found that working through Smullyan's books helps build mathematical intuition better than repeatedly walking through proofs and applications of theorems. I would much rather go through Smullyan's Gödel book than ever see [Enderton's Chapter 3](https://www.logicmatters.net/tyl/booknotes/enderton/) again!   

The Knights and Knaves are a trope found throughout several of Smullyan's books. Knights can only tell truths, while Knaves can only tell falsehoods. In Chapter 2 of The Gödelian Puzzle Book, our narrator finds himself on *The Island of Knights and Knaves* where each inhabitant is either a Knight or a Knave. What follows is a fun, open-ended problem using natural language to reason about self-reference.  

> **Problem 7.** One day I saw an extremely beautiful lady on this island and was immediately smitten with her. I longed to know whether or not she was married, but I did not have the courage to ask her. The next day I came across her two brothers Alfred and Bradford. Alfred then made a statement. From this statement I could not tell whether or not the lady was married. Then to my surprise, Bradford made the same statement, from which I could tell that she was not married. What statement could that have been?

Be sure to try to solve the problem before expanding the solution below!

<details>
  <summary><b>Solution</b> (click the arrow to expand)</summary>

  <p>There are several such solutions, but the one I landed on is "I am a knave, my brother is a knave, and my sister is married." Let's refer to the two brothers as Brother A and Brother B. Let Brother A utter "I am a knave, my brother is a knave, and my sister is married." Brother A can either be a knight or a knave. If Brother A is a knight, then he truly asserts that he is a knave: a contradiction; hence, Brother A is a knave. Then his utterance is false. So we have that either Brother A is a knight (we know to be false), Brother B is a knight, or the sister is not married. While we have some information, we do not yet know whether or not the sister is married.</p>

  <p>Suppose now that Brother B utters "I am a knave, my brother is a knave, and my sister is married." As with Brother A, Brother B must also be a knave. Since either Brother B is a knight or the sister is not married, it must be the case that the sister is unmarried!</p>
</details>

I find that these open-ended problems are the most entertaining and instructive. Rather than asking the reader to determine $P$ or $\neg P$, these problems challenge the reader to create a sentence, situation, or condition. Being able to identify and find what is needed to solve some problem and then prove that it, indeed, solves the problem is much closer to how mathematics is actually practiced than the former approach.

If you're interested in more on Smullyan, I recommend picking up any of his puzzle books or [Four Lives](https://store.doverpublications.com/048649067x.html), part biography of Smullyan, part collection of interesting mathematical and metamathematical thoughts, and part sampler of Smullyan's most well known logic puzzles.
