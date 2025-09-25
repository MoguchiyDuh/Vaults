---
tags:
  - algebra
  - matrices
---

## Introduction
A **matrix** is a rectangular array of numbers, symbols, or expressions arranged in rows and columns. Matrices are widely used in mathematics, physics, computer science, engineering, and other fields to represent and solve systems of linear equations, transformations, and data structures.

---

## Basic Definitions

### Matrix Notation
A matrix is typically written as:
$$
A = \begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \dots & a_{mn}
\end{bmatrix}
$$
Where:
- $m$: Number of rows.
- $n$: Number of columns.
- $a_{ij}$: Element in the $i$-th row and $j$-th column.

### Dimensions of a Matrix
The dimensions of a matrix are given as:
### $$\text{Dimensions} = m \times n$$
For example, a $3 \times 2$ matrix has 3 rows and 2 columns.

---

## Matrix Operations

### Addition
Two matrices of the same dimensions can be added element-wise:
$$
\boxed{\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
+
\begin{bmatrix}
e & f \\
g & h
\end{bmatrix}
=
\begin{bmatrix}
a+e & b+f \\
c+g & d+h
\end{bmatrix}}
$$

### Scalar Multiplication
Multiply each element of the matrix by a scalar $k$:
$$
\boxed{k \cdot \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
=
\begin{bmatrix}
k \cdot a & k \cdot b \\
k \cdot c & k \cdot d
\end{bmatrix}}
$$

### Matrix Multiplication
To multiply two matrices $A(m \times n)$ and $B(n \times p)$, the result is a matrix $C(m \times p)$. Each entry $c_{ij}$ in the resulting matrix $C$ is the **dot product** of the $i$-th row of $A$ and the $j$-th column of $B$:
$$
\boxed{C_{ij} = \sum_{k=1}^{n} A_{ik} \cdot B_{kj}}
$$
Example:
$$
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
\cdot
\begin{bmatrix}
5 & 6 \\
7 & 8
\end{bmatrix}
=
\begin{bmatrix}
(1 \cdot 5 + 2 \cdot 7) & (1 \cdot 6 + 2 \cdot 8) \\
(3 \cdot 5 + 4 \cdot 7) & (3 \cdot 6 + 4 \cdot 8)
\end{bmatrix}
=
\begin{bmatrix}
19 & 22 \\
43 & 50
\end{bmatrix}
$$

---

## Special Properties

### Transpose of a Matrix
The transpose of a matrix $A(m \times n)$ is obtained by swapping its rows and columns:
$$
\boxed{A^T = \begin{bmatrix}
a_{11} & a_{21} & \dots & a_{m1} \\
a_{12} & a_{22} & \dots & a_{m2} \\
\vdots & \vdots & \ddots & \vdots \\
a_{1n} & a_{2n} & \dots & a_{mn}
\end{bmatrix}}
$$

### Symmetric Matrix
A square matrix is symmetric if $A = A^T$:
$$
\boxed{B = \begin{bmatrix}
1 & 2 & 3 \\
2 & 4 & 5 \\
3 & 5 & 6
\end{bmatrix}}
$$

### Determinant
The determinant is a scalar value associated with a square matrix.
### $$\boxed{\text{det}(A)=a(ei−fh)−b(di−fg)+c(dh−eg)}$$
### #Rule_of_Sarrus :
1. Rewrite the first two columns of the matrix to the right:

$$\begin{bmatrix}
a & b & c & \color{gray}{a} & \color{gray}{b} \\
d & e & f & \color{gray}{d} & \color{gray}{e} \\
g & h & i & \color{gray}{g} & \color{gray}{h}
\end{bmatrix}$$

2. Add the products of the downward diagonals:

$$
+ aei + bfg + cdh
$$

3. Subtract the products of the upward diagonals:

$$
- ceg - bdi - afh
$$

### $$\boxed{\text{det}(A) = (aei + bfg + cdh) - (ceg + bdi + afh)}$$



### Inverse of a Matrix
A square matrix $A$ has an inverse $A^{-1}$ if $\text{det}(A) \neq 0$. The inverse satisfies:
$$
\boxed{A \cdot A^{-1} = I}
$$

---

## Applications of Matrices

### Systems of Linear Equations
Matrices are used to represent and solve systems of linear equations:
$$
\boxed{\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
\cdot
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
\begin{bmatrix}
e \\
f
\end{bmatrix}}
$$

## Cramer's Rule for 3 Variables #cramers_rule
<img src="Pictures/cramers_rule.png" width=500 height="auto" style="display: block; margin: auto">

For a system of linear equations:

$$
\begin{cases}
a_1x + b_1y + c_1z = d_1 \\
a_2x + b_2y + c_2z = d_2 \\
a_3x + b_3y + c_3z = d_3
\end{cases}
$$

The solution can be found using determinants:

### Main Determinant ($D$)
Find the main determinant using the #Rule_of_Sarrus 


### Variable Determinants

- ### For $x$ ($D_x$):
Replace first column with constants

$$
D_x = \begin{vmatrix}
d_1 & b_1 & c_1 \\
d_2 & b_2 & c_2 \\
d_3 & b_3 & c_3 \\
\end{vmatrix}
$$

- ### For $y$ ($D_y$):
Replace second column with constants

$$
D_y = \begin{vmatrix}
a_1 & d_1 & c_1 \\
a_2 & d_2 & c_2 \\
a_3 & d_3 & c_3 \\
\end{vmatrix}
$$

- ### For $z$ ($D_z$):
Replace third column with constants

$$
D_z = \begin{vmatrix}
a_1 & b_1 & d_1 \\
a_2 & b_2 & d_2 \\
a_3 & b_3 & d_3 \\
\end{vmatrix}
$$

## Solution

If $D \neq 0$, the system has a unique solution:

$$
x = \frac{D_x}{D}, \quad y = \frac{D_y}{D}, \quad z = \frac{D_z}{D}
$$

If $D = 0$ and at least one $D_i \neq 0$, the system is inconsistent.  
If $D = 0$ and all $D_i = 0$, the system may have infinitely many solutions or no solution.