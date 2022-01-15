+++
title = "My Graph Theory Notes - Part 2"
date = "2022-01-14"
author = "LeiMath"
+++

The book followed throughout is: _Graph Theory with Applications_ by _Bondy J.A., Murty U.S.R._. Please refer to the book for examples as well as visual graph drawings.


# Degree of a Vertex

The `degree` of a vertex $v$ in a graph $G$, denoted by $d_G(v)$ (or simply, $d(v)$ if the context of graph is clear), is the number of edges incident ot $v$ of $G$. Each loop is counted as two edges. $\delta(G)$ and $\Delta(G)$ are used to represent the minimum and maximum degrees of the vertices of $G$ respectively. A vertex is odd if the degree is odd, else it is even.

Let $G(V,E)$ be a graph where $V,E$ are the vertex and edge set respectively. If it happens that for ALL vertex $v$, $d(v) = k$ for some $k$, then the graph $G$ is called `k-regular`. The complete graph on $n$ vertices is $(n-1)$ regular.

Theorem[I]: For any graph $G$ with $n$ vertices, the sum of degrees of all the vertices is twice as large as the number of edges. In symbols, if the $n$ vertices are $V = \lbrace v_1, v_2, \dots, v_n \rbrace$ then $$\sum\limits_{k = 1}^n d(v_k) = 2 |E|$$

This is popularly known as the `Hand-Shaking Lemma`.

Theorem[II]: In any *finite* graph $G$, the number of vertices with odd degree is even.

Theorem[III]: A vertex is at most adjacent to other $n-1$ vertices in a simple graph on $n$ vertices i.e $$d(v) \leqslant n-1$$ for all $v \in V.$

---

Let there be $n$ vertices of type $x$ all contained in the set $X$ i.e, $X = \lbrace x_1, x_2, \dots, x_n \rbrace$ and $m$  vertices of type $y$ in $Y$ as $Y = \lbrace y_1, y_2, \dots, y_m\rbrace$ then $X \cap Y = \phi$ and if we connect $x_i$ with $y_i$ if a relationship exists then an edge $(x_i, y_i)$ is formed. This graph $G$ is called a `bipartite` graph, or `even` graph and is denoted by $G = (X,Y; E)$

If $G$ is a simple graph on $n$ vertices, then if we generate a graph by deleting all the edges belonging to $G$ from the complete graph $K_n$, this is called the `complementary` graph of G, denoted by $\bar{G}$.


---

# Tactics

* Looking for some contradiction with the use of Hand-Shaking Lemma.
* Selectively looking for what the degree of a vertex value can be.
* Looking at the subgraph by deleting some edges, vertices and then reaching some contradiction.
* Getting bounds on the degree of all vertex values.
* Viewing $d(v)$ as some algebraic object to use inequalities in it.

---

# Questions

`1.`  Show that at any party, there are always at least two people with exactly the
same number of friends at the party.

`2.` A cube with edge of length $n$ is cut into $n^3$ unit cubes by planes parallel to  its sides. How many pairs of unit cubes whose common vertices are no more than $2$ are there? 

`3.` There are $n$ points on the plane. Prove that the number of pairs of points whose distance is $1$ would not exceed $$\frac{n}{4} + \frac{\sqrt{2}}{2}n^{\frac{3}{2}}$$