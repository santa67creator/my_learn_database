---
tags: [terver, lecture5, Bayes]
---

# Lecture 5. Total probability formula. Bayes formula

## Total probability formula

Let $H_1, H_2, \ldots, H_n$ be a complete group of incompatible hypotheses, and the event $A$ can occur only with one of them:
$$P(A) = \sum_{i=1}^{n} P(H_i)\, P_{H_i}(A)$$

> [!example] Example - ball in urn
> A white ball is dropped into an urn with 2 balls, one ball is drawn at random. Hypotheses about the original composition: $H_1$ (no white ones), $H_2$ (one white one), $H_3$ (two white ones), each with $P(H_i)=1/3$.
> Conditional probabilities: $P_{H_1}(A)=1/3,\; P_{H_2}(A)=2/3,\; P_{H_3}(A)=1$.
>$$P(A) = \frac13\cdot\frac13+\frac13\cdot\frac23+\frac13\cdot1 = \frac23$$

## Bayes formula

If the event $A$ has already occurred, the conditional probability of the hypothesis $H_i$ is recalculated:
$$P_A(H_i) = \frac{P(H_i)\,P_{H_i}(A)}{\displaystyle\sum_{j=1}^{n} P(H_j)\,P_{H_j}(A)}$$

> [!example] Example - specialists and reliability of the device
> 30% of the devices are assembled by a highly qualified specialist ($P(H_1)=0{,}3$, reliability $P_{H_1}(A)=0{,}9$), 70% - average ($P(H_2)=0{,}7$, reliability $P_{H_2}(A)=0{,}8$). The device turned out to be reliable - find the probability that it was assembled by a highly qualified specialist.
>$$P_A(H_1) = \frac{0{,}3\cdot0{,}9}{0{,}3\cdot0{,}9+0{,}7\cdot0{,}8} = \frac{0{,}27}{0{,}83} \approx 0{,}325$$
> (respectively $P_A(H_2)\approx0{,}675$)

> [!example] Example - two tanks
> The probability of hitting a target with the first tank is 0.8, with the second - 0.4. The target is hit with one hit. Find the probability that it was the first tank that was hit.
> Hypotheses: $H_1$ (hit 1st, not 2nd): $P=0{,}8\cdot0{,}6=0{,}48$; $H_2$ (hit 2nd, not 1st): $P=0{,}2\cdot0{,}4=0{,}08$; under both hypotheses $A$ occurs.
>$$P_A(H_1) = \frac{0{,}48}{0{,}48+0{,}08} \approx 0{,}857 \;(6/7)$$

## Related notes
-[[00 Contents]]
- [[04 Consequences of Addition and Multiplication Theorems]]
-[[06 Bernoulli Formula]]