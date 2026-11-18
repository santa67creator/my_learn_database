---
tags: [tpr, lecture15, statistical_games, Wald, Bayes]
---

# Lecture 15. Statistical games

The creator of the theory is **A. Wald**. A game of two “persons” - statistics and nature, but nature is not an intelligent opponent (does not strive to win) - unlike an antagonistic game.

## Basic notation
$\Omega$ — states of nature $\theta$; $A$ - solutions statistics $a$; $L(\theta,a)$ - loss function; $D$ - pure functions of the $d(x)$ solution; $x$ — result of the experiment (random vector); $F(x|\theta)$ - conditional distribution.

**Risk function:** $R(\theta,d)=ML(\theta,a)=\int_x L(\theta,a)\,dF(x|\theta)$, where $a=d(x)$.

The statistical game $G=(\Omega, D, R)$ is a 2-person zero-sum game, where the risk $R$ is a payment to nature.

## Randomization and game expansions
- **Randomization on the statistics side:** distribution of $\delta$ on the set $D$ → **extended game** $(\Omega, D^*, R)$.
- **Randomization on the side of nature:** prior distribution $\xi$ to $\Omega$ → **Bayesian risk**
  $$r(\xi,\delta) = \int_\Omega R(\theta,\delta)\,d\xi(\theta)$$
- Both randomizations together → **fully expanded statistical game** $(\Xi, D^*, r)$.

**Acceptable solution function** $\delta$ - there is no other $\delta_0$ that is not worse for all $\theta$ and strictly better for at least one.

**Bayesian decision function** - minimizes the Bayesian risk $r(\xi,\delta)$ with a given prior $\xi$; Bayesian functions are always valid.

## Bayes formula (reminder)
$$P(B_j|A) = \frac{P(B_j)P(A|B_j)}{\sum_{k=1}^n P(B_k)P(A|B_k)}$$

> [!example] Revaluation of the share of enterprises
> Factories produce 60%/30%/10% of batch products, the share of serviceable ones is 0.98/0.99/0.96. Full probability of serviceability: $P(A)=0{,}6{\cdot}0{,}98+0{,}3{\cdot}0{,}99+0{,}1{\cdot}0{,}96=0{,}981$. Posterior shares: $P(B_1|A)\approx0{,}599$, $P(B_2|A)\approx0{,}303$, $P(B_3|A)\approx0{,}098$.

## Non-standard principles (comparison with Lecture 10)
- **Bayes-Laplace principle** - states of nature are equally probable (Bayes, 1763), take the average over all states.
- **Hurwitz principle** (here is a simplified version): the arithmetic mean of the best and worst results (for unknown probabilities).

> [!example] Enterprise type selection (4 states of nature, 4 types)
> According to Wald (maximin) - enterprise A3. According to Hurwitz (average of worst/best) - A2. According to Bayes - Laplace (equal probabilities 1/4) - also A3 ($M_3=7{,}5$ - maximum of average values). Different criteria again diverge - the choice depends on how much information is actually available and whether the decision is repeated many times (the law of large numbers justifies averaging only when repeated many times).

## Comparison with a strategy game
| 2 person zero sum game | Statistics game |
|---|---|
| $X, Y$ - strategies of players 1, 2 | $\Omega, D$ - states of nature, solution functions |
| $W(x,y)$ - payment | $R(\theta,d)$ - risk statistics |
| Maximum/minimax strategy | Minimax function solution $\delta^0$ |

## Related notes
- [[00 Contents]]
- [[10 Decision-Making Under Uncertainty]] - Wald, Hurwitz, Laplace criteria in their “pure” form
- [[09 Risk and Expected Utility]] - Bayes' formula has already been found there


# NEXT CHAPTER --> [[PRACTICE-1]]