+++
title = "My Graph Theory Notes - Part 8"
date = "2022-01-19"
author = "LeiMath"
tags = [
    "graph_theory",
    "graphs",
    "notes"
]
series = ["GT Notes"]
categories = [
    "graph_theory",
    "math"
]
+++

This is the eight part of the graph theory notes. We take a look at some theorems mostly related to Ramsey Numbers.

The book followed for the other notes is : _Graph Theory with Applications_ by _Bondy J.A., Murty U.S.R._. Please refer to the book for examples as well as visual graph drawings.

For this post, the readers are also encouraged to seek the proofs in other books such as the legendary _Adrian Bondy & U.S.R Murty - Graph Theory_ from _Springer - Verlag_ or _Graph Theory: A Problem Oriented Approach by Daniel Marcus_. 

---
---

# Ramsey Number

Consider $k$ colors, $c_1, c_2, c_3, \ldots, c_k$ to color the complete graph $K_n$. We call $K_n$ as the `k-color complete graph` if **every** edge is colored in one color. It doesn't take much convincing to claim that if $n$ is large enough, $k$-color complete graph $K_n$ must contain a monochromatic triangle. Call the least of such $n$ by $r_k$. 

$\displaystyle r_k$ is nothing but the `Ramsey Number` named after British mathematician Ramsey who proved its existence. 

Suppose every edge of the complete graph $K_{n}$ is colored in red or blue, which means that $K_{n}$ is a two-color (red, blue) complete graph $K_{n}$. For two constant natural numbers $p, q$, when $n$ is large enough, the two-color (red, blue) complete graph $K_{n}$ must contain a red $K_{p}$ or a blue $K_{q}$. We denote the least $n$ satisfying the above proposition by $r(p, q)$. We also call $r(p, q)$ the Ramsey number.

$r(p,q)$ is hence the minimum $n$ so that any $n$-subgraph $G$ of the complete graph $K_n$ contains a complete subgraph $K_p$ or its complementary graph $\bar{G}$ contains a complete subgraph $K_q$.
Also that, $r(1,q) = r(p,1) = 1$.


# Theorems

`All of the proofs are omitted as some are way too long or quite difficult for the needs of these notes`, particularly that they hold no purpose here (or for a Scholarship exam for which these notes are for!) and might as well be referred directly from any standard Graph Theory book - like the ones mentioned below.

$$\dotsb$$


`Theorem 1`: If a complete graph $K_n$ in two colors contains a monochromatic triangle, then the minimum $n$ is equal to 6.

$$\dotsb$$

For Theorem 1, $r(3,3) = r_2 = 6$. 
See [here, page 2](https://math.mit.edu/~apost/courses/18.204_2018/ramsey-numbers.pdf) for a proof.

$$\dotsb$$


`Theorem 2`: [I] For every positive integer $k$, the Ramsey Number $r_k$ exists. When $k \geqslant 2$, $$r_k \leqslant k(r_{k-1}-1 ) + 2$$

[II] For any $k \in \mathbb{N}$, $$r_k \leqslant 1 + 1 + k + k(k-1) + \ldots + \frac{k!}{2!} + \frac{k!}{1!} + k!$$

Note that Theorem 2 [II] is also written (with the help of series expansion of $e$) as $r_k \leqslant \lfloor k!~e~ \rfloor + 1$ where $\lfloor . \rfloor$ is the greatest integer function.

Some hints for the proof can be found [here](https://math.stackexchange.com/questions/1055435/modification-of-the-ramsey-number?noredirect=1)

$$\dotsb$$

Note that $r(2,q) = q$ and $r(p,2) = p$. Also, $r(p,q) = r(q,p)$ See  _Graph Theory with Applications_ by _Bondy J.A., Murty U.S.R._ Page 103, Section 7.2 for the discussion/proof.


`Theorem 4` [Ramsey's Theorem] For any two positive integers $n$ and $m$, the number $r(p, q)$ exists and satisfies the inequality $R(p, q) \leq r(p-1, q)+r(p, q-1) .$

For a proof see, _Adrian Bondy & Murty - Graph Theory (GTM) by Springer - Verlag_  Page 309 m, **Theorem 12.5**.

$$\dotsb$$

`Theorem 4`: When $p \geqslant 2$ and $q \geqslant 2$ then $$r(p,q) \leqslant \binom{p+q-2}{p-1}$$

Proof can be found in _Graph Theory with Applications_ by _Bondy J.A., Murty U.S.R._ Page 106, Theorem 7.5

---

# Questions

A lot of questions on Ramsey Numbers can be found [here](https://artofproblemsolving.com/community/q2_%22ramsey%20number%22) and also similarly searching "Ramsey" in the search field of artofproblemsolving forums. We direct the reader to try them to truly cover the varieties of such questions.