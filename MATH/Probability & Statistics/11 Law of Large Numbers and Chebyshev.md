---
tags: [terver, lecture 11, Chebyshev]
---

# Lecture 11. The law of large numbers. Chebyshev's theorem

## Chebyshev's inequality

$$P\big(|X-M(X)|<\varepsilon\big) \ge 1 - \frac{D(X)}{\varepsilon^2}$$

## Chebyshev's theorem

If $X_1, X_2, \ldots$ are pairwise independent SVs with uniformly bounded variances ($\le C$), then with $n\to\infty$ for any $\varepsilon>0$:
$$P\left(\left|\frac{X_1+\ldots+X_n}{n} - \frac{M(X_1)+\ldots+M(X_n)}{n}\right| < \varepsilon\right) \to 1$$
That is the arithmetic average of a large number of independent SVs is almost no different from their average. expectations.

> [!example] Example - estimate using Chebyshev's inequality
> | $X$ | 0.3 | 0.6 |
> |---|---|---|
> | $p$ | 0.2 | 0.8 |
>
> $M(X)=0{,}54$, $D(X)=0{,}0144$. Estimate $P(|X-M(X)|<0{,}2)$ using the Chebyshev inequality.

## Distribution function $F(x)$

$$F(x) = P(X<x)$$
(“integral function”). Defined for any SV - both discrete and continuous.

**Properties:**
1. $0 \le F(x) \le 1$
2. $F(x)$ does not decrease: $F(x_2)\ge F(x_1)$ with $x_2>x_1$
3. If all values are $X \in (a;b)$: $F(x)=0$ for $x\le a$, $F(x)=1$ for $x\ge b$
4.$\lim_{x\to-\infty}F(x)=0,\quad \lim_{x\to\infty}F(x)=1$

Consequence: $P(a\le X<b) = F(b)-F(a)$; for continuous CB $P(X{=}c)=0$.

> [!example] Example - calculating probability using $F(x)$
>$$F(x)=\begin{cases}0, & x\le-1\\ \dfrac{x}{4}+\dfrac14, & -1<x\le3\\ 1, & x>3\end{cases}$$
>$$P(0<X<2) = F(2)-F(0) = \frac34-\frac14=\frac12$$

## Related notes
- [[00 Contents]]
- [[10 Numerical Characteristics of Discrete Random Variables]]
- [[12 Probability Density]]