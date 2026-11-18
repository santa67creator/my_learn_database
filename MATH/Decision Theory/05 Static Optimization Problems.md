---
tags: [tpr, lecture 5, optimization]
---

# Lecture 5. Decision making under conditions of complete information. Static optimization problems

## Basic concepts
Optimization task: $f(x) \to \max,\ x \in X$. $x^o$ is the **global maximum** point, if $f(x^o) \ge f(x)\ \forall x \in X$. **Local maximum** - the same in a certain neighborhood. Problem for the **unconditional** extremum: $X = \mathbb{R}^n$; on **conditional** - otherwise.

**Weierstrass's theorem.** If $X$ is closed and bounded, $f$ is continuous on $X$, then a global maximum (minimum) exists.

**Fermat's principle (necessary condition of the 1st order).** If $x^0$ is the local extremum of the differentiable $f$, then $f'(x^0) = 0$ (the gradient is zero) is called a stationary point.

**Hessian Matrix** $f''(x) = \left(\dfrac{\partial^2 f}{\partial x_i \partial x_j}\right)$. A necessary 2nd order condition for a maximum: $f''(x^0)$ is non-positive definite. Sufficient condition: $f'(x^0)=0$ and $f''(x^0)$ are negative definite.

## Nonlinear programming
General task: $f(x) \to \max,\ g_i(x) \ge 0,\ i=1,\ldots,m,\ x \in P$.

**Lagrange function:** $L(x,y) = f(x) + \sum_{i=1}^m y_i g_i(x)$ - The Lagrange multiplier method reduces conditional maximization to unconstrained optimization $L$.

## Linear programming (LP)
Standard form: $cx \to \max,\ Ax \le b,\ x \ge 0$.

> [!example] Production planning task
> Resources $R_1,R_2,R_3$, goods $T_1,T_2$ with prices $c_1,c_2$, consumption rates $a_{ij}$ and stocks $b_i$. Model:
>$$c_1x_1+c_2x_2 \to \max,\quad a_{i1}x_1+a_{i2}x_2 \le b_i\ (i=1,2,3),\quad x_1,x_2\ge0$$

Terminology: strategy $x$ = **plan**; a valid plan satisfies the constraints; vertex of feasible set = **reference plan**.

**Theorem.** If the LP problem has a solution, there is a vertex of the admissible set (reference plan), which is the optimal plan → hence the **simplex method** (enumeration of vertices with a strictly improving value of the objective function).

**Transport problem:** minimize $\sum_i\sum_j c_{ij}x_{ij}$ under production/consumption balance conditions; solved by the **potential method** (a special case of the simplex method).

## Discrete (integer) programming
Variables accept only integer/discrete (often Boolean $\{0,1\}$) values.

> [!example] Assignment problem
> $n$ employees and $n$ works, income $c_{ij}$. $x_{ij}\in\{0,1\}$, $\sum_j x_{ij}=1\ \forall i$, $\sum_i x_{ij}=1\ \forall j$, maximize $\sum\sum c_{ij}x_{ij}$.

> [!example] Traveling Salesman Problem
> The shortest route through $n$ cities with a return to the starting point. Requires additional $u_i$ variables to eliminate disconnected subroutes.

Solution methods: **cutting method** (Gomori algorithms - sequentially solve the LP problem without integer and cut off non-integer solutions) and **branch and bound method** (Land-Doig algorithm: partitioning an admissible set, discarding obviously unpromising subsets).

## Related notes
- [[00 Contents]]
- [[04 Mathematical Tools for Decision-Making]]
- [[06 Dynamic Optimization Problems]]