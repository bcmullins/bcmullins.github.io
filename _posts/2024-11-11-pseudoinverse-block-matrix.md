---
layout: post
title: Pseudoinverse of Repeating Vertical Block Matrix
categories: DifferentialPrivacy
mathjax: True
---

A [block matrix](https://en.wikipedia.org/wiki/Block_matrix) is a structured representation of a matrix as partitioned into submatrices. 
For example, let $A, B, C, D$ be $m \times n$ matrices. Then 
$$\begin{bmatrix} A & B \\ C & D \end{bmatrix}$$ 
is a $2m \times 2n$ block matrix. 
A special case called vertical (or horizontal) block matrices have blocks stacked in a single column (or row). 
In this post, we discuss a simple result for calculating the pseudoinverse of a repeating vertical block matrix i.e. a vertical block matrix where each block is identical. 
This result has been mentioned in a few places on [Wikipedia](https://en.wikipedia.org/wiki/Block_matrix_pseudoinverse#Derivation) and elsewhere but not with a direct proof.

The [Moore-Penrose pseudoinverse](https://en.wikipedia.org/wiki/Moore–Penrose_inverse) is a generalization of the inverse to non-square matrices. 
Suppose we have $Bx = y$, and observe $y$ and $B$. 
We can obtain a [least-squares estimate](https://en.wikipedia.org/wiki/Moore–Penrose_inverse#Linear_least-squares) of $x$ given by $\widehat{x} = B^+ y$, where $B^+$ is the pseudoinverse of $B$. In general, computing the pseudoinverse is computationally expensive. For a repeating vertical block matrix, we can reduce the running time by a factor of at least $k$, where $k$ is the number of repeated blocks, using the following result.

**Theorem.** Let $A$ be a matrix and $B$ be the vertical block matrix consisting of $k$ copies of $A$. Then $B^+ = \big(\frac{1}{k}\big)[A^+ A^+ \cdots A^+]$ is a horizontal block matrix of $k$ copies of $A^+$ multiplied by $\frac{1}{k}$. 

**Proof:** Let $A = U \Sigma V^T$ be a [singular value decomposition](https://en.wikipedia.org/wiki/Singular_value_decomposition) of $A$ where $U, V$ are [orthogonal matrices](https://en.wikipedia.org/wiki/Orthogonal_matrix). Then $B = U_k \Sigma V^T$ where $U_k$ is a vertical block matrix consisting of $k$ copies of $U$. Since $U$ is full column rank, $U_k$ is full column rank, and 

$$\begin{align*}
    U_k^+ &= (U_k^T U_k)^{-1} U_k^T \\
            &= (k U^T U)^{-1} U_k^T \\
            &= \frac{1}{k} U_k^T.
\end{align*}$$

Then 

$$\begin{align*}
    B^+ &= V \Sigma^{-1} U_k^+ \\
        &= V \Sigma^{-1} \frac{1}{k} U_k^T \\
        &= \frac{1}{k} [A^+ A^+ \cdots A^+].
\end{align*}$$ 

Let $A$ and $B$ be defined as above. If $A$ is an $m \times n$ matrix, then $B$ is a $km \times n$ matrix. For simplicity, suppose $n < m$. If we disregard the structure of $B$, the running time of computing $B^+$ is $\mathcal{O}(km n^2)$, the cost of SVD on $B$. However, using the above theorem, we can compute $B^+$ in $\mathcal{O}(m n^2)$ time. This is because we only need to compute $A^+$ once and then replicate it $k$ times, giving a speedup by a factor of $k$. Under other settings of $m$, $n$ and $k$, the speedup is greater: a factor of $k^2$ if $km \leq n$, and a factor of $k \big(\frac{n}{m}\big)$ if $m < n \leq km$.