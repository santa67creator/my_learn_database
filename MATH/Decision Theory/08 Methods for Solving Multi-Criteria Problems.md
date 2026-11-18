---
tags: [tpr, lecture8, saati]
---

# Lecture 8. Methods for solving multicriteria problems

## Criteria collapse
General view: $f_0 = \varphi(f_1,\ldots,f_m)$.
- **Summation with scales** (economic method): $f_0 = \sum_i a_i f_i$, $\sum a_i=1$.
- **Logical methods** (for qualitative criteria 0/1): negation, conjunction $f_0=\prod f_i$, disjunction $f_0 = 1-\prod(1-f_i)$.
- **By worst/best value:** $f_0 = \min_i a_if_i$ or $f_0=\max_i a_if_i$.

**Carlin/Germeier theorem:** for concave criteria on a convex set, any effective (Pareto-optimal) point is obtained as the maximum of the weighted sum of criteria with some weights $a_i$.

## Methods for solving vector optimization problems
- **Method of successive concessions** - criteria are ordered by importance; maximize the first, then the second with an acceptable deviation from the maximum of the first, etc.
- **Ideal point method** - look for the point on the Pareto frontier that is closest to the “utopia point” (desired/best values ​​of all criteria).
- **Suboptimization (constraint method)** - one criterion is maximized, the rest are converted into restrictions: $f_1(x)\to\max,\ f_i(x)\ge l_i,\ i=2,\ldots,m$.
- **Lexicographic optimization (priority method)** - maximize $f_1$, then $f_2$ on the set of solutions that maximize $f_1$, etc.
- **Target programming** - minimizing the distance $\rho(f(x), Y^*)$ to the target set $Y^*$ in the criteria space.

## Hierarchy analysis method (MAI, Saaty method)
Decomposition of the problem into levels (hierarchy) + pairwise comparisons of elements by experts.

**Pairwise comparison matrix** $A=(a_{ij})$: $a_{ji}=1/a_{ij}$ (backward symmetric); **agreed** if $a_{ik}=a_{ij}\cdot a_{jk}$.

**Saaty's theorem:** a positive inversely symmetric matrix is ​​consistent $\Leftrightarrow \lambda_{max}=n$ (the maximum eigenvalue is equal to the dimension of the matrix).

**Priority vector** $\omega$ is an eigenvector: $A\omega = \lambda_{max}\omega$, normalized so that $\sum \omega_i = 1$.

> [!example] Matched 3x3 matrix
> The criterion $f_1$ is 3/2 times more important than $f_2$ and 3 times more important than $f_3$; $f_2$ is 2 times more important than $f_3$. Solving $(A-3E)\omega=0$, we get $\omega = (1/2,\ 1/3,\ 1/6)$.

For an inconsistent matrix, the approximate methods are: (1) row sum normalization, (2) column reciprocal sum normalization, (3) averaging over normalized columns, (4) geometric average of row elements (the most accurate).

**Consistency Index (CI)** $=\dfrac{\lambda_{max}-n}{n-1}$; **consistency ratio (CR)** $=$ IS / (average random index for a matrix of the same order). OS $\le 0{,}10$ - acceptable.

## Related notes
-[[00 Contents]]
- [[07 Multi-Criteria Choice]]