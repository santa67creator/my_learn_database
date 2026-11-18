---
tags: [terver, lecture13]
---

# Lecture 13. Numerical characteristics of a continuous random variable

Analogues of the characteristics of a discrete SV ([[10 Numerical Characteristics of Discrete Random Variables]]), but the sum is replaced by an integral.

## Mathematical expectation

If possible values of $X \in [a;b]$:
$$M(X) = \int_a^b x\,f(x)\,dx$$
If the values are on the entire $OX$ axis:
$$M(X) = \int_{-\infty}^{\infty} x\,f(x)\,dx$$

## Variance

$$D(X) = \int_a^b \big[x-M(X)\big]^2 f(x)\,dx = \int_a^b x^2 f(x)\,dx - \big(M(X)\big)^2$$
(similarly from $-\infty$ to $\infty$, if necessary).

## Standard deviation

$$\sigma(X) = \sqrt{D(X)}$$

All properties of $M(X)$ and $D(X)$ discrete SV are saved here.

> [!example] Example - uniform distribution on $[a;b]$
>$$M(X) = \int_a^b x\cdot\frac{1}{b-a}\,dx = \frac{a+b}{2}$$
>$$D(X) = \frac{(b-a)^2}{12}$$

## Related notes
-[[00 Contents]]
- [[12 Probability Density]]
- [[14 Normal and Exponential Distributions]]