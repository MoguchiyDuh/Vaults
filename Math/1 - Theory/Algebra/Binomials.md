---
tags:
  - algebra
  - binomials
---
## Definition
A binomial is a [[Polynomials|polynomial]] with exactly two terms.

## Notation
- **n**: Exponent (non-negative integer)
- **a, b**: Terms in the polinom expression
- **k**: Index of the term in the expansion (from 0)
- **C(n, k)**: Polinom coefficient, also written as <h3>$\binom{n}{k}$</h3>
---
## General Formula #binomials  #fomula
The Binomial Theorem states that:
### $$\boxed{(a + b)^n = \sum_{k=0}^{n} \binom{n}{k} a^{n-k} b^k}$$
Where:
### $\binom{n}{k} = \frac{n!}{k!(n-k)!}$ is the polinom coefficient.
---

## Expanded Form
The expanded form of $(a + b)^n$ is:
### $$\boxed{(a + b)^n = a^n + \binom{n}{1} a^{n-1}b + \binom{n}{2} a^{n-2}b^2 + \dots + b^n}$$

---

## General Term
The general term in the expansion of $(a + b)^n$ is:
### $$\boxed{T_k = \binom{n}{k} a^{n-k} b^k}$$
Where:
- $T_k$ is the $(k+1)$-th term in the expansion.
- $k$ ranges from 0 to $n$.

---
## Pascal's Triangle
```
				1
              1   1
            1   2   1
          1   3   3   1
        1   4   6   4   1
      1   5  10  10   5   1
    1   6  15  20  15   6   1
```
**Rule:** Each number = sum of two numbers above it
**Row n:** Contains coefficients for $(a + b)^n$

## Sum of coefficients $2^n$
