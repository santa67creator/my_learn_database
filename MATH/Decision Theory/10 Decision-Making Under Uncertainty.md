---
tags: [tpr, lecture10, Wald, Savage, Hurwitz, Laplace]
---

# Lecture 10. Decision making under conditions of uncertainty (“playing with nature”)

The decision maker has $n$ strategies, “nature” has $m$ states; **payoff matrix** $A=(a_{ij})_{n\times m}$ — winnings with the $i$ strategy and the $j$ state.

## Criteria for choosing a strategy
**Savage Risk Matrix:** $r_{ij}=\max_k a_{kj} - a_{ij} \ge 0$ (how much worse than the best choice given the same state of nature).

| Criterion | Formula | Logic |
|---|---|---|
| **Valda** | $W=\max_i \min_j a_{ij}$ | nature is hostile - maximize the worst case (pessimist) |
| **Maximax** | $M=\max_i \max_j a_{ij}$ | nature is favorable (pure optimist) |
| **Gurvitsa** | $H=\max_i\big[\alpha\min_j a_{ij}+(1-\alpha)\max_j a_{ij}\big]$ | weighs pessimism ($\alpha$) and optimism |
| **Laplace** | $L=\max_i \frac1m\sum_j a_{ij}$ | all states of nature are equally probable |
| **Savage** | $S=\min_i \max_j r_{ij}$ | minimize maximum risk (regret) |

> [!example] Calculation example (payment matrix $A$ 3×3)
>$A=\begin{pmatrix}2&3&3\\2&4&1\\0{,}1&1&8\end{pmatrix}$. According to Wald: $W=2$ (strategy 1). According to Savage: $S=3$ (strategy 3). Different criteria give different recommendations - none are universal.

## Is it worth doing the experiment?
If the prior probabilities of $q_1,\ldots,q_m$ states are known, and the experiment (cost $C$) accurately reveals the state of nature: the experiment is profitable if
$$C < \min_i \sum_j r_{ij} q_j = \min_i r_i^*$$
(average expected risk).

## Properties of criteria (axioms)
Axioms: ordering, symmetry, strict dominance, continuity, linear transformation, appended rows, shift column, repeat column, convexity, append special row.

The Wald criterion satisfies everything except the column shift; Laplace - everything except column repetition; Savage - to all except the added lines; Hurwitz - everything except column shift and convexity. These sets of axioms uniquely define each criterion.

## Related notes
-[[00 Contents]]
-[[09 Risk and Expected Utility]]
- [[12 Matrix and Non-Cooperative Games]] - the same payment matrix, but the enemy is reasonable
- [[15 Statistical Games]] - Bayes-Laplace principle and Hurwitz principle for statistics