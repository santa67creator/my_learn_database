---
tags: [terver, lecture 15, mathematical_statistics]
---

# Lecture 15. Statistical sampling distribution

## Basic concepts

- **Options** $x_i$ — observed values of the $X$ trait.
- **Variation series** - options written in ascending order.
- **Statistical distribution of the sample** - a list of variants $x_i$ and their corresponding frequencies $n_i$ (sum of all $n_i$ = sample size $n$) or relative frequencies $\omega_i = n_i/n$ (sum of $\omega_i = 1$).

> [!example] Example - frequencies → relative frequencies
> | $x_i$ | 2 | 5 | 7 |
> |---|---|---|---|
> | $n_i$ | 1 | 3 | 6 |
>
> Sample size $n=10$. Relative frequencies: $\omega_1=0{,}1,\ \omega_2=0{,}3,\ \omega_3=0{,}6$.

## Empirical distribution function

$$F^*(x) = \frac{n_x}{n}$$
where $n_x$ is the number of options less than $x$.

**Properties:**
1. $0 \le F^*(x) \le 1$
2. $F^*(x)$ does not decrease
3. $F^*(x)=0$ with $x \le x_1$ (smallest option), $F^*(x)=1$ with $x > x_k$ (largest)

> [!example] Example
> | $x_i$ | 1 | 4 | 6 |
> |---|---|---|---|
> | $n_i$ | 10 | 15 | 25 |
>
>$n=50$.
> $$F^*(x)=\begin{cases}0,& x\le1\\ 0{,}2,& 1<x\le4\\ 0{,}5,& 4<x\le6\\ 1,& x>6\end{cases}$$

## Polygon and histogram

- **Frequency polygon** - a broken line through the points $(x_i, n_i)$ (for a discrete characteristic).
- **Relative frequency polygon** - broken line through $(x_i, \omega_i)$.
- **Frequency histogram** (for a continuous feature) - rectangles at partial intervals of length $h$, height $n_i/h$; area = sample volume $n$.
- **Histogram of relative frequencies** - height $\omega_i/h$; area = 1.

## Related notes
-[[00 Contents]]
- [[14 Normal and Exponential Distributions]]
- [[08 Random Variables and Distribution Law]] - compare with the law of distribution of SV