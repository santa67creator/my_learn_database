---
tags: [terver, lecture2]
---

# Lecture 2. Basic concepts of probability theory. Event classification

## Key definitions

- **Random phenomenon** - with a massive repetition of an experiment under unchanged conditions, each time it proceeds somewhat differently.
- **Random event** is an event that may or may not occur as a result of an experiment. Denoted by $A, B, C, \ldots$
- **Incompatible events** - the appearance of one excludes the appearance of the other.
- **Joint events** - the appearance of one does not exclude the appearance of the other.
- **Opposite events** $A$ and $\overline{A}$ are incompatible, and one of them will definitely happen.
- **Reliable event** - will definitely happen (the only outcome).
- **Impossible event** - cannot happen.
- **Equally possible events** - there is no reason to consider one more probable than the other.
- **Full group of events** - incompatible events, one of which will definitely occur as a result of experience.

## Relative frequency and classical definition

Relative frequency of the $A$ event in $n$ experiments in which $A$ appeared $m$ times:
$$W(A) = \frac{m}{n}$$

**Classical definition of probability:**
$$P(A) = \frac{m}{n}$$
where $m$ is the number of elementary outcomes favorable to $A$, $n$ is the total number of equally possible outcomes.

## Properties of probability

1.$P(\text{достоверного события}) = 1$
2. $P(\text{невозможного события}) = 0$
3. $0 \le P(A) \le 1$ for any random event

> [!example] Example 1 - painted part
> There are 50 parts in the box, 5 painted. Find the probability of removing the painted part.
>$$P(A) = \frac{5}{50} = 0{,}1$$

> [!example] Example 2 - the word “SORT”
> On 6 cards there are letters A, T, M, P, O, S. Find the probability that 4 cards taken out one at a time will form the word “SORT”.
> Total number of selections - placements from 6 to 4: $A_6^4 = 6\cdot5\cdot4\cdot3 = 360$. There is only one favorable outcome.
>$$P(A) = \frac{1}{360}$$

> [!example] Example 3 - colored ball
> There are 4 balls in the urn: 2 red, 1 blue, 1 white. One ball is drawn at random. Find the probability that it is colored (not white).
> Favorable outcomes 3 out of 4:
>$$P(A) = \frac{3}{4} = 0{,}75$$

## Related notes
-[[00 Contents]]
-[[03 Geometric Probability and Event Operations]]