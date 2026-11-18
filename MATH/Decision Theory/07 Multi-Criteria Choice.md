---
tags: [tpr, lecture7, Pareto]
---

# Lecture 7. Decision making under conditions of multicriteria choice

When there are several conflicting criteria, there is usually no absolutely best solution - the choice is always a **compromise**. Vector criterion $f=(f_1,\ldots,f_m)$ on the set of solutions $X$; $Y=f(X)$ is the space of estimates.

## Preference relationships
- **Strict preference** $x' \succ x''$, **indifference** $x'\sim x''$, **non-strict preference** $x' \succeq x''$.
- **Binary relation** $\mathfrak{R} \subset A\times A$ can be: reflexive, irreflexive, symmetrical, asymmetrical, antisymmetrical, transitive, complete/partial.
- **Order** – reflexive + antisymmetric + transitive; **strict order** - irreflexive + transitive.
- The preference relation of a decision maker behaving “reasonably” is **strict order** (irreflexive and transitive).

**Utility (value) function** $u(x)$ is monotonic: $u(x')>u(x'') \Leftrightarrow x' \succ x''$. Defined up to increasing transformation.

## Domination
$x'$ **dominates** $x''$ if $x' \succ x''$. **Many non-dominated solutions** $N_{dom}X$. Axiom for eliminating dominated solutions: $Sel\,X \subset N_{dom}X$.

## Pareto optimality
$x^o$ **Pareto optimal** if there is no $x\in X$ with $f(x) \ge f(x^o)$ (componentwise, at least one inequality is strict) - i.e. You cannot improve one component without worsening the other.

**Edgeworth-Pareto principle:** if the decision maker behaves “reasonably” (axioms of irreflexivity, transitivity, continuation of preference and consistency of criteria), the chosen solutions are necessarily Pareto-optimal:
$$Sel\,X \subset N_{dom}X \subset P_f(X) \subset X$$

The Pareto set can be empty, consist of one element, be infinite, or coincide with the entire $X$.

## Related notes
-[[00 Contents]]
-[[08 Methods for Solving Multi-Criteria Problems]]
- [[11 Fundamentals of Game Theory]] - the same idea of Pareto optimality applies to game outcomes