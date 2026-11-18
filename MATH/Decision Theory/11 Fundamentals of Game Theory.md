---
tags: [tpr, lecture11, game_theory, nash]
---

# Lecture 11. Static decision-making problems under conflict conditions

**Conflict** is a clash of interests of several parties. **Game** is a mathematical model of conflict. **Game theory** is a theory of decision making in conflict conditions.

## Classification of games
- **Coalition of action** (jointly acting subjects) vs **coalition of interests** (equally interested) - may not coincide. If they match → **player**.
- **Antagonistic** games 2 persons (opposite goals) vs games $N$ persons.
- **Non-coalition** (coalitions are prohibited) vs **coalition** (including **cooperative** - one common coalition).
- **Finite** games (finite number of strategies); with $N=2$: **bimatrix** game (2 payoff matrices), **matrix** = final antagonistic.
- **Positional** games (consecutive moves, e.g. chess) vs games in **normal form** (one-act, simultaneous choice).
- **Pure strategy** — element of the original set; **mixed strategy** - probability distribution on pure strategies.

The game in normal form: $\Gamma = \langle I, \{U_i\}, \{g_i\}\rangle$, where $g_i$ is the payoff function of player $i$ (maximized).

## Principles of optimality
**Nash Equilibrium** $u^0$: it is not beneficial for anyone to deviate alone -
$$g_i(u^0) = \max_{u_i\in U_i} g_i(u_1^0,\ldots,u_i,\ldots,u_N^0)\quad \forall i$$
Disadvantages: may not exist; may not be unique without a selection criterion; There may be non-equilibrium situations that are more beneficial for all players (see “prisoner’s dilemma”).

**Pareto Optimality** $u^0$: There is no $u$ with $g_i(u)>g_i(u^0)$ for all $i$ and strict inequality for at least one.

**Dominance of strategies:** strategy $u_i$ dominates $v_i$ if it gives no less winnings for any actions of the others. The sequential elimination of dominated strategies leading to a single outcome is called a **complex equilibrium** - the game is **dominance soluble**.

**The principle of guaranteed results (maximin)** - careful behavior when isolated: $g_i^\Gamma(u_i)=\inf_{u_{-i}} g_i(u_i,u_{-i})$; a guarantee strategy maximizes this guaranteed outcome.

> [!example] Prisoner's dilemma
> $A=\begin{pmatrix}5&0\\10&1\end{pmatrix}$, $B=\begin{pmatrix}5&10\\0&1\end{pmatrix}$. The only Nash equilibrium is (2,2) with payoff (1,1), although (1,1) gives both (5,5) - but this is unstable.

> [!example] Family dispute
> Two equilibrium situations (1,1) and (2,2) with payoffs (2,1) and (1,2) - players benefit from different equilibria, an agreement is needed.

## Related notes
- [[00 Contents]]
- [[07 Multi-Criteria Choice]] - Pareto optimality
- [[12 Matrix and Non-Cooperative Games]]
-[[13 Cooperative Games]]