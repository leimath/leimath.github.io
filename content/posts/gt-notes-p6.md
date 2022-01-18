+++
title = "My Graph Theory Notes - Part 6"
date = "2022-01-18"
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

This is the sixth part of the graph theory notes. We take a look at Hamiltonian Graphs. We omit a tactics section since the questions related to Hamiltonian Graphs are diverse each requiring some approach unique in its own way, please see the **#Questions** section for further references.

The book followed throughout is: _Graph Theory with Applications_ by _Bondy J.A., Murty U.S.R._. Please refer to the book for examples as well as visual graph drawings.

---
---

# Hamiltonian Graph

If a chain exists such that it passes through **every** vertex only once, then the chain is called a `Hamiltonian Chain`, respectively the definition also follows similarly for `Hamiltonian Cycles`. Put differently, a Hamiltonian chain is where it visits every vertex
exactly once but need not cover every edge. If a graph contains a Hamiltonian **_cycle_** then the graph is called a `Hamiltonian Graph`. 

Note that no nontrivial necessary and sufficient condition for a graph to be Hamiltonian is known, it is one of the main unsolved problem of graph theory. However, there are some negative tests, which can show that a given
graph contains no Hamilton path or cycle, and some positive tests, which can show that
a given graph contains a Hamilton path or cycle without actually constructing one. These
tests do not apply to every graph.

Refer to [this](https://www.youtube.com/watch?v=CEOGcSCTar8) to get a idea on the differences in the Eulerian Graph and Hamiltonian Graphs. Loosely, Eulerian graphs only bother with edges whereas a Hamiltonian graph has to deal with the vertices.

# Theorems

`Theorem 1`: In a bigraph $G$ if $|V_1| \neq |V_2|$, $G$ must contain no Hamiltonian cycle. If the difference between $|V_1|$ and $|V_2|$ is more than $1$, $G$ must contain no Hamiltonian chain.

`Theorem 2`: Let $G$ be a simple graph with $n \geqslant 3$ vertices. For every pair of vertices $v,v'$ if $$d(v) + d(v') \geqslant n - 1$$ then $G$ contains a Hamiltonian chain.

Note that the Theorem 2 condition is indeed gives a way for existence of a Hamiltonian chain but it is not necessary. There exists examples (e.g, a regular hexagon) where the condition fails yet the graph is a Hamiltonian chain.

`Theorem 3[Ore]`: Let $G$ be a simple graph with $n$ vertices. For every two nonadjacent vertices $v,v'$ if $$d(v) + d(v') \geqslant n$$ then $G$ is a Hamiltonian cycle.

`Theorem 4[Dirac]`: Let $G$ be a simple graph with $n$ vertices. If the degree of every vertex $v$ is no less than $\frac{n}{2}$, then $G$ must contain a Hamiltonian cycle.

`Theorem 5[Pósa]` Let $G$ be a graph with $n$ vertices, where $n \geq 3$, and suppose that the degrees in $G$ satisfy $$d_{1}>1 ~ ,~ d_{2}>2~,~ \ldots ~, ~ d_{i}>i$$ where $d_1,d_2, \ldots, d_i$ represents the degrees of each vertex for all values of $i < \frac{n}{2}$.
Then $G$ contains a Hamilton cycle.

This is the so called `Pósa's theorem`, and in a way -- the combined power form of Theorem 3 and 4.

$$\dotsb$$


`Theorem 6`: If $G$ contains a Hamiltonian graph, remove several vertices $v_1, v_2, v_3, \ldots v_k$ and their adjacent edges from $G$ to get new graph $G^\prime$, then the number of connected components in $G^\prime$ is no more than $k$.

---

# Questions

A lot of different variants of questions are possible and simply listing down tactics wouldn't cover the strategies usually required, hence we recommend the reader to do questions from any standard book (either from the one mentioned at the begining of this post, or _Graph Theory: A Problem Oriented Approach by Daniel Marcus, Chapter G_) along with the questions presented below.

`1.` Arrange 7 examinations in 7 days so that the two courses which are taught by one teacher cannot be arranged in two consecutive days. If every teacher can teach at most 4 courses which have examination. Prove that it is possible to arrange the examinations in the above way.

`2.` A factory produces two-color paper using 6 distinct colored yarns. Among six kinds of yarns, every color must be matched in groups with three other colors. Prove that it is possible to choose three kinds of two-color paper so that all 6 colors are present.

`3.` If $A_{0} A_{1} A_{2} \ldots A_{2 n-1}$ is a regular polygon of $2 n$ sides. Join all its diagonals to get a graph $G$. Prove that every Hamiltonian cycle of $G$ must contain two edges which are parallel in the graph.

`4.` An executive has $2 n$ friends, among whom there are several friends hate each other. But the number of persons every friend hates is no more than $n-1$. Can they sit in a round table so that no two adjacent friend hate each other?

`5.` Around a table there sit at least five persons and it is possible to rearrange their seats so that beside everyone there are two new neighbours.