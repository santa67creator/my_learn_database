---
tags: [terver, lecture7, laplace, poisson]
---

# Lecture 7. Poisson's formula. Local and integral theorems of Laplace

Bernoulli's formula is inconvenient for large $n$ - approximations are used.

## Local Laplace theorem

If $p$ is constant and different from 0 and 1:
$$P_n(m) \approx \frac{1}{\sqrt{npq}}\,\varphi(x), \qquad \varphi(x)=\frac{1}{\sqrt{2\pi}}e^{-x^2/2}, \qquad x=\frac{m-np}{\sqrt{npq}}$$
$\varphi(x)$ - even function: $\varphi(-x)=\varphi(x)$ (values are taken from tables).

> [!example] Example
> $n=400$, $p=0{,}8$, $m=330$. $x = \dfrac{330-320}{\sqrt{64}} = 1{,}25$, $\varphi(1{,}25)=0{,}1826$.
>$$P_{400}(330) = \frac{1}{8}\cdot0{,}1826 \approx 0{,}0228$$

## Poisson's formula

With a large $n$ and a small $p$ (a “rare” event), $\lambda = np$:
$$P_n(m) = \frac{\lambda^m}{m!}\,e^{-\lambda}$$

> [!example] Example
> Out of 1000 parts, 4 are defective ($p=0{,}004$). Find the probability that among the 50 taken there are no defective ones.
>$\lambda = 50\cdot0{,}004=0{,}2$
>$$P_{50}(0) = \frac{(0{,}2)^0}{0!}e^{-0{,}2} \approx 0{,}8187$$

## Laplace's integral theorem

The probability that $A$ will appear between $m_1$ and $m_2$ times:
$$P_n(m_1,m_2) = \Phi(x'') - \Phi(x'), \qquad x'=\frac{m_1-np}{\sqrt{npq}},\;\; x''=\frac{m_2-np}{\sqrt{npq}}$$
where the Laplace function $\displaystyle \Phi(x)=\frac{1}{\sqrt{2\pi}}\int_0^x e^{-z^2/2}dz$ is **odd**: $\Phi(-x)=-\Phi(x)$.

> [!example] Example
> $n=100$, $p=0{,}8$, find $P(72\le m\le84)$.
>$x'=\dfrac{72-80}{4}=-2,\quad x''=\dfrac{84-80}{4}=1$
>$$P_{100}(72,84)=\Phi(1)-\Phi(-2)=\Phi(1)+\Phi(2)=0{,}3413+0{,}4772=0{,}8185$$

## Related notes
- [[00 Contents]]
- [[06 Bernoulli Formula]]
- [[14 Normal and Exponential Distributions]] - $\varphi(x)$ and $\Phi(x)$ the same functions as for normal distribution