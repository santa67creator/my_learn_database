---
tags: [terver, lecture6, Bernoulli]
---

# Lecture 6. Repeated independent tests. Bernoulli's formula

Trials are independent with respect to the $A$ event if the probability of $A$ occurring in each trial does not depend on the outcomes of the others.

## Bernoulli formula

The probability that during $n$ independent trials the event $A$ (with probability $p$ in each, $q=1-p$) will appear exactly $m$ times:
$$P_n(m) = C_n^m\, p^m q^{n-m}$$

> [!example] Example - 5 hits out of 6
> Chance to hit when shooting $p=0{,}8$. Find the probability of exactly 5 hits with 6 shots.
>$$P_6(5) = C_6^5 (0{,}8)^5(0{,}2)^1 = 6\cdot(0{,}8)^5\cdot0{,}2 \approx 0{,}3932$$

> [!example] Example - no more than two defective
> Defects - 30%. Out of 7 taken bars, find the probability that no more than two will be without defects ($p=0{,}7$ block without a defect).
>$$P_7(\le2) = P_7(0)+P_7(1)+P_7(2) \approx 0{,}0288$$

## Most likely number of occurrences of the event $m_0$

$$np - q \le m_0 \le np + p$$

> [!example] Example 1 - 50 shots
> $n=50$, $p=0{,}9$, $q=0{,}1$: $44{,}9 \le m_0 \le 45{,}9 \Rightarrow m_0=45$.

> [!example] Example 2 - inverse problem
> At what $n$ is the most likely number of hits of $m_0=16$, if $p=0{,}7$?
> Solving the double inequality $0{,}7n-0{,}3\le16\le0{,}7n+0{,}7$, we get $n=22$ or $n=23$.

## Related notes
-[[00 Contents]]
- [[05 Total Probability and Bayes]]
- [[07 Poisson Formula and Laplace Theorems]] — approximations of the Bernoulli formula for large $n$
- [[09 Binomial and Geometric Distribution]] - the same formula as the distribution law