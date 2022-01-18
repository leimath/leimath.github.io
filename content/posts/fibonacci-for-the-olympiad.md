+++
title = "Fibonacci For the Olympiad"
date = "2022-01-03"
author = "LeiMath"
tags = [
    "fibonacci",
    "olympiads",
    "maths"
]
+++


Often-a-while fibonacci sequence problems stars as the guest problem in olympiad exam papers and often the solution is hidden from the untrained eye as some form of application of its properties. 
This article assumes familiarity with the definition of the "Fibonacci Sequence" and the ability to comprehend recursive definitions at the minimum.

We will present various properties related to Fibonacci Numbers (and related) without any proof. It is the interest of the reader to seek out the proofs and validate each result for their own.

----

# Definitions

For the sake of recourse, we present the defintions -

Fibonacci Sequence : A sequence of integers $F_1, F_2, \cdots$ such that $F_{n+2} = F_{n+1} + F_n$ for all $n \geqslant 1$, with, $F_1 = F_2 = 1$. 

-- The first few terms are : $1,1,2,3,5,8,13,21,34,55,89,144, \cdots$

Golden Ratio: $\phi =	\frac{1+\sqrt{5}}{2}$

Lucas Sequence: A sequence of integers with $L_0 = 2, L_1 = 1$ such that $L_n = L_{n-2} + L_{n-1}$ for all $n \geqslant 1$.

$G_n$: The ratio of two successive term in the Fibonacci Sequence, i.e, $\displaystyle G_n = \frac{F_{n+1}}{F_n}$

----

# Binet's Formula

$$F_{n}=\frac{1}{\sqrt{5}}\left(\frac{\sqrt{5}+1}{2}\right)^{n}-\frac{(-1)^{n}}{\sqrt{5}}\left(\frac{\sqrt{5}-1}{2}\right)^{n}$$

for $n \geq 0$.


---

# Properties


1. (Strong Divisibility) $$\operatorname{gcd}(F_n,F_m)= F_{\operatorname{gcd}(n,m)}$$
   (GCD Rule) $$\operatorname{gcd}\left(F_{n}, F_{n-1}\right)=1$$
2. (Divisibility Sequence) $$m \mid n \implies F_m \mid F_n$$
3. (Cassini's Identity) $$F_{n+1}^{2}-F_{n+2} F_{n}=(-1)^{n}$$
4. (Forward Jump Identity) $$F_{n+1} = \sum\limits_{k=0}^n \binom{n-k}{k}$$
5. (Parity[I]) If $n$ is even, then $F_n$ is an odd number.
   
   (Parity[II]) If $F_n$ is even if and only if $n$ is divisible by $3$
6. (Lucas Identity) $$F_n^2+F_{n+1}^2 = F_{2n+1}  $$
7. (Fibonacci Generating Function) $$\sum_{n=1}^{\infty} F_{n} x^{n}=\frac{x}{1-x-x^{2}}$$
8. (Finite Sum) $$F_1 + F_2 + F_3 + F_4 + \cdots + F_n = F_{n+2} - 1$$
9. (Balls and Urns Formulation) $$F_n=\sum\limits_{k=0}^{n-1} \binom{n-k-1}{k} \text{ or, } 	\sum\limits_{k=1}^{n}\binom{n-k}{k-1} $$ 
10. (Fibonacci Limit Theorem) $$\lim\limits_{n \to \infty} \frac{F_{n+1}}{F_n} = \phi$$ 
11. (Gap Telescope) $$\frac 1{F_{n-1}F_{n+1}}=\frac 1{F_{n-1}F_n}-\frac 1{F_nF_{n+1}}$$
12. (Difference Rule) $$F_nF_{n+1}=F_n^2+F_{n-1}F_n$$
13. (Square Sum) $$\sum_{k=1}^{n}F_{k}^{2}=F_{n}F_{n+1}$$
14. (Double Sum)$$F_{m}F_{n+1} + F_{m-1}F_{n} = F_{n+m}$$
15. (Triple Sum) $$F_a F_{a+b+c}-F_{a+b}F_{a+c}=(-1)^{a+1} F_b F_c$$
16. (First Form Inequality) $$F_k > F_{k-2}+F_{k-3}+\ldots+F_2$$
17. (n-odd-even Equality)$$F_2+F_3+F_5+\ldots+F_{2k-1} = F_{2k}$$
 

--- 

# Fact File

Fact 1: The only Fibonacci numbers that are squares are $0, 1, 144.$ 

// Proof: https://math.la.asu.edu/~checkman/SquareFibonacci.html#intro

Fact 2: Every positive integer $m$, there is a Fibonacci number divisible by $m$.

// Proof: https://math.stackexchange.com/questions/1523198/proving-that-every-integer-has-a-fibonacci-number-multiple (also see, https://artofproblemsolving.com/community/c6h2231614p17047441)



---

# Theorems

* Theorem[Zeckendorf]: Every positive integer can be represented `uniquely` as the sum of one or more Fibonacci numbers in such a way that the sum does not include any two consecutive Fibonacci numbers.

* Theorem[Counting]: 

   + $F_{n}$ is the number of binary sequences of length $n-2$ with no consecutive 0 s.
   + $F_{n}$ is the number of subsets of ${1,2, \ldots, n-2}$ that do not contain any pair of consecutive numbers.

*  Theorem: All the odd divisors of Fibonacci numbers with odd subscripts are of
the form $4t + 1$

---

# The Proof of a Theorem

Theorem: Let $r \in \mathbb{N}$. The Fibonacci numbers modulo $r$ form a periodic sequence.

Proof: 

The total number of possible pairs $\left(F_{i} \bmod r, F_{i+1} \bmod r\right)$ is $r^{2}$. Therefore some ordered pair must occur more than once, so pick one that repeats and label it $n$ and $n+j$; that is,
$$
\left(F_{n} \bmod r, F_{n+1} \bmod r\right)=\left(F_{n+j} \bmod r, F_{n+j+1} \bmod r\right) .
$$
Then induction on $k \geq 2$ and using the recurrence for the Fibonacci numbers show that $F_{n+k} \bmod r=F_{n+k+j} \bmod r$. Therefore the sequence $F_{n} \bmod r$ is periodic. $\blacksquare$

This above theorem while may or may not be useful, has seen usage because of the proof. The idea of finite pairs of remainders and that eventually some remainder of index values will repeat has been used in question based on divisibility sequences.

---

# Questions

Key: [D] means Very Difficult. [E] means Easy. [M] means Moderate. [E-M] means between Easy to Moderate. Difficulty grading is ofcourse relative.

`1.` [E] Prove that if $a_{n}=F_{2 n-1}, b_{n}=2 F_{n} F_{n-1}$, and $c_{n}=F_{n}^{2}-F_{n-1}^{2}$, then $a_{n}^{2}=b_{n}^{2}+c_{n}^{2} .$

`2.` [D] [IMO Longlist 1974 2] Let $\lbrace u_{n}\rbrace$ be the Fibonacci sequence, i.e., $u_{0}=0, u_{1}=1$, $u_{n}=u_{n-1}+u_{n-2}$ for $n>1$. Prove that there exist infinitely many prime numbers $p$ that divide $u_{p-1}$.

`3.` [D] Prove that, for every $n \in \mathbb{N}$, we have
$$
\sum_{j=1}^{n}\left(\begin{array}{l}
n \\
j
\end{array}\right) F_{2 n+1-j}=F_{2 n+1}-1,
$$
where $F_{k}$ is the $k$-th Fibonacci number.

`4.` [M] Let $F_{n}$ be the $n^{\text {th }}$ Fibonacci number defined by $F_{1}=F_{2}=1$ and $F_{n+2}=F_{n+1}+F_{n}$ for $n \in \mathbb{N}$. Prove that
$$
\sum_{k=0}^{n}\left(\begin{array}{c}
n-k+1 \\
k
\end{array}\right)=F_{n+2}
$$

`5.` [E-M] Prove
$$
f_{n}^{4}-f_{n-2} f_{n-1} f_{n+1} f_{n+2}=1, \quad n \geq 3
$$

Note: The identity in `5.` is called the `Gelin-Cesàro` identity.

$$\dots$$
