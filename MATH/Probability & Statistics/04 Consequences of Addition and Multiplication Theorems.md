---
tags: [terver, lecture4]
---

# Lecture 4. Corollaries from the theorems of addition and multiplication of probabilities

## Probability of at least one event occurring

If $A_1, A_2, \ldots, A_n$ are independent in aggregate, with the probabilities of opposite events $q_1, q_2, \ldots, q_n$:
$$P(A) = 1 - q_1 q_2 \cdots q_n$$
If all probabilities are equal to $p$ (meaning $q$ is the same):
$$P(A) = 1 - q^n$$

> [!example] Example - a chain of three elements
> Failure probabilities: $p_1=0{,}1$, $p_2=0{,}15$, $p_3=0{,}2$. Find the probability that there will be no current (at least one element will fail).
>$$P(A) = 1-(1-0{,}1)(1-0{,}15)(1-0{,}2) = 0{,}388$$

> [!example] Example - lottery tickets
> The probability of winning on a ticket is 0.15. Find the probability of winning at least one of 4 tickets.
>$$P(A) = 1-(0{,}85)^4 = 0{,}5563$$

## Theorem for adding probabilities of joint events

$$P(A+B) = P(A) + P(B) - P(AB)$$

> [!example] Example - dice
> Find the probability that an even number or a multiple of three will be rolled.
> $P(A)=1/2$ (even), $P(B)=1/3$ (multiples of 3), $P(AB)=1/6$ (the number 6 is both even and a multiple of 3).
>$$P(C) = \frac12+\frac13-\frac16 = \frac23$$

## Related notes
- [[00 Contents]]
- [[03 Geometric Probability and Event Operations]]
- [[05 Total Probability and Bayes]]