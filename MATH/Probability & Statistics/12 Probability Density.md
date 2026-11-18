---
tags: [terver, lecture12]
---

# Lecture 12. Probability distribution density

**Distribution density** $f(x)$ is the first derivative of the distribution function:
$$f(x) = F'(x)$$

$$P(a<X<b) = \int_a^b f(x)\,dx \qquad F(x) = \int_{-\infty}^{x} f(t)\,dt$$

**Properties:**
1.$f(x) \ge 0$
2.$\displaystyle\int_{-\infty}^{\infty} f(x)\,dx = 1$

**Probabilistic meaning:** $f(x) \approx \dfrac{P(x<X<x+\Delta x)}{\Delta x}$ - probability density at a point.

> [!example] Example
>$$f(x)=\begin{cases}0,& x\le0\\ 2x,& 0<x\le1\\ 0,& x>1\end{cases}$$
>$$P(0{,}5<X<1)=2\int_{0.5}^{1} x\,dx = x^2\Big|_{0.5}^{1} = 1-0{,}25=0{,}75$$

## Law of uniform distribution

The density is constant over the interval $(a;b)$:
$$f(x)=\begin{cases}0,& x\le a\\ \dfrac{1}{b-a},& a<x\le b\\ 0,& x>b\end{cases} \qquad\qquad F(x)=\begin{cases}0,& x\le a\\ \dfrac{x-a}{b-a},& a<x\le b\\ 1,& x>b\end{cases}$$

For $R$, uniform on $(0;1)$: $P(c<R<d) = d-c$.

## Related notes
- [[00 Contents]]
-[[11 Law of Large Numbers and Chebyshev]]
- [[13 Numerical Characteristics of Continuous Random Variables]]
- [[14 Normal and Exponential Distributions]]