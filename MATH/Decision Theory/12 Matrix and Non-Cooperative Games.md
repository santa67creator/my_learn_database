---
tags: [tpr, lecture 12, matrix_games, saddle_point]
---

# Lecture 12. Antagonistic, matrix and non-cooperative games

## Antagonistic (matrix) games
Two-person zero-sum game: player 1 maximizes $g(u_1,u_2)$, player 2 minimizes.

**Low price of the game:** $\underline v = \sup_{u_1}\inf_{u_2} g$. **Top price:** $\overline v = \inf_{u_2}\sup_{u_1} g$. Always $\underline v \le \overline v$. If $\underline v = \overline v$ is **the price of the game**.

For the matrix game $A=(a_{ij})_{n\times m}$: $\underline v = \max_i\min_j a_{ij}$, $\overline v=\min_j\max_i a_{ij}$. Equality is achieved if and only if there is a **saddle point** $(i_0,j_0)$: $a_{ij_0}\le a_{i_0j_0}\le a_{i_0j}\ \forall i,j$.

## Mixed strategies
$p=(p_1,\ldots,p_n)$ - mixed strategy of player 1 ($\sum p_i=1$), $q$ - player 2. Winning: $h(p,q)=\sum_i\sum_j a_{ij}p_iq_j = pAq$.

**Main theorem of matrix games (von Neumann):** any matrix game has a price in mixed strategies:
$$v = \max_p\min_q h(p,q) = \min_q\max_p h(p,q) = h(p^0,q^0)$$

**Dominance principle:** a row (column) dominated by a linear combination of the others can be crossed out - it reduces the dimension of the problem before solving it.

> [!example] Saddle point
> $A=\begin{pmatrix}1&2\\0&1\end{pmatrix}$ - saddle point (1,1), game price = 1.

## Non-cooperative games $N$ persons
**Nash equilibrium situation:** $g_i(u^0)\ge g_i(u_1^0,\ldots,u_i,\ldots,u_N^0)\ \forall u_i\in U_i,\ \forall i$. For differentiable $g_i$ at the interior point: $\partial g_i/\partial u_i = 0$.

**Bimatrix game** $\Gamma(A,B)$: equilibrium is found by marking the maximum of the 1st coordinate in each column, and the maximum of the 2nd in each row; coincidence of both marks = equilibrium point.

> [!example] Different gains in equilibrium
> $\begin{pmatrix}1;0 & -1;-1\\0;0 & 0;1\end{pmatrix}$ - two equilibrium points (1,1) and (2,2) with payoffs (1,0) and (0,1): players may not hit either of them, aiming at different ones.

For completely mixed equilibrium situations in a bimatrix game with non-degenerate square $A,B$: $p=v_2uB^{-1}$, $q=v_1A^{-1}u$, where $u=(1,\ldots,1)$, $v_1=1/(uA^{-1}u^T)$, $v_2=1/(uB^{-1}u^T)$.

## Related notes
- [[00 Contents]]
- [[11 Fundamentals of Game Theory]]
- [[10 Decision-Making Under Uncertainty]] - the same payment matrix, but without a reasonable opponent