---
tags: [tpr, lecture13, cooperative_games, shapley, core]
---

# Lecture 13. Cooperative games

Players can form **coalitions** $K \subset N$ for mutual benefit. The number of possible coalitions: $2^n-1$.

**Characteristic function** $v(K)$ is the largest guaranteed win of the $K$ coalition. Co-op play is entirely driven by the $(N, v)$ pair.

**Division** is the vector $x=(x_1,\ldots,x_n)$ of distribution of winnings $v(N)$ between players.

## Properties of the characteristic function
- Personality: $v(\emptyset)=0$
- Additional: $v(K)+v(N\setminus K)=v(N)$
- Monotony: $A\subseteq B \Rightarrow v(A)\le v(B)$
- **Superadditivity:** $v(K\cup L) \ge v(K)+v(L)$ for non-overlapping $K,L$

The game is **essential** if superadditivity is strict for at least one pair of disjoint coalitions (otherwise it is **insignificant**, and then the division is unique). In an essential game there are infinitely many divisions.

## Conditions for division
- **Individual rationality:** $x_i \ge v(\{i\})$ for all $i$.
- **Collective rationality (efficiency):** $\sum_i x_i = v(N)$.

## C-core
**C-core** is a set of non-dominated divisions that are resistant to deviation of any coalition (no coalition can improve the result of all its members independently). Geometrically, it is a convex polyhedron. In an unimportant game, it consists of one division; in the essential - it can be empty.

## Shapley Vector
**Contribution** of player $i$ to the $K$ coalition: $v(K)-v(K\setminus i)$.

**Shapley vector (value)** is the average contribution of the player across all coalitions:
$$\varphi_i = \sum_{K \ni i} \frac{(k-1)!(n-k)!}{n!}\big(v(K)-v(K\setminus i)\big)$$
where $k=|K|$.

**Shapley's axioms:** linearity (aggregation across games), symmetry (payoff does not depend on player number), efficiency (a blockhead who does not contribute gets 0; $\sum_i \varphi_i = v(N)$).

**Shapley's theorem:** for any cooperative game there is a unique distribution that satisfies all three axioms - this is the Shapley vector. If it belongs to the C-core, the division is both fair and stable (but may not belong to a non-empty C-core).

## Related notes
-[[00 Contents]]
- [[11 Fundamentals of Game Theory]]
- [[12 Matrix and Non-Cooperative Games]]