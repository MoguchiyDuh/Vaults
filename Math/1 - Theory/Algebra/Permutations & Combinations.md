---
tags:
  - math/algebra
  - combinatorics
  - permutations
  - combinations
related:
  - '[[Binomials]]'
  - '[[Algebra MOC]]'
---

## Permutations #permutations
A **permutation** is an arrangement of objects in a specific order. **The order of arrangement matters in permutations.**

### Formula for Permutations #formula
The number of permutations of $n$ objects taken $r$ at a time is given by:
### $$\boxed{P(n, r) = \frac{n!}{(n - r)!}}$$


<p style="text-align: center; font-weight: bold;">Permutation of all items:</p>

### $$\boxed{P = n!}$$

<p style="text-align: center; font-weight: bold;">When you have identical items</p>

### $$\boxed{P = \frac{n!}{n_1! \times n_2! \times \cdots \times n_k!}}$$

Where:
- $n$: Total number of distinct items
- $r$: Number of objects selected.
- *If $r > n$, permutations are not possible ($P(n, r) = 0$).*



### Permutation Example
You have **5 friends**: Alice (A), Bob (B), Charlie (C), Diana (D), and Emma (E).
Imagine you are organizing a photo shoot where **3 friends** will stand in a line , and the order in which they stand matters (e.g., who stands first, second, or third).

The number of ways to arrange 3 friends out of 5 is given by the permutation formula:
### $$P(5,3) = \frac{5!}{(5-3)!}=\frac{120}{2}=60$$
So, there are **60 different ways** to arrange 3 friends in a line. For example: ABC, ACB, BAC, BCA, CAB, CBA.

---

## Combinations #combinations
A **combination** is a selection of objects where the order does not matter. Unlike permutations, combinations focus only on the group of selected objects.

### Formula for Combinations #formula
The number of combinations of $n$ objects taken $r$ at a time is given by:
### $$\boxed{C(n, r) = \frac{n!}{r!(n - r)!}}$$
Where:
- $n!$: Factorial of $n$.
- $r!$: Factorial of $r$.
- $(n - r)!$: Factorial of $(n - r)$.

### Combination Example
You have the same **5 friends**: Alice (A), Bob (B), Charlie (C), Diana (D), and Emma (E).
Now imagine you are forming a **team of 3 friends** to work on a project. In this case, the order in which you select them does not matter —a team with Alice, Bob, and Charlie is the same as a team with Charlie, Bob, and Alice.

The number of ways to select 3 friends out of 5 is given by the combination formula:
### $$C(5,3) = \frac{5!}{3!(5-3)!}=\frac{120}{6\cdot2}=10$$


So, there are **10 different teams** possible. For example: {Alice, Bob, Charlie}, {Alice, Bob, Diana}, {Alice, Bob, Emma}, etc.

---

## 4. Special Cases
### Case 1: Repetition Allowed
If repetition of objects is allowed:
- **Permutations**: The number of arrangements is $\boxed{n^r}$.
- **Combinations**: Use the "stars and bars" theorem:
  $$\boxed{C(n + r - 1, r) = \frac{(n + r - 1)!}{r!(n - 1)!}}$$

### Case 2: Circular Permutations
For arranging $n$ objects in a circle, the number of permutations is:
$$\boxed{(n - 1)!}$$

---

## Summary
| FEATURE           | PERMUTATIONS                    | COMBINATIONS                      |
| ----------------- | ------------------------------- | --------------------------------- |
| **Order Matters** | Yes                             | No                                |
| **Example**       | Arranging 3 friends in a line   | Selecting 3 friends for a team    |
| **Formula**       | $P(n, r) = \frac{n!}{(n - r)!}$ | $C(n, r) = \frac{n!}{r!(n - r)!}$ |


---

## See Also
- [[Binomials]] - Binomial coefficients
- [[Algebra MOC]] - Algebra topics overview
