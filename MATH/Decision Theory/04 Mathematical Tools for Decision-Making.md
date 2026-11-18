---
tags: [tpr, lecture4]
---

# Lecture 4. Mathematical tools for decision making

## Basic formalization
- **Active means (resource)** - what the decision maker has at his disposal.
- **Strategy (decision)** $x$ - the method of using resources, controlled by the decision-maker.
- **Uncontrollable factor** $y$ - beyond the power of the decision maker; can be **fixed** (known exactly), **random** (distribution law is known) or **uncertain** (only the range of values ​​is known).
- **Efficiency criterion** $W = F(x, y)$ (synonyms: utility function, payoff function, objective function) - usually maximized.
- Static (normal) form of the model: object $\{W, x, y\}$, $x \in X$, $y \in Y$.

## Strategy effectiveness assessments
- If the factor is fixed ($y=y^0$): $f_0(x) = F(x, y^0)$, the optimal value is $x^0$: $f_0(x^0) \ge f_0(x)\ \forall x \in X$.
- If the factor is random with probabilities $p_1,\ldots,p_n$: **average estimate**
  $$f_0(x) = \sum_{i=1}^n p_i F(x, y_i)$$
- If the factor is undefined (only the area $Y$ is known): **guaranteed score**
  $$f_г(x) = \min_{y \in Y} F(x, y)$$
  Maximum guaranteed result: $F_г(x) = \max_{x\in X}\min_{y\in Y} F(x,y)$ is **maximin** (or **minimax** when permuting operations).

## Classification of TPR tasks
By type of uncontrollable factors and type of criterion/strategy space:
- **Without uncontrollable factors (or only fixed ones)** → **mathematical programming**: linear, integer, nonlinear (including convex), dynamic.
- **Several criteria** → problem of **multi-criteria (vector) optimization**.
- **Uncertain factors** → **maximin (minimax) problems**; if the uncertainty is associated with the actions of an intelligent opponent → **game theory**.
- **Random/uncertain factors, incomplete information** → decision-making under conditions of **risk**.

## Related notes
- [[00 Contents]]
- [[03 Mathematical Model of a Problem Situation]]
- [[05 Static Optimization Problems]]
- [[09 Risk and Expected Utility]]
-[[10 Decision-Making Under Uncertainty]]