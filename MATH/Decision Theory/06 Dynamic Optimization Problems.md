---
tags: [tpr, lecture6, dynamic_programming]
---

# Lecture 6. Dynamic optimization problems

**Dynamic programming (DP)** is a method of solving complex problems by breaking them down into simpler overlapping subtasks with **optimal substructure** (the optimal solution to the subtask is used to solve the original problem). Each subtask is solved only once, the result is remembered (memoization).

- **Downward DP** - breaking down the task from top to bottom + memorization.
- **Ascending DP** - all necessary subtasks are calculated in advance, from bottom to top.

Classic DP problems: greatest common subsequence, Levenshtein distance, Fibonacci numbers, order of matrix multiplication, knapsack problem, **Floyd-Warshall** and **Bellman-Ford** algorithms (shortest paths in a graph).

## Bellman function
$N$-step process with states $x^{(0)} \to \ldots \to x^{(N)}$, transitions $x^{(k)} = f^{(k)}(x^{(k-1)}, u^{(k)})$, additive objective function
$$J(\bar x, \bar u) = \sum_{k=1}^N J_k(x^{(k-1)}, u^{(k)}) + J_{N+1}(x^{(N)}) \to extr$$

**Optimality principle:** whatever decisions are made at the initial steps, subsequent decisions must be optimal relative to the resulting new initial state.

**Bellman function** $B_k(x^{(k-1)})$ is the optimal value of the objective function of the remaining $N-k+1$ steps. Bellman equations:
$$B_N(x^{(N-1)}) = \underset{u^{(N)}}{extr}\left[J_{N+1}(f^{(N)}(x^{(N-1)},u^{(N)})) + J_N(x^{(N-1)},u^{(N)})\right]$$
$$B_k(x^{(k-1)}) = \underset{u^{(k)}}{extr}\left[B_{k+1}(f^{(k)}(x^{(k-1)},u^{(k)})) + J_k(x^{(k-1)},u^{(k)})\right],\quad k=1,\ldots,N-1$$

**DP Algorithm:**
1. **Conditional optimization (backward sweep)** - from step $N$ to step $1$ we find conditionally optimal controls $u^{(k)*}(x^{(k-1)})$ and Bellman functions.
2. **Unconditional optimization (direct sweep)** - from the optimal initial state we successively find $u^{(1)*}, x^{(1)*}, u^{(2)*}, x^{(2)*}, \ldots$

## Network planning
**Critical path method (CPM)** and **PERT** - management of a set of works through a graph (network): vertices = events, arcs = works (with duration/cost). **Critical path** is a sequence of work, the shift of which increases the total time of the project. Solved by the DP method: sequential calculation of the earliest dates for the occurrence of events.

## Related notes
-[[00 Contents]]
- [[05 Static Optimization Problems]]
- [[14 Dynamic Games]] - similar idea of reverse induction