+++
title = "Dirichlet's Approximation Theorem"
date = "2022-01-22"
author = "LeiMath"
tags = [
    "math_problems",
    "math_questions",
    "maths"
]
+++

I recently came across this question given in some olympiad paper and found it quite accessible, so here is the proof in all its glory after a lemma that will be in use.

By the way, all the theorem says is that as long as $p \geqslant 1$ we can approximate any real number to a rational number by some arbitary precision.

---

`Lemma`: Consider $n+1$ positive real numbers $x_0, x_1, x_2, x_3, \ldots, x_n$ all being in $[0,1)$ then for any $i \neq j$ and $i > j$ it so happens that $$\left | x_j - x_i \right | < \frac{1}{n}$$ for $i,j \in \mathbb{Z}^+$

_Proof._ Divide the interval $[0,1)$ into $n$ subintervals as $\displaystyle \left[0,\frac{1}{n}\right), \left[\frac{1}{n} , \frac{2}{n}\right), \ldots , \left [ \frac{n-1}{n} , 1 \right)$. Now by Pigeonhole Principle, there exists $i , j ~(0 \leqslant i < j \leqslant n)~ $ such that $x_i,x_j$ remain in one of the subintervals and hence the result $$ \displaystyle |x_j - x_i| < \frac{1}{n}$$ holds. $\blacksquare$


---


`Theorem[Dirichlet's Rational Approximation]`: Let $\alpha$ be a positive real number. Let $n$ be a positive integer. There exists $p,q \in \mathbb{Z}^+$ which satisfies $$\left|\alpha - \frac{q}{p}\right| \leqslant \frac{1}{np}$$ 

_Proof._ Consider the numbers $m_i = [i \alpha]$ for some $i \in \lbrace 1,2,3, \ldots \rbrace$ that means $m_i \leqslant i \alpha < m_i + 1$ or $0 \leqslant i \alpha - m_i < 1$. By the above lemma, there exists $k,l$ such that $0 \leqslant k < l \leqslant n$ for $\displaystyle \left | (l \alpha - m_l) - (k \alpha - m_k)\right | < \frac{1}{n}$. Rearranging this gives $\displaystyle \left | \alpha ( l - k) - (m_l - m_k) \right | < \frac{1}{n}$. Now let $p = l - k$ and $q = m_l - m_k$ then after subsituting (note the inequality change)  $$\left|\alpha - \frac{q}{p}\right| \leqslant \frac{1}{np}$$ $\blacksquare$

---

