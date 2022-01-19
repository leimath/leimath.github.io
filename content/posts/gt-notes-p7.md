+++
title = "My Graph Theory Notes - Part 7"
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

This is the seventh part of the graph theory notes. We take a look at Planar Graphs.

The book followed throughout is: _Graph Theory with Applications_ by _Bondy J.A., Murty U.S.R._. Please refer to the book for examples as well as visual graph drawings.

---
---

# Planar Graphs

A graph is called `Planar` if it can be drawn in the plane so that its edges intersect only at their ends.

The vertices and edges of the graph partition (no overlap) the plane into several regions, each such region is called a `face`, denoted by $F_i$ for some $i \in \mathbb{N}$. The only unbound face which exists is the `outer` face, the others are termed as `inner` faces.

Two graphs $G_1,G_2$ are called `homeomorphic` if $G_1$ can be obtained by inserting some new **vertices** on $G_2$'s  edge. By this definition, inserting or deleting a number of 2-degree vertices does not change planarity.

Note that $K_5$ and $K_{3,3}$ are not planar (Can be proven by Theorem 1/2).

---

# Theorems

`Theorem 1[Euler's Formula]`: For a connected planar graph $G$ with $v$ vertice, $e$ edges and $f$ faces, then $$v - e + f = 2.$$

`Theorem 2`: For a connected simple planar graph $G$ with $v ~ (v \geqslant 3)$ vertices and $e$ edges, $$e \leqslant 3v - 6$$

This is an extension from Euler's Formula, obtained for maximizing edges in a simple planar graph. Theorem 2 also holds for disconnected simple planar graphs. It can also be used to determine if a graph is planar or not.

`Theorem 3[Kuratowski]`: A graph is planar if and only if it contains no subgraph homeomorphic to $K_5$ and $K_3,3$.

A neat proof can be found in the text mentioned above.

`Theorem 4[Kozyrev-Grinberg]`: If a planar graph has a Hamiltonian cycle $c$, let $f_{i}^{\prime}$ be the number of $i$-polygons inside $c$, and $f_{i}^{\prime \prime}$ be the number of $i$-polygons outside $c$, then
1. $1 \cdot f_{3}^{\prime}+2 \cdot f_{4}^{\prime}+3 \cdot f_{5}^{\prime}+\cdots=n-2$;
2. $1 \cdot f_{3}^{\prime \prime}+2 \cdot f_{4}^{\prime \prime}+3 \cdot f_{5}^{\prime \prime}+\cdots=n-2$;
3. $1 \cdot\left(f_{3}^{\prime}-f_{3}^{\prime \prime}\right)+2 \cdot\left(f_{4}^{\prime}-f_{4}^{\prime \prime}\right)+3 \cdot\left(f_{5}^{\prime}-f_{5}^{\prime \prime}\right)+\cdots=0$, where $n$ is the number of the vertices of $G$, and also the length of $c$.

# Questions

`1.` Prove that the $K_5$ and $K_3,3$ are not planar.

`2.` In a bus network there are $n$ stations. Each station is connected to at least 6 roads. Prove that there must be two roads intersecting on the plane.

`3.` Let $S=\lbrace x_{1}, x_{2}, \ldots, x_{n}\rbrace ~~   (n \geqslant 3)$ be the set of vertices on the plane. The distance between two arbitrary vertices is no less than 1. Prove that there are at most $3 n-6$ pairs of vertices whose distances are 1 .