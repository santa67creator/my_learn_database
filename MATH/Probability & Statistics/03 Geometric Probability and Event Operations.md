---
tags: [terver, lecture3]
---

# Lecture 3. Geometric probabilities. Operations on events

## Geometric probability

The classical definition is not applicable to tests with an infinite number of outcomes - a geometric probability is introduced (a point falling into a region).

Section: $\displaystyle P = \frac{\text{length } l}{\text{length } L}$

Flat figure: $\displaystyle P = \frac{S_g}{S_G}$

> [!example] Example - a point on a segment
> On the segment $OA$ of length $L$, the point $B$ is placed at random. Find the probability that the smaller of the segments $OB$ and $BA$ is longer than $L/3$.
>$$P = \frac{L/3}{L} = \frac{1}{3}$$

> [!example] Example - a circle inscribed in a square
> A point is thrown into a square with a side equal to the diameter of the inscribed circle. Find the probability of getting into the circle.
>$$P = \frac{S_{\text{circle}}}{S_{\text{square}}} = \frac{\pi R^2}{4R^2} = \frac{\pi}{4} \approx 0{,}785$$

## Operations on events

- **Sum** $C = A+B$ - the offensive of $A$, or $B$, or both (union of sets).
- **Product** $C = A \cdot B$ - joint offensive of $A$ and $B$ (intersection of sets).

## Theorem for adding probabilities of incompatible events

$$P(A+B) = P(A) + P(B)$$
$$P(A_1+A_2+\ldots+A_n) = P(A_1)+P(A_2)+\ldots+P(A_n)$$

Corollary: for opposite events $p+q=1$; for a complete group of incompatible events, the sum of the probabilities is equal to 1.

> [!example] Example - trolleybus
> Of the 40 trolleybuses, 8 are on route No. 3 and 10 are on route No. 11. Find the probability that the first person to arrive is on the desired route.
>$$P(A)=\frac{8}{40}=\frac{1}{5},\quad P(B)=\frac{10}{40}=\frac{1}{4}$$
>$$P(A+B) = \frac{1}{5}+\frac{1}{4} = \frac{9}{20}$$

## Conditional probability and multiplication theorem

**Conditional probability** $P_A(B)$ (or $P(B/A)$) - the probability of $B$ provided that $A$ has already occurred.

For **dependent** events:
$$P(AB) = P(A)\cdot P(B/A)$$

For **independent** events ($P(B/A)=P(B)$):
$$P(AB) = P(A)\cdot P(B)$$

For three events: $P(ABC) = P(A)P(B/A)P(C/AB)$ (dependent) or $P(ABC)=P(A)P(B)P(C)$ (independent).

> [!example] Example - balls with and without return
> Urn with 12 balls, 7 white. Find the probability of drawing the white ball twice.
> **a) welcome back** (independent events):
>$$P(AB) = \frac{7}{12}\cdot\frac{7}{12} = \frac{49}{144} \approx 0{,}34$$
> **b) without return** (dependent events, $P(B/A)=6/11$):
> $$P(AB) = \frac{7}{12}\cdot\frac{6}{11} = \frac{7}{22} \approx 0{,}3$$

## Related notes
- [[00 Contents]]
- [[04 Consequences of Addition and Multiplication Theorems]]