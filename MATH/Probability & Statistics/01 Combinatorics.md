---
tags: [terver, lecture 1, combinatorics]
---

# Lecture 1. Elements of combinatorics

Combinatorics studies the number of combinations, subject to certain conditions, that can be made from a finite set of objects.

## Multiplication rule

If the $A_1$ object can be selected in $k_1$ ways, then (for each $A_1$ selection) the $A_2$ object can be selected in $k_2$ ways, etc. to the object $A_n$ - $k_n$ in ways, then the selection of all $n$ objects together can be carried out
$$k_1 \cdot k_2 \cdot \ldots \cdot k_n$$
ways.

## Addition rule

If the actions of $A_1, A_2, \ldots, A_m$ are independent (the execution of any one does not depend on the others) and $A_i$ can be performed in $k_i$ methods, then **any one** of them can be performed
$$k_1 + k_2 + \ldots + k_m$$
ways.

## Three types of connections

| View | Differ | Designation | Formula |
|---|---|---|---|
| Placements | elements or order | $A_n^m$ | $A_n^m = \dfrac{n!}{(n-m)!}$ |
| Permutations | only in order (all $n$ elements) | $P_n$ | $P_n = n!$ |
| Combinations | only elements | $C_n^m$ | $C_n^m = \dfrac{n!}{m!\,(n-m)!}$ |

Rule of symmetry of combinations: $C_n^m = C_n^{n-m}$.

> [!example] Example 1 - three-digit even numbers
> How many three-digit even numbers can be made from the digits 0,1,2,3,4,5,6, if the digits can be repeated?
> **Solution.** The first digit is any except 0 (6 options), the second is any of 7, the third is even: 0,2,4,6 (4 options).
>$$6 \cdot 7 \cdot 4 = 168$$

> [!example] Example 2 - telephone numbers
> How many seven-digit phone numbers are there where not a single digit is repeated?
>$$A_{10}^{7} = \frac{10!}{(10-7)!} = 604\,800$$

> [!example] Example 3 - six-digit even numbers without repetitions
> Of the numbers 1,3,4,5,7,9 (without repetitions), the number must be even.
> The only even digit is 4, it must be in the ones place. The remaining 5 digits are rearranged in the remaining places:
>$$P_5 = 5! = 120$$

> [!example] Example 4 - team of 12 people
> In how many ways can a team of 4 be selected from 12 people?
> $$C_{12}^{4} = \frac{12!}{4!\,(12-4)!} = 495$$

> [!example] Example 5 - commission (addition rule)
> From 2 mathematicians and 10 economists, create a commission of 8 people so that there is at least one mathematician in it.
> **Solution.** Two non-overlapping cases: 1 mathematician + 7 economists, or 2 mathematicians + 6 economists.
> $$C_2^1 \cdot C_{10}^7 = 2 \cdot 120 = 240$$
>$$C_2^2 \cdot C_{10}^6 = 1 \cdot 210 = 210$$
> According to the addition rule: $240 + 210 = 450$.

## Related notes
- [[00 Contents]]
- [[09 Binomial and Geometric Distribution]] - combinations occur again in Bernoulli’s formula