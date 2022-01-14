+++
title = "My Graph Theory Notes - Part 1"
date = "2022-01-13"
author = "LeiMath"
+++

This is a series of my notes on graph theory and usage in Scholarship Problems. We look at what a graph is today and present some terminologies. We also present some basic tactics to solve elementary problems. 

Following the tradition of this blog, we do not present any illustrations on using the tactics as it limits the readers to thinking about the problems only through a specific approach whereas in an exam environment multiple approaches and various combination of techniques is necessary.

---

# Graphs

A graph is a set of points with certain vertices joined by some edge. The graph represents a binary relationship.

When to look through a Graph Theoritic perspective ? Whenever there is a clear-cut distinction provided in the question as some "objects" and some "relationship" between the objects.

To represent such objects, we use a point and call it "vertex" and to signify the relationship between two vertex, we draw a line between them and call it an "edge". Whatever figure this generates, we call it a graph.

We present the proper definition just for the sake of completeness.

* Graph[Definition]: A graph is a triplet $(V,E,\varphi)$ where $V$ and $E$ are two disjoint sets, $V$ is non-empty and $\varphi$ is a mapping from $V \times V \to E.$ The set $V$ is the vertex set, $E$ is called the edge set an $\varphi$ is the incidence function.

* Rules for Graphs:

$\qquad$ [I] It is allowed that vertices and edges may not be in the same plane 

$\qquad$ [II] It is NOT allowed for an edge to pass through a third vertex

$\qquad$ [III] It is NOT allowed for an edge to intersect itself. 

---

For two graphs $G_1, G_2$ if there exists a bijection between the vertices of $G_1$ to $G_2$ such that the number of edges joining two points in $G_1$ equals the number the edges joining two in $G_2$, then we call such two graphs $G_1, G_2$ as `isomorphic`.

For a graph $G_0$ and $G_1$, if it is so that vertex and edge of $G_0$ is a subset of vertex and edge of $G_1$ then $G_0$ is called a `subgraph`.

Two points are `adjacent` if there is a edge joining them. A vertex is `incident` to edge if the vertex is the end of the edge. A vertex which has a edge joining itself to itself is called a `loop`. Two edges with same pair of vertex are called `parallel`. A graph is `simple` if it has no loops or parallel edges. A `complete` graph is a graph in which *every* two point are adjacent i.e they have a edge between them.

If $n$ is the number of vertices of a graph, the number of edges are $\binom{n}{2} = \frac{1}{2} n(n-1).$

A graph is `finite` if cardinality of vertices and edges are finite. If a graph has infinitely many vertices OR edges, then it is `infinite`.

---
# Tactics

A wide variety of questions can be tackled merely by the above definitions. The tactics to solve such problems are:

* `Reformulate the question` : This sounds simple enough but not always clicks to mind by a first look. After translating the question in graph theoritic terms and **constructing a graph**, a few too many questions are tremendously simplified to some form of logical argument or something to do with the data provided/inferred. 
* `Parity` : Somehow reach contradictions with even-odd arguments. Works best if the question already provides some concrete data on some variable bein even/odd. 
* `Coloring` : Usually works great when some form of trait is to be deonstrated among $2 + k$ objects. Then the problem can be reduced to showing monochromatic structure among these $2+k$ objects. 
* `Pigeonhole principle` :  If we put $n$ pigeons in less than $n$ pigeonholes, then at least one pigeonhole contains more than one pigeons. Simple enough to state, but it might take a while to frame the question to use this, the most apt use case is when paired with the above mention "coloring" strategy. 
* `Neighborhood Dragging` : We consider the neighbourhood (denoted by the set $N$) of two defined objects, or vertex (in the question) and then argue if a foreign object can be in it or not (usually depends on the question for partculars).
* `WLOG vertex` : In some instances where the graph isn't particularly defined well, we might WLOG assume a pair of vertex or an edge to exist.

---

# Questions

`1.` There are 50001 people in a party. Suppose that each of them shakes hands with at least one person. Prove that there must be someone who shakes hands with at least two persons.

`2.`  There are $n$ athelete who attend a meeting. For any four athelete, there is one person who has shaked hands with the other three. 
Prove that for any four athelete, there must be one person who 
shakes hands with the rest of the $n - 1$ athelete. 

`3.` [USAMO 1978] Nine mathematicians meet at an international mathematics conference. For any three persons, at least two of them can have a talk in the same language. If each mathematician can speak at most three languages, prove that at least three mathematicians can have a talk in the same language.

`4.` There are $n$ fruit boxes. Any two fruit box have the 
same kind of fruit inside and every kind of fruit is contained 
in just two fruit boxes. How many kinds of fruit are there?

`5.` In a bus with any $m$ travellers, $m \geqslant 3$, they have only one common friend. If $A$ is friends with $B$ then $B$ is friends with $A$, anyone is not a friend of ownself. How many people are there in the carriage ? 

$$\dots$$


In the next post we look at Degree of a Vertex and other related topics.