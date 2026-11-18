---
tags: [terver, lecture10]
---

# Lecture 10. Numerical characteristics of discrete random variables

## Mathematical expectation

$$M(X) = x_1p_1 + x_2p_2 + \ldots + x_np_n$$

Meaning: approximately equal to the arithmetic mean of the observed values; “distribution center” ($M(X)$ lies between the smallest and largest possible values).

**Properties:**
1. $M(C) = C$ (mathematical expectation of a constant is equal to itself)
2. $M(CX) = C\,M(X)$
3. For independent $X,Y$: $M(XY) = M(X)\,M(Y)$
4. $M(X+Y) = M(X)+M(Y)$ (for any $X,Y$)
5. For the number of occurrences of an event in $n$ trials: $M(X) = np$

> [!example] Example
> | $X$ | 2 | 4 | 7 |
> |---|---|---|---|
> | $p$ | 0.1 | 0.5 | 0.4 |
>
>$$M(X) = 2\cdot0{,}1+4\cdot0{,}5+7\cdot0{,}4 = 5$$

## Deviation and variance

**Deviation**: $X - M(X)$, and $M(X-M(X))=0$.

**Dispersion** — mat. expectation of squared deviation:
$$D(X) = M\big[(X-M(X))^2\big] = M(X^2) - M^2(X)$$

**Dispersion properties:**
1. $D(C) = 0$
2.$D(CX) = C^2 D(X)$
3. For independents: $D(X+Y) = D(X)+D(Y)$
4. For independents: $D(X-Y) = D(X)+D(Y)$
5. For the number of occurrences of an event in $n$ trials: $D(X) = npq$

## Standard deviation
$$\sigma(X) = \sqrt{D(X)}$$

> [!example] Example - M(XY) for independent variables
> $X$: values 1,3,5 with $p$: 0.6/0.1/0.3. $Y$: values ​​2.8 with $p$: 0.4/0.6.
>$$M(X)=0{,}6+0{,}3+1{,}5=2{,}4,\quad M(Y)=0{,}8+4{,}8=5{,}6$$
>$$M(XY)=M(X)M(Y)=2{,}4\cdot5{,}6=13{,}44$$

## Related notes
- [[00 Contents]]
- [[09 Binomial and Geometric Distribution]]
- [[11 Law of Large Numbers and Chebyshev]] - variance is used in Chebyshev’s inequality
- [[13 Numerical Characteristics of Continuous Random Variables]] - similar definitions through the integral