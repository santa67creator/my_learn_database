---
tags: [tpr, lecture 14, positional_games]
---

# Lecture 14. Dynamic problems of decision-making in conditions of conflict

Real conflicts are often multi-step - players take turns taking into account previous development. A convenient representation is a **positional game**: a finite directed graph-tree, vertices = positions (choice situations or “nature” case), leaves = outcomes with final payoffs.

## Games with complete information
**Multi-stage positional game** is given by: the tree $G$ with the initial position $x_0$; dividing positions into sets of order of players $X_1,\ldots,X_N$ and final positions $X_{N+1}$; function of winnings $H(x)$ on the final positions.

**Full information** - when making a move, the player knows the current position (and therefore the entire background).

**Strategy of behavior** of the player $i$ is a display that associates each of his positions with the next position. The game (the path from $x_0$ to the sheet) is uniquely determined by the set of strategies of all players → reduces the game to normal form.

**Theorem:** Any finite game with complete information has a Nash equilibrium situation.

## Absolute (perfect) balance
The situation $u^0$ is a **perfect equilibrium** if its restriction to any subgame (with any initial vertex $z$) is also a Nash equilibrium in this subgame.

**Kuhn's theorem:** in any finite multi-stage game with complete information there is a situation of absolute Nash equilibrium.

**Backward induction method** - finds a perfect equilibrium: starting from the vertices preceding the final ones, each vertex is assigned a payoff vector of the optimal subgame, then a step back to the beginning of the tree.

> [!example] Issuing a loan
> Bank: issue/refuse. Borrower: return/default. In case of default, the bank loses 100, the borrower receives 110. Perfect equilibrium - (failure), because Knowing that the borrower will choose to default if issued, the bank prefers not to issue a loan at all, although (issuing, returning) would be more profitable for both (Pareto is better, but unsustainable).

## Games with incomplete information
**Information set** of a player is positions that are indistinguishable to him at the moment of his move (he does not know which one he is in). The game may not have equilibrium in pure strategies.

> [!example] Product quality control
> Without the supplier's guarantee, the Nash equilibrium gives both of them a smaller gain than they could get; the introduction of a fine (guarantee) for poor quality changes the equilibrium to a more beneficial one for both players - it is profitable to introduce guarantees.

## Related notes
- [[00 Contents]]
- [[11 Fundamentals of Game Theory]]
- [[06 Dynamic Optimization Problems]] - same backward sweep/induction principle as Bellman