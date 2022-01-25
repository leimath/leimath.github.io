+++
title = "A Result and a Theorem"
date = "2022-01-25"
author = "LeiMath"
tags = [
    "maths"
]
+++
I found this results while doing my favourite activity - skimming through old books at library :)
The first one is a result (n-above-a) and what follows is a theorem called `Pasting Theorem` in literature.

---

# n above a

Let $a$ be a fixed real number. Then - 

{{< image src="/assets/images/athares.png" alt="the limit" position="center" style="width:24em; height:7em;" >}}

_Proof:_ 

$$\text{Part I}$$

Suppose first that $0 < a < 1.$ It follows that ${1 \over a} > 1$ and so we may write $${1 \over a} = 1 + h \quad \text{where } h > 0$$

`[Lemma I]` Now note that if $-1 < a$ then it implies that $(1+a)^n \geqslant 1 + na$ for every positive integer $n$ (can be proven by induction). And now by Lemma I it follows that $$0 < a^n = {1 \over (1+h)^n} \leqslant {1 \over 1 + nh} < {1 \over h} \cdot {1 \over n}$$ Since the last term is convergent and coverges to ${1\over h} \cdot 0 = 0$, it follows by [Sandwich/Squeeze](https://en.wikipedia.org/wiki/Squeeze_theorem) Lemma that $\lim\limits_{n \to \infty} a^n = 0.$

$$\text{Part II}$$

If $-1 < a < 0$, then $$-|a|^n \leqslant a^n \leqslant |a|^n$$ and from the first part of the proof we get $$\lim\limits_{n \to \infty} |a|^n = 0 = \lim\limits_{n \to \infty} (-|a|^n)$$ and thus again by Sandwich Lemma we conclude that $\lim\limits_{n \to \infty} a^n = 0$.

Now it is easy to see that $\lbrace 0^n \rbrace \to 0$ and so this finishes the case for $|a| < 1$.

Also $\lbrace 1^n \rbrace \to 1$ is also understood. Since no neighbourhood of length 2 or less contains both $1$ and $-1$, it follows that the sequence $\lbrace(-1)^n\rbrace$ does not converge.

Lastly, if $|a| > 1$ then by Lemma I we have $$a^2n = [1 + (a^2 -1)]^n \geqslant 1 + n(a^2 - 1)$$ and so $\lbrace a^n \rbrace$ is unbounded and does not converge. $\blacksquare$

---

# Pasting Theorem

`[Pasting Theorem]` Let $[a, b] \subseteq \mathbb{R}$ and $[b, c] \subseteq \mathbb{R}$ be non-degenerate closed bounded intervals, and let $f:[a, b] \rightarrow \mathbb{R}$ and $g:[b, c] \rightarrow \mathbb{R}$ be functions. Let $h:[a, c] \rightarrow \mathbb{R}$ be defined by

{{< image src="/assets/images/athares2.png" alt="the limit" position="center" style="width:17em; height:3em;" >}}

If $f$ and $g$ are continuous, and if $f(b)=g(b)$, then $h$ is continuous.

Note that by **non-degenerate** interval we refer to intervals of the form $(a,b),(a,b],[a,b)$ or $[a,b]$ where necessarily $a < b$, or any unbounded interval.

The proof is left to the readers as it makes up for a good exercise.