---
tags: [terver, lecture14, normal_distribution]
---

# Lecture 14. Normal distribution. Exponential distribution

## Normal distribution

Density:
$$f(x) = \frac{1}{\sigma\sqrt{2\pi}}\, e^{-\frac{(x-a)^2}{2\sigma^2}}$$
Determined by two parameters: $a$ and $\sigma$, while
$$a = M(X), \qquad \sigma = \sigma(X)\;\text{(standard deviation)}$$
(proved by substitution $z=(x-a)/\sigma$ and Poisson integral $\int e^{-z^2/2}dz=\sqrt{2\pi}$).

Changing $a$ shifts the curve along the $OX$ axis; an increase in $\sigma$ makes the curve flatter (stretched along $OX$), a decrease makes it more “pointy.”

### Probability of falling into the interval

$$P(\alpha<X<\beta) = \Phi\!\left(\frac{\beta-a}{\sigma}\right) - \Phi\!\left(\frac{\alpha-a}{\sigma}\right)$$
where $\Phi(x)$ is the Laplace function (see [[07 Poisson Formula and Laplace Theorems]]).

For symmetrical deflection $|X-a|<\delta$:
$$P(|X-a|<\delta) = 2\Phi\!\left(\frac{\delta}{\sigma}\right)$$

> [!example] Example 1
> $a=10,\ \sigma=4,\ \alpha=2,\ \beta=13$:
>$$P(2<X<13)=\Phi(0{,}75)+\Phi(2) = 0{,}2734+0{,}4772=0{,}7506$$

> [!example] Example 2 - part diameter
> $M(X)=50$mm, $\sigma=5$mm. Find the probability of deviation by no more than 3 mm.
>$$P(|X-50|<3)=2\Phi(0{,}6)=2\cdot0{,}2257=0{,}4514$$

### Three sigma rule

$$P(|X-a|<3\sigma) = 2\Phi(3) = 0{,}9973$$
A deviation of more than $3\sigma$ is an almost impossible event (probability 0.0027).

## Exponential distribution

$$f(x)=\begin{cases}0,& x<0\\ \lambda e^{-\lambda x},& x\ge0\end{cases}\qquad(\lambda={\rm const}>0)$$
$$F(x)=\begin{cases}0,& x<0\\ 1-e^{-\lambda x},& x\ge0\end{cases}$$
$$P(a<X<b) = e^{-\lambda a} - e^{-\lambda b}$$

Numerical characteristics:
$$M(X)=\sigma(X)=\frac{1}{\lambda}, \qquad D(X)=\frac{1}{\lambda^2}$$

## Related notes
-[[00 Contents]]
-[[13 Numerical Characteristics of Continuous Random Variables]]
- [[07 Poisson Formula and Laplace Theorems]] - functions $\varphi(x)$ and $\Phi(x)$
-[[15 Sample Statistical Distribution]]