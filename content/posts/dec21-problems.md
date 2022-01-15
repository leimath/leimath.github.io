+++
title = "Problems from December '21"
date = "2022-01-12"
author = "LeiMath"
+++

`1.` 

It is asked to show that $10^r \equiv 1 \operatorname{mod} p$ or, $10^r - 1 = pk$ for some $k \in \mathbb{Z}$

-----

Let $\overline{a_1a_2a_3a_4\dots a_r} = \mathcal{F}$ and $a_1a_2\dots a_r = \mathcal{I} \in \mathbb{Z}$
Consider $$\frac{10^r - 1}{p} = \frac{10^r}{p} - \frac{1}{p} \\ = \mathcal{I} . \mathcal{F} - 0.\mathcal{F} = \mathcal{I}$$ where the $``."$ represents the decimal period sign. Therefore $\frac{10^r - 1}{p} = \mathcal{I} \implies 10^r - 1 = p \mathcal{I}$ and thus $10^r \equiv 1 \operatorname{mod} p$. Hence proved. $\diamondsuit$