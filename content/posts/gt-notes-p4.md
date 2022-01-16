+++
title = "My Graph Theory Notes - Part 4"
date = "2022-01-16"
author = "LeiMath"
tags = [
    "graph_theory",
    "graphs",
    "notes",
]
categories = [
    "graph_theory",
    "math",
]
series = ["GT Notes"]
+++


This is the fourth part of the graph theory notes. We take a look at Trees.

The book followed throughout is: _Graph Theory with Applications_ by _Bondy J.A., Murty U.S.R._. Please refer to the book for examples as well as visual graph drawings.

---
---

# Trees

Before introducing trees, here are some essential terminologies:

Let $G$ be a graph and its edges are $e_1,e_2,e_3,e_4,\ldots,e_m$

1. If edge $e_i = (v_{i-1},v_i)$ for $i = 1,2,3, \ldots, m$ then we call the sequence a `chain` from $v_0$ and $v_m$. It is denoted as $v_0v_1\ldots v_m$
2. $m$ is called the `length` of the chain.
3. If $v_0$ and $v_m$ are the same, then the chain is called a `cycle`. Note that the proper definition for a cycle requires all $v_i$ , $i \in \lbrace 2,m-1 \rbrace$ to be distinct and $v_0 = v_m$ however we do not use the distinctness part for use in these notes for simplicity.
4. If a graph is not cyclic then it is called acyclic.
5. If a chain exists between **ANY** two vertices, then the graph is called connected, else the graph is disconnected.

$$\dotsb$$

A connected graph which contains no cycle (i.e, acyclic) is called a `tree`. It is denoted by $T$. By definition, tree is a simple graph. A tree can be used to construct a graph with more than $n-1$ edges, hence such a tree is called `generating tree` of the graph.

A graph without circles must be composed of one or more trees whose vertices are disjoint, such a graph is called a `forest`.

The vertex of a tree which has degree 1 is called a `leaf` or a `pendant vertex`.

---

# Theorems

`Theorem 1`: If a tree has no less than two vertices, then it has at least two leaves (pendant vertices).

_Proof 1_ : Suppose we start from some vertex $u$, along the edges of $T$, every edge can only be passed by once. Since a tree has no cycle, it cannot return to the vertices which have been passed. It means that each vertex can be passed at most once. If the vertex we pass is not a pendant vertex, because its degree is more than 1 , we can continue. But the number of vertices of $T$ is finite, so it is impossible to continue forever. If we cannot continue further at $v$, then $v$ is a pendant vertex.
We start from a pendant vertex $v$ and we can end up at another pendant vertex $v^{\prime}$. So tree $T$ has at least two pendant vertices.

_Proof 2_ : Assume that $\mu=u v_{1} v_{2} \cdots v_{k} v$ is the longest chain of $T$, we can show that $d(u)=d(v)=1$, i.e. $u, v$ are pendant vertices.
In fact, if $d(u) \geqslant 2$, then there exists vertex $w\left(w \neq v_{1}\right)$ adjacent to $u$. If $w$ is one of $v_{2}, \ldots, v_{k}, v$, then a cycle occurs. It contradicts the definition of tree. If $w$ is different from $v_{2}, \ldots, v_{k}$, $v$, then $w u v_{1} \cdots v_{k} v$ is a chain longer than $\mu$, a contradiction. So $d(u)=1$. Similarly, $d(v)=1$. Hence tree $T$ has at least two pendant vertices.

$$\dotsb$$

`Theorem 2[Pösá]` Let $V$ be the set of all the vertices of $G, E$ the set of all the edges of $G$. Prove that if $|E| \geqslant|V|+4$, then there must be two cycles which have no common edges.

$$\dotsb$$

`Theorem 3`: Let $n$ be the number of vertices of $T$, then the number of edges of $T$ is $n - 1$.

$$\dotsb$$

`Theorem 4`: Let $T$ be a graph with $n$ vertices and $e$ edges. Then the following three propositions are equivalent:

* $T$ is a tree
* $T$ has no cycle, and edges of $T$ equal $n-1$
* $T$ is connected, and edges of $T$ equal $n-1$

$$\dotsb$$

`Theorem 5`: If $T$ is a tree then $T$ is connected, but after deleting any edge of $T$, the obtained graph $G$ is disconnected.

`Corollary`: If $T$ is a tree and $T$ then after adding an edge the obtained graph contains only one unique cycle.

$$\dotsb$$

`Optimization of Tree`: Tree is a graph with the least number of edges. Tree is also a graph without a cycle which the has the most possible number of edges.

`Theorem 6`: In any graph $G$, let $e$ denote the number of edges and $n$ be the number of vertices. If $e < n - 1$ then $G$ is disconnected. If $e > n -1$ then $G$ must have a cycle

$$\dotsb$$

`Theorem 7`: If there is only one chain between any two vertices of $T$ then $T$ must be a tree.


---

# Tactics


* `Proof by construction`: Theorem 1 Proof 1 is an example. It can be employed when the given question is intuitvely obvious enough.
* `Longest Chain Method`: Theorem 2 Proof 2 is an example. It relies on the principles of Neighbourhood Dragging (more accurately, the reverse principle of neighbourhood dragging) as discussed in Part 1 of the notes. We pick an element and argue if the neighbours belong in the chain or not to reach some sort of contradiction.

---

# Questions

`1.` Prove Pösá's Theorem (Theorem 2 above).

`2.` [USAMO 1986] In a lecture, there are five mathematicians. Each of them took a nap twice and every two of them took naps at the same time. Prove that there must be three persons who took naps at the same time.

`3.` Given a number table with $n$ rows and $n$ columns, every two rows are different. Prove that there must exist a column, after deleting it, every two rows are still different.

`4.` [CMC 1987] $n(n>3)$ table tennis players play several single games. The opponents of any two players are different. Prove that we can remove one player so that the opponents of any two players in the remaining players are still different. 

`5.` If a graph $G$ has $n$ vertices and $n-1$ edges, then $G$ is a tree. Prove or disprove.