---
tags: [terver, lecture9]
---

# Lecture 9. Binomial and geometric distribution

## Binomial distribution

$n$ independent trials, $A$ appears with probability $p$, $q=1-p$. The number of occurrences of $X$ has a distribution law:
$$P_n(m) = C_n^m\, p^m q^{n-m}, \qquad m=0,1,\ldots,n$$
This is the general term of the expansion of Newton's binomial $(p+q)^n$ - hence the name.

> [!example] Example - coat of arms with two rolls
> The coin is tossed 2 times, $p=q=1/2$. $X$ — number of coat of arms drops.
>$$P_2(2)=0{,}25,\quad P_2(1)=0{,}5,\quad P_2(0)=0{,}25$$
> Control: $0{,}25+0{,}5+0{,}25=1$.

## Geometric distribution

Trials continue until the **first** occurrence of the $A$ event (probability of $p$ in each). $X$ is the challenge number where $A$ first appeared:
$$P(X=k) = q^{k-1}p, \qquad k=1,2,\ldots$$
(geometric progression with first term $p$ and denominator $q$).

> [!example] Example - shots to hit
> $p=0{,}3$ (probability of hit), only 4 rounds. $X$ — number of spent cartridges.
>
> | $X$ | 1 | 2 | 3 | 4 |
> |---|---|---|---|---|
> | $P$ | 0.3 | 0.21 | 0.147 | 0.343 |
>
> ($P(X{=}4)$ includes both the case of four misses and a hit after three misses: $q^4+q^3p=q^3$.)

## Related notes
-[[00 Contents]]
- [[06 Bernoulli Formula]]
-[[08 Random Variables and Distribution Law]]
-[[10 Numerical Characteristics of Discrete Random Variables]]