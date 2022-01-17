+++
title = "My Graph Theory Notes - Part 5"
date = "2022-01-17"
author = "LeiMath"
tags = [
    "graph_theory",
    "graphs",
    "notes"
]
series = ["GT Notes"]
categories = [
    "graph_theory",
    "math",
]
+++

This is the fifth part of the graph theory notes. We take a look at Euler's Problem and its resolution in this post.

The book followed throughout is: _Graph Theory with Applications_ by _Bondy J.A., Murty U.S.R._. Please refer to the book for examples as well as visual graph drawings.

---
---

# Regarding the Konigsberg Problem

The entirety of the Konigsberg problem solved by Euler is covered at various places; Please refer to [here - for a audiovisual treatment](https://www.youtube.com/watch?v=nZwSo4vfw6c) or [here - for a full report on it.](https://www.maa.org/press/periodicals/convergence/leonard-eulers-solution-to-the-konigsberg-bridge-problem)

The key question that was put forward against Euler was: Can a traveler go through every bridge once and only once ?

His solution led to many theorems that came forward and is presented below.

---

# Eulerian Graphs

A `tour` of a graph $G$ is a closed walk that traverses each edge of $G$ **at least** once.
If a cycle in a graph traverses every edge of the graph **exactly** once then the cycle is termed as `Euler Tour` (old books also call it `Euler Trail` as well).
A graph where Euler tour is admitted is called a `Eulerian Graph`.

Note that in various instances a _chain_ is also referred to as a `walk`.
A `path` is any walk (or, chain) with distinct vertices.

---

# Theorems

`Theorem 1`: A finite graph $G$ is a chain or a cycle if and only if $G$ is connected and the number of vertices with odd degree in $G$ is equal to $2$ or $0$. When and only when the number of vertices with odd degrees in $G$ is equal to $0$, the connected graph $G$ is a cycle.

`Theorem 2`: If $G$ is a connected graph and has $2k$ odd vertices, then graph $G$ can be drawn by lifting one's pen $k$ times and at least $k$ times.

`Theorem 3`: A nonempty connected graph is Eulerian if and only if it has 
no vertices of odd degree.

`Theorem 4`: A connected graph has an Euler trail if and only if it has at 
most two vertices of odd-degree

Note: Some theorems are quite tricky, especially Theorem 1, and non-intuitive. Please refer to the book mentioned above for proofs else, skip them.

---

# Tactics

Along with previously discussed tactics, some extra ones are:

* `Coloring`: We try to divide the graph into subgraphs and see if keep some color invariant results in some concrete evaluation of data given in the question paired with the theorems presented above.
* `Principle of Least Action`: We try to generate a tour which requires the least _weightage_ (weightage can mean the degree value, moves set or any other restriction) and then try to see at cases which either maximize or minimize some condition respectively.

---

# Questions

`1.` Arrange $n$ vertices $v_{1}, v_{2}, \ldots, v_{n}$ in order on a line. Each vertex is colored in red or blue. If the ends of a segment $v_{i} v_{i+1}$ are colored differently, we call it a standard segment. Suppose the colors of $v_{1}$ and $v_{n}$ are different. Prove that the number of the standard segments is odd.

`2.` (CMC 5th) A graph which consists of a convex $n$-polygon and $n-3$ disjoint diagonal lines in the polygon is called a subdivision graph.
Prove that there exists a `subdivision graph` which is a cycle drawn without lifting one's pen (i. e. start from a vertex, go through each segment only once and return the starting point) if and only if $3 \mid n$. 

`3.` On an $8 \times 8$ chessboard with 64 black and white squares we move a knight. In whatever direction the knight moves, is it possible to make the knight move to all the squares and each square only once? (A knight moves from a corner square of a rectangle with $2 \times 3$ black and white squares to another corner square diagonal to the starting position.)