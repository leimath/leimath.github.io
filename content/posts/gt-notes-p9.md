+++
title = "My Graph Theory Notes - Part 9"
date = "2022-01-20"
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


This is the final part of the graph theory notes. We take a look at Tournaments.

---

# Tournaments

So far all the graphs encountered were `undirected` that is, none of the edges that stood for "relationship" between two vertex had any direction. If we attach some directional information to an edge, then the graph is called a `directed` graph. Let the directional information be represented by an arrow which points _to_ a vertex _from_ another vertex, the _from_ side has the arrow and is called an `arc` in literature. If there is an arc from $v_i$ to $v_j$ then the pair is represented as $(v_i,v_j)$ and the order is fixed. A directed graph is represented as $G = (V,U)$ where the $V$ stands for the usual vertex set and $U$ stands for the arc set composed of directed pairs like $(v_i,v_j)$ etc if an arc exists. The directed graph also follow the _simple_ nature. 

The number of arcs which have the starting point from $v_i$ have a name, `outdegree` represented by $d^{\star}(v_i)$. Similarly the number of arcs whose arrow points to $v_i$ also have a name, `indegree` represented by $d^{\circ}(v)$.

We call a directed graph a `tournament` if the graph contains $n$ vertices and there is only one arc joining every two vertices. We denote the directed graph by $\overline{K_n}$.


In a directed graph $D = (V,U)$ let there exist distinct arcs $u_i$. If the starting point of $u_i$ is $v_i$ and endpoint of $u_i$ is $v_{i+1}$ for $i \in \lbrace 1,2,3, \ldots , n \rbrace $ then $n$ is called the length of the directed path from $v_1$ to $v_{n+1}$, and if $v_1 = v_{n+1}$ then this path is called a circuit.

---

# Theorems

`Theorem 1`: Let $v_i$ be the vertices of a tournament $\overline{K_n}$ for $i \in \lbrace 1,2,3, \ldots \rbrace$ then, $$\sum\limits_{k=1}^n d^{\star}(v_k) = \sum\limits_{k=1}^n d^{\circ}(v_k) = \frac{1}{2} n (n-1)$$

`Theorem 2`: There exists a vertex in a tournament so that there is a path from it to any other vertices. The maximum length of the paths is 2.

`Theorem 3`: If the vertex of $\overline{K_n}$ with maximum outdegree is unique, then this outdegree is $n-1$.

`Theorem 4`: Tournament $\overline{K_n}$ contains a Hamiltonian path whose length is $n-1$.

`Theorem 5`: The tournament $\overline{K_n}$ for $n \geqslant 3$ contains a circuit which is a triangle, if and only if there are two vertices $v,v^{\prime}$ which satisfy $$d^{\star}(v) = d^{\circ}(v^{\prime})$$

---

# Questions

`1.` Prove that if a tournament $\overline{K_n}$ contains a circuit, then $\overline{K_n} contains a triangular circuit.

`2.` There are $100$ species of insects. Among every two of them 
there is one species who can eliminate another species. (But A 
eliminates B, B eliminates C, which does not mean that A eliminates 
C . ) Prove that the $100$ species of insects can be arranged in an order so 
that any species can perish another species next to it. 