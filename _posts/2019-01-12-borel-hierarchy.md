---
layout: post
title: Borel Hierarchy in Latex with TikZ
categories: Helpful
mathjax: true
---

<img width="40%" height="40%" src="/images/blog/borel_hierarchy/borel_hierarchy.png">


I was looking online for a simple vertical Borel Hierarchy in Latex for a paper that I'm writing and had no luck. So I've written one. See the code below to use it.


```latex
\documentclass{article}

\usepackage{tikz}

\begin{document}
\begin{figure}
  \centering
  \begin{tikzpicture} [scale=1]
    \node (delta01) at (0,0) {$\Delta^0_1$};
    \node (sigma01) at (1,1) {$\Sigma^0_1$};
    \node (pi01) at (-1,1) {$\Pi^0_1$};
    \node (delta02) at (0,2) {$\Delta^0_2$};
    \node (sigma02) at (1,3) {$\Sigma^0_2$};
    \node (pi02) at (-1,3) {$\Pi^0_2$};
    \node (deltamid) at (0,4) {};
    \node (sigmamid) at (1,5) {};
    \node (pimid) at (-1,5) {};
    \node (delta0alpha) at (0,4) {$\Delta^0_\alpha$};
    \node (sigma0alpha) at (1,5) {$\Sigma^0_\alpha$};
    \node (pi0alpha) at (-1,5) {$\Pi^0_\alpha$};
    \node (delta0alpha1) at (0, 6) {$\Delta^0_{\alpha + 1}$};
    \node (deltatop) at (0,7) {};
    \node (sigmatop) at (1,7) {};
    \node (pitop) at (-1,7) {};
    \path (delta01) edge node[left] {} (sigma01);
    \path (delta01) edge node[left] {} (pi01);
    \path (delta02) edge node[left] {} (sigma01);
    \path (delta02) edge node[left] {} (pi01);
    \path (delta02) edge node[left] {} (sigma02);
    \path (delta02) edge node[left] {} (pi02);
    \path (delta02) -- (deltamid) node [midway, sloped] {$\dots$};
    \path (sigma02) -- (sigmamid) node [midway, sloped] {$\dots$};
    \path (pi02) -- (pimid) node [midway, sloped] {$\dots$};
    \path (delta0alpha) edge node[left] {} (sigma0alpha);
    \path (delta0alpha) edge node[left] {} (pi0alpha);
    \path (delta0alpha1) edge node[left] {} (sigma0alpha);
    \path (delta0alpha1) edge node[left] {} (pi0alpha);
    \path (delta0alpha1) -- (deltatop) node [midway, sloped] {$\dots$};
    \path (sigma0alpha) -- (sigmatop) node [midway, sloped] {$\dots$};
    \path (pi0alpha) -- (pitop) node [midway, sloped] {$\dots$};
  \end{tikzpicture}
  \caption{Borel Hierarchy}
  \label{g:borel_hierarchy}
\end{figure}
\end{document}
```
