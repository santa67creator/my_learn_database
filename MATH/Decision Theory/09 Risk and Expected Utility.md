---
tags: [tpr, lecture9, risk, usefulness]
---

# Lecture 9. Decision making under conditions of incomplete information (risk)

**Risk** is the unpredictability of the system state as a result of incomplete information. **Risk management** - making decisions taking into account and assessing risk factors.

## Statistical characteristics
$$M(Y)=\sum_k p_k y_k,\qquad D(Y) = M\big[(Y-M(Y))^2\big]=M(Y^2)-M(Y)^2$$
**Unbiased** sample variance estimator: $D(Y)=\dfrac{1}{N-1}\sum_k(y_k-M(Y))^2$ (biased estimator with denominator $N$ underestimates variance by $\frac{N-1}{N}$ times).

**Correlation moment (covariance):** $\sigma_{Y_1Y_2}=M\big[(Y_1-M(Y_1))(Y_2-M(Y_2))\big]$. **Correlation coefficient:** $\rho_{Y_1Y_2}=\sigma_{Y_1Y_2}/(\sigma_{Y_1}\sigma_{Y_2}) \in [-1,1]$.

## Risk functions
- $l_1$-metric (average deviation): $R(x)=M|r(x)-d(x)|$
- $l_2^2$-metric (variance): $R(x)=M(r(x)-d(x))^2$
- $l_2$-metric (RMS): $R(x)=\sqrt{M(r(x)-d(x))^2}$

**Value at Risk (VaR):** $VaR_\alpha(Y)=\max\{\vartheta \mid P(Y\ge \vartheta)\ge\alpha\}$ - return that the portfolio will not exceed (will not fall below) with probability $\alpha$.

## Expected utility theory
**Lottery** $l=(X,p)$ - outcomes $x_1,\ldots,x_n$ with probabilities $p_1,\ldots,p_n$.
**Utility function** $u(x)$: $l_1 \succ l_2 \equiv M_{l_1}u > M_{l_2}u$, where $M_l u = \sum_i u(x_i)p_i$ is **expected utility**.

> [!example] Comparison of two lotteries
> $l_1$: win 200 (p=0.9) / lose 800 (p=0.1). $l_2$: win 1000 (p=0.1) / 0 (p=0.9). With $u(x)=\ln(x+1000)$: $\tilde u(l_1)=6{,}911$, $\tilde u(l_2)=6{,}977$ → the second lottery is preferable, although $M_{l_1}x=M_{l_2}x=100$.

**Reliable equivalent (DDE)** of the $l$ lottery - the amount of $x$, equivalent to participation in $l$: $u(x)=\tilde u(l)$.

Attitude to risk (comparison of DDE with mathematical expectation $M_lx$):
- DDE $< M_lx$ → Decision maker **not inclined** to risk (cautious), $u(x)$ is concave;
- DDE $> M_lx$ → decision maker **prone** to risk, $u(x)$ convex;
- DDE $= M_lx$ → **indifferent** to risk, $u(x)$ is linear.

**Risk aversion function (Arrow-Pratt):** $r(x) = -u''(x)/u'(x)$. $r>0$ - not inclined, $r<0$ - inclined, $r\equiv0$ - neutral.

**Neumann-Morgenstern Theorem:** if a preference relation on a set of lotteries satisfies the axioms of continuity and independence, there is a utility function $u(x)$ representing it as expected utility (defined up to a positive linear transformation $u'=ku+b$, $k>0$).

## Related notes
-[[00 Contents]]
- [[04 Mathematical Tools for Decision-Making]]
-[[10 Decision-Making Under Uncertainty]]
- [[15 Statistical Games]] - Bayes formula for reestimating probabilities