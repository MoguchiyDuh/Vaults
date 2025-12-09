# Matrices - Complete Guide

A **matrix** is a rectangular array of numbers, symbols, or expressions arranged in rows and columns. Matrices are fundamental to linear algebra and have extensive applications in mathematics, physics, computer graphics, machine learning, and engineering.

---

## Definition and Notation

### Matrix Definition

A matrix is denoted by a capital letter and defined by its elements:

$$\boxed{A = \begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{bmatrix}}$$

Where:
- $a_{ij}$ is the element in row $i$, column $j$
- $m$ is the number of rows
- $n$ is the number of columns

---

### Dimension (Order/Size)

The **dimension** of a matrix is written as $m \times n$ (read as "$m$ by $n$").

$$\boxed{\text{Dimension} = m \times n}$$

**Examples:**

$$A = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{bmatrix} \quad \text{Dimension: } 2 \times 3$$

$$B = \begin{bmatrix}
7 \\
8 \\
9
\end{bmatrix} \quad \text{Dimension: } 3 \times 1$$

$$C = \begin{bmatrix}
1 & 2 \\
3 & 4 \\
5 & 6
\end{bmatrix} \quad \text{Dimension: } 3 \times 2$$

---

### Element Notation

$$\boxed{A_{ij} \text{ or } a_{ij}}$$

Represents the element in the $i$-th row and $j$-th column.

**Example:**
$$A = \begin{bmatrix}
2 & 5 & 1 \\
3 & 7 & 9
\end{bmatrix}$$

- $a_{11} = 2$ (row 1, column 1)
- $a_{12} = 5$ (row 1, column 2)
- $a_{23} = 9$ (row 2, column 3)

---

## Types of Matrices

### Square Matrix

A matrix where the number of rows equals the number of columns ($m = n$).

$$\boxed{A = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}} \quad (3 \times 3)$$

---

### Row Matrix (Row Vector)

A matrix with only one row ($m = 1$).

$$\boxed{A = \begin{bmatrix}
1 & 2 & 3 & 4
\end{bmatrix}} \quad (1 \times 4)$$

---

### Column Matrix (Column Vector)

A matrix with only one column ($n = 1$).

$$\boxed{A = \begin{bmatrix}
1 \\
2 \\
3 \\
4
\end{bmatrix}} \quad (4 \times 1)$$

---

### Diagonal Matrix

A square matrix where all non-diagonal elements are zero.

$$\boxed{D = \begin{bmatrix}
d_1 & 0 & 0 \\
0 & d_2 & 0 \\
0 & 0 & d_3
\end{bmatrix}}$$

**Example:**
$$D = \begin{bmatrix}
5 & 0 & 0 \\
0 & -2 & 0 \\
0 & 0 & 7
\end{bmatrix}$$

---

### Identity Matrix

A diagonal matrix where all diagonal elements are 1.

$$\boxed{I_n = \begin{bmatrix}
1 & 0 & 0 & \cdots & 0 \\
0 & 1 & 0 & \cdots & 0 \\
0 & 0 & 1 & \cdots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \cdots & 1
\end{bmatrix}}$$

**Properties:**
- $AI = IA = A$ (identity property)
- $I^n = I$ for any positive integer $n$

**Examples:**
$$I_2 = \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}, \quad I_3 = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}$$

---

### Zero Matrix (Null Matrix)

A matrix where all elements are zero.

$$\boxed{O = \begin{bmatrix}
0 & 0 & \cdots & 0 \\
0 & 0 & \cdots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & 0
\end{bmatrix}}$$

**Properties:**
- $A + O = A$
- $AO = OA = O$

**Example:**
$$O_{2 \times 3} = \begin{bmatrix}
0 & 0 & 0 \\
0 & 0 & 0
\end{bmatrix}$$

---

### Symmetric Matrix

A square matrix that equals its transpose: $A = A^T$

$$\boxed{a_{ij} = a_{ji} \text{ for all } i, j}$$

**Example:**
$$A = \begin{bmatrix}
1 & 2 & 3 \\
2 & 5 & 6 \\
3 & 6 & 9
\end{bmatrix}$$

Note: $a_{12} = a_{21} = 2$, $a_{13} = a_{31} = 3$, etc.

---

### Skew-Symmetric Matrix

A square matrix where $A^T = -A$

$$\boxed{a_{ij} = -a_{ji} \text{ for all } i, j}$$

**Properties:**
- All diagonal elements must be zero
- $a_{ii} = 0$

**Example:**
$$A = \begin{bmatrix}
0 & 2 & -3 \\
-2 & 0 & 5 \\
3 & -5 & 0
\end{bmatrix}$$

---

### Upper Triangular Matrix

A square matrix where all elements below the main diagonal are zero.

$$\boxed{U = \begin{bmatrix}
u_{11} & u_{12} & u_{13} & \cdots \\
0 & u_{22} & u_{23} & \cdots \\
0 & 0 & u_{33} & \cdots \\
\vdots & \vdots & \vdots & \ddots
\end{bmatrix}}$$

**Example:**
$$U = \begin{bmatrix}
2 & 3 & 4 \\
0 & 5 & 6 \\
0 & 0 & 7
\end{bmatrix}$$

---

### Lower Triangular Matrix

A square matrix where all elements above the main diagonal are zero.

$$\boxed{L = \begin{bmatrix}
l_{11} & 0 & 0 & \cdots \\
l_{21} & l_{22} & 0 & \cdots \\
l_{31} & l_{32} & l_{33} & \cdots \\
\vdots & \vdots & \vdots & \ddots
\end{bmatrix}}$$

**Example:**
$$L = \begin{bmatrix}
2 & 0 & 0 \\
3 & 5 & 0 \\
4 & 6 & 7
\end{bmatrix}$$

---

### Orthogonal Matrix

A square matrix $Q$ where:
$$\boxed{Q^T Q = Q Q^T = I}$$

Equivalently: $\boxed{Q^T = Q^{-1}}$

**Properties:**
- Preserves lengths and angles
- Represents rotations and reflections
- Determinant is $\pm 1$

**Example:**
$$Q = \frac{1}{\sqrt{2}}\begin{bmatrix}
1 & 1 \\
-1 & 1
\end{bmatrix}$$

---

### Singular Matrix

A square matrix that does **not** have an inverse.

$$\boxed{\det(A) = 0}$$

**Example:**
$$A = \begin{bmatrix}
1 & 2 \\
2 & 4
\end{bmatrix} \quad (\det(A) = 4 - 4 = 0)$$

---

### Non-Singular (Invertible) Matrix

A square matrix that **has** an inverse.

$$\boxed{\det(A) \neq 0}$$

**Example:**
$$A = \begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix} \quad (\det(A) = 4 - 6 = -2 \neq 0)$$

---

## Matrix Operations

### Addition

Matrices of the **same dimensions** can be added element-wise.

$$\boxed{C = A + B \quad \Rightarrow \quad c_{ij} = a_{ij} + b_{ij}}$$

**Example:**
$$\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
+
\begin{bmatrix}
5 & 6 \\
7 & 8
\end{bmatrix}
=
\begin{bmatrix}
6 & 8 \\
10 & 12
\end{bmatrix}$$

**Properties:**
- **Commutative:** $A + B = B + A$
- **Associative:** $(A + B) + C = A + (B + C)$
- **Identity:** $A + O = A$

---

### Subtraction

$$\boxed{C = A - B \quad \Rightarrow \quad c_{ij} = a_{ij} - b_{ij}}$$

**Example:**
$$\begin{bmatrix}
5 & 7 \\
9 & 11
\end{bmatrix}
-
\begin{bmatrix}
2 & 3 \\
4 & 5
\end{bmatrix}
=
\begin{bmatrix}
3 & 4 \\
5 & 6
\end{bmatrix}$$

---

### Scalar Multiplication

Multiply each element by a scalar $k$.

$$\boxed{B = kA \quad \Rightarrow \quad b_{ij} = k \cdot a_{ij}}$$

**Example:**
$$3 \times \begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
=
\begin{bmatrix}
3 & 6 \\
9 & 12
\end{bmatrix}$$

**Properties:**
- $k(A + B) = kA + kB$
- $(k + m)A = kA + mA$
- $(km)A = k(mA)$
- $1A = A$

---

### Matrix Multiplication

For $A_{m \times n}$ and $B_{n \times p}$, the product $C = AB$ is $m \times p$.

$$\boxed{c_{ij} = \sum_{k=1}^{n} a_{ik} \cdot b_{kj}}$$

**Requirement:** Number of columns in $A$ must equal number of rows in $B$.

**Example:**
$$\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
\times
\begin{bmatrix}
5 & 6 \\
7 & 8
\end{bmatrix}
=
\begin{bmatrix}
1(5)+2(7) & 1(6)+2(8) \\
3(5)+4(7) & 3(6)+4(8)
\end{bmatrix}
=
\begin{bmatrix}
19 & 22 \\
43 & 50
\end{bmatrix}$$

**Properties:**
- **NOT Commutative:** $AB \neq BA$ (in general)
- **Associative:** $(AB)C = A(BC)$
- **Distributive:** $A(B + C) = AB + AC$
- **Identity:** $AI = IA = A$

**Example showing non-commutativity:**
$$A = \begin{bmatrix}
1 & 2 \\
0 & 1
\end{bmatrix}, \quad B = \begin{bmatrix}
1 & 0 \\
3 & 1
\end{bmatrix}$$

$$AB = \begin{bmatrix}
7 & 2 \\
3 & 1
\end{bmatrix}, \quad BA = \begin{bmatrix}
1 & 2 \\
3 & 7
\end{bmatrix} \quad (AB \neq BA)$$

---

### Transpose

The transpose of matrix $A$ is denoted $A^T$ and obtained by swapping rows and columns.

$$\boxed{(A^T)_{ij} = A_{ji}}$$

**Example:**
$$A = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{bmatrix} \quad \Rightarrow \quad A^T = \begin{bmatrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{bmatrix}$$

**Properties:**
- $(A^T)^T = A$
- $(A + B)^T = A^T + B^T$
- $(kA)^T = kA^T$
- $(AB)^T = B^T A^T$ (reverse order!)

---

## Determinant

The **determinant** is a scalar value associated with square matrices.

### 2×2 Determinant

$$\boxed{\det\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} = ad - bc}$$

**Example:**
$$\det\begin{pmatrix}
3 & 5 \\
2 & 4
\end{pmatrix} = 3(4) - 5(2) = 12 - 10 = 2$$

---

### 3×3 Determinant (Rule of Sarrus)

$$\boxed{\det(A) = a_{11}(a_{22}a_{33} - a_{23}a_{32}) - a_{12}(a_{21}a_{33} - a_{23}a_{31}) + a_{13}(a_{21}a_{32} - a_{22}a_{31})}$$

**Alternative (Rule of Sarrus):**

1. Rewrite first two columns:
$$\begin{bmatrix}
a & b & c & \color{gray}{a} & \color{gray}{b} \\
d & e & f & \color{gray}{d} & \color{gray}{e} \\
g & h & i & \color{gray}{g} & \color{gray}{h}
\end{bmatrix}$$

2. Add products of downward diagonals:
$$+aei + bfg + cdh$$

3. Subtract products of upward diagonals:
$$-ceg - bdi - afh$$

$$\boxed{\det(A) = (aei + bfg + cdh) - (ceg + bdi + afh)}$$

**Example:**
$$\det\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 4 \\
5 & 6 & 0
\end{pmatrix} = (1 \cdot 1 \cdot 0 + 2 \cdot 4 \cdot 5 + 3 \cdot 0 \cdot 6) - (3 \cdot 1 \cdot 5 + 2 \cdot 0 \cdot 0 + 1 \cdot 4 \cdot 6)$$
$$= (0 + 40 + 0) - (15 + 0 + 24) = 40 - 39 = 1$$

<img src="Pictures/rule_of_sarrus.png" width=500 height="auto" style="display: block; margin: auto">

---

### Cofactor Expansion (Laplace Expansion)

For any $n \times n$ matrix, expand along any row or column:

**Along row $i$:**
$$\boxed{\det(A) = \sum_{j=1}^{n} (-1)^{i+j} a_{ij} M_{ij}}$$

**Along column $j$:**
$$\boxed{\det(A) = \sum_{i=1}^{n} (-1)^{i+j} a_{ij} M_{ij}}$$

Where $M_{ij}$ is the **minor** (determinant of submatrix after removing row $i$ and column $j$).

**Example (expand along first row):**
$$\det\begin{pmatrix}
2 & 3 & 1 \\
4 & 1 & 2 \\
5 & 0 & 3
\end{pmatrix} = 2 \det\begin{pmatrix}
1 & 2 \\
0 & 3
\end{pmatrix} - 3 \det\begin{pmatrix}
4 & 2 \\
5 & 3
\end{pmatrix} + 1 \det\begin{pmatrix}
4 & 1 \\
5 & 0
\end{pmatrix}$$

$$= 2(3) - 3(2) + 1(-5) = 6 - 6 - 5 = -5$$

---

### Properties of Determinants

1. $\det(I) = 1$
2. $\det(A^T) = \det(A)$
3. $\det(AB) = \det(A) \cdot \det(B)$
4. $\det(kA) = k^n \det(A)$ for $n \times n$ matrix
5. $\det(A^{-1}) = \frac{1}{\det(A)}$ if $A$ is invertible
6. If two rows (or columns) are identical, $\det(A) = 0$
7. Swapping two rows (or columns) changes sign: $\det(A) \to -\det(A)$
8. If a row is multiplied by $k$, $\det$ is multiplied by $k$
9. Determinant of triangular matrix = product of diagonal elements

---

## Matrix Inverse

### Definition

The inverse of matrix $A$ is $A^{-1}$ such that:
$$\boxed{AA^{-1} = A^{-1}A = I}$$

**Existence:** $A^{-1}$ exists if and only if $\det(A) \neq 0$

---

### 2×2 Matrix Inverse

$$\boxed{A^{-1} = \frac{1}{\det(A)} \begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}}$$

Where $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$ and $\det(A) = ad - bc \neq 0$

**Example:**
$$A = \begin{bmatrix}
3 & 5 \\
2 & 4
\end{bmatrix}$$

$$\det(A) = 12 - 10 = 2$$

$$A^{-1} = \frac{1}{2} \begin{bmatrix}
4 & -5 \\
-2 & 3
\end{bmatrix} = \begin{bmatrix}
2 & -2.5 \\
-1 & 1.5
\end{bmatrix}$$

**Verification:**
$$AA^{-1} = \begin{bmatrix}
3 & 5 \\
2 & 4
\end{bmatrix} \begin{bmatrix}
2 & -2.5 \\
-1 & 1.5
\end{bmatrix} = \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix} = I$$

---

### General Inverse (Adjugate Method)

$$\boxed{A^{-1} = \frac{1}{\det(A)} \text{adj}(A)}$$

Where $\text{adj}(A)$ is the **adjugate** (transpose of cofactor matrix).

**Steps:**
1. Find cofactor matrix $C$ where $C_{ij} = (-1)^{i+j} M_{ij}$
2. Transpose to get adjugate: $\text{adj}(A) = C^T$
3. Divide by determinant: $A^{-1} = \frac{1}{\det(A)} \text{adj}(A)$

**Example:**
$$A = \begin{bmatrix}
1 & 2 & 3 \\
0 & 1 & 4 \\
5 & 6 & 0
\end{bmatrix}$$

(Detailed calculation would follow the steps above)

---

### Inverse by Gaussian Elimination

Augment $A$ with $I$ and row reduce to $[I | A^{-1}]$:

$$\boxed{[A | I] \xrightarrow{\text{row operations}} [I | A^{-1}]}$$

**Example:**
$$A = \begin{bmatrix}
2 & 1 \\
1 & 1
\end{bmatrix}$$

$$\begin{bmatrix}
2 & 1 & | & 1 & 0 \\
1 & 1 & | & 0 & 1
\end{bmatrix}
\xrightarrow{\text{operations}}
\begin{bmatrix}
1 & 0 & | & 1 & -1 \\
0 & 1 & | & -1 & 2
\end{bmatrix}$$

$$A^{-1} = \begin{bmatrix}
1 & -1 \\
-1 & 2
\end{bmatrix}$$

---

### Properties of Inverse

1. $(A^{-1})^{-1} = A$
2. $(AB)^{-1} = B^{-1}A^{-1}$ (reverse order!)
3. $(A^T)^{-1} = (A^{-1})^T$
4. $\det(A^{-1}) = \frac{1}{\det(A)}$
5. $(kA)^{-1} = \frac{1}{k}A^{-1}$ for $k \neq 0$

---

## Rank of a Matrix

The **rank** of a matrix is the maximum number of linearly independent rows (or columns).

$$\boxed{\text{rank}(A) \leq \min(m, n)}$$

**Methods to find rank:**
1. Row reduction to row echelon form
2. Count non-zero rows
3. Largest non-zero minor

**Example:**
$$A = \begin{bmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
1 & 1 & 1
\end{bmatrix}$$

Row reduce:
$$\begin{bmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & -1 & -2
\end{bmatrix}$$

Rank = 2 (two non-zero rows)

**Properties:**
- $\text{rank}(A) = \text{rank}(A^T)$
- $\text{rank}(AB) \leq \min(\text{rank}(A), \text{rank}(B))$
- $\text{rank}(A + B) \leq \text{rank}(A) + \text{rank}(B)$
- Full rank: $\text{rank}(A) = \min(m, n)$

---

## Trace

The **trace** is the sum of diagonal elements of a square matrix.

$$\boxed{\text{tr}(A) = \sum_{i=1}^{n} a_{ii}}$$

**Example:**
$$A = \begin{bmatrix}
3 & 5 & 1 \\
2 & 4 & 7 \\
6 & 8 & 9
\end{bmatrix}$$

$$\text{tr}(A) = 3 + 4 + 9 = 16$$

**Properties:**
1. $\text{tr}(A + B) = \text{tr}(A) + \text{tr}(B)$
2. $\text{tr}(kA) = k \cdot \text{tr}(A)$
3. $\text{tr}(AB) = \text{tr}(BA)$
4. $\text{tr}(A^T) = \text{tr}(A)$
5. $\text{tr}(I_n) = n$
6. For eigenvalues $\lambda_1, \ldots, \lambda_n$: $\text{tr}(A) = \sum \lambda_i$

---

## Eigenvalues and Eigenvectors

### Definition

For square matrix $A$, if there exists a non-zero vector $\mathbf{v}$ and scalar $\lambda$ such that:

$$\boxed{A\mathbf{v} = \lambda\mathbf{v}}$$

Then:
- $\lambda$ is an **eigenvalue**
- $\mathbf{v}$ is an **eigenvector** corresponding to $\lambda$

---

### Finding Eigenvalues

Solve the **characteristic equation**:

$$\boxed{\det(A - \lambda I) = 0}$$

**Example:**
$$A = \begin{bmatrix}
4 & 1 \\
2 & 3
\end{bmatrix}$$

$$\det\begin{pmatrix}
4-\lambda & 1 \\
2 & 3-\lambda
\end{pmatrix} = 0$$

$$(4-\lambda)(3-\lambda) - 2 = 0$$
$$\lambda^2 - 7\lambda + 10 = 0$$
$$(\lambda - 5)(\lambda - 2) = 0$$

Eigenvalues: $\lambda_1 = 5$, $\lambda_2 = 2$

---

### Finding Eigenvectors

For each eigenvalue $\lambda$, solve:
$$\boxed{(A - \lambda I)\mathbf{v} = \mathbf{0}}$$

**Example (continued):**

For $\lambda_1 = 5$:
$$\begin{bmatrix}
-1 & 1 \\
2 & -2
\end{bmatrix} \begin{bmatrix}
v_1 \\
v_2
\end{bmatrix} = \begin{bmatrix}
0 \\
0
\end{bmatrix}$$

Solution: $v_1 = v_2$, so $\mathbf{v}_1 = \begin{bmatrix} 1 \\ 1 \end{bmatrix}$ (or any scalar multiple)

For $\lambda_2 = 2$:
$$\begin{bmatrix}
2 & 1 \\
2 & 1
\end{bmatrix} \begin{bmatrix}
v_1 \\
v_2
\end{bmatrix} = \begin{bmatrix}
0 \\
0
\end{bmatrix}$$

Solution: $2v_1 + v_2 = 0$, so $\mathbf{v}_2 = \begin{bmatrix} 1 \\ -2 \end{bmatrix}$

---

### Properties of Eigenvalues

1. **Sum of eigenvalues** = $\text{tr}(A)$
   $$\sum_{i=1}^{n} \lambda_i = \text{tr}(A)$$

2. **Product of eigenvalues** = $\det(A)$
   $$\prod_{i=1}^{n} \lambda_i = \det(A)$$

3. Eigenvalues of $A^T$ = eigenvalues of $A$
4. Eigenvalues of $A^{-1}$ = $\frac{1}{\lambda_i}$
5. Eigenvalues of $kA$ = $k\lambda_i$
6. Eigenvalues of $A^n$ = $\lambda_i^n$

---

### Diagonalization

A matrix $A$ is **diagonalizable** if it can be written as:

$$\boxed{A = PDP^{-1}}$$

Where:
- $D$ is diagonal matrix of eigenvalues
- $P$ is matrix of eigenvectors

**Condition:** $A$ has $n$ linearly independent eigenvectors

**Example:**
$$A = \begin{bmatrix}
4 & 1 \\
2 & 3
\end{bmatrix}, \quad \lambda_1 = 5, \lambda_2 = 2$$

$$P = \begin{bmatrix}
1 & 1 \\
1 & -2
\end{bmatrix}, \quad D = \begin{bmatrix}
5 & 0 \\
0 & 2
\end{bmatrix}$$

$$A = PDP^{-1}$$

**Benefits:**
- $A^n = PD^nP^{-1}$ (easy to compute)
- Simplifies matrix powers and exponentials

---

## Systems of Linear Equations

### Matrix Form

A system of linear equations:
$$\begin{cases}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n = b_1 \\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n = b_2 \\
\vdots \\
a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n = b_m
\end{cases}$$

Can be written as:
$$\boxed{A\mathbf{x} = \mathbf{b}}$$

Where:
$$A = \begin{bmatrix}
a_{11} & \cdots & a_{1n} \\
\vdots & \ddots & \vdots \\
a_{m1} & \cdots & a_{mn}
\end{bmatrix}, \quad \mathbf{x} = \begin{bmatrix}
x_1 \\
\vdots \\
x_n
\end{bmatrix}, \quad \mathbf{b} = \begin{bmatrix}
b_1 \\
\vdots \\
b_m
\end{bmatrix}$$

---

### Solution Methods

#### 1. Matrix Inverse (if $A$ is square and invertible)

$$\boxed{\mathbf{x} = A^{-1}\mathbf{b}}$$

**Example:**
$$\begin{bmatrix}
2 & 1 \\
1 & 1
\end{bmatrix} \begin{bmatrix}
x \\
y
\end{bmatrix} = \begin{bmatrix}
5 \\
3
\end{bmatrix}$$

$$\begin{bmatrix}
x \\
y
\end{bmatrix} = \begin{bmatrix}
1 & -1 \\
-1 & 2
\end{bmatrix} \begin{bmatrix}
5 \\
3
\end{bmatrix} = \begin{bmatrix}
2 \\
1
\end{bmatrix}$$

Solution: $x = 2, y = 1$

---

#### 2. Gaussian Elimination

Row reduce augmented matrix $[A|\mathbf{b}]$ to row echelon form.

**Example:**
$$\begin{bmatrix}
2 & 1 & | & 5 \\
1 & 1 & | & 3
\end{bmatrix}
\xrightarrow{R_1 \leftrightarrow R_2}
\begin{bmatrix}
1 & 1 & | & 3 \\
2 & 1 & | & 5
\end{bmatrix}$$

$$\xrightarrow{R_2 - 2R_1}
\begin{bmatrix}
1 & 1 & | & 3 \\
0 & -1 & | & -1
\end{bmatrix}$$

Back substitution: $y = 1$, $x = 2$

---

#### 3. Cramer's Rule

For square system with $\det(A) \neq 0$:

$$\boxed{x_i = \frac{\det(A_i)}{\det(A)}}$$

Where $A_i$ is $A$ with column $i$ replaced by $\mathbf{b}$.

**Example:**
$$\begin{bmatrix}
2 & 1 \\
1 & 1
\end{bmatrix} \begin{bmatrix}
x \\
y
\end{bmatrix} = \begin{bmatrix}
5 \\
3
\end{bmatrix}$$

$$\det(A) = 2(1) - 1(1) = 1$$

$$x = \frac{\det\begin{bmatrix} 5 & 1 \\ 3 & 1 \end{bmatrix}}{1} = \frac{5 - 3}{1} = 2$$

$$y = \frac{\det\begin{bmatrix} 2 & 5 \\ 1 & 3 \end{bmatrix}}{1} = \frac{6 - 5}{1} = 1$$


---

### Solution Types

1. **Unique solution:** $\text{rank}(A) = \text{rank}([A|\mathbf{b}]) = n$
2. **Infinite solutions:** $\text{rank}(A) = \text{rank}([A|\mathbf{b}]) < n$
3. **No solution:** $\text{rank}(A) < \text{rank}([A|\mathbf{b}])$

---

## Special Matrices and Decompositions

### LU Decomposition

Decompose $A$ into lower and upper triangular matrices:

$$\boxed{A = LU}$$

Where $L$ is lower triangular and $U$ is upper triangular.

**Use:** Efficiently solve multiple systems with same $A$.

**Example:**
$$A = \begin{bmatrix}
2 & 1 \\
4 & 5
\end{bmatrix} = \begin{bmatrix}
1 & 0 \\
2 & 1
\end{bmatrix} \begin{bmatrix}
2 & 1 \\
0 & 3
\end{bmatrix} = LU$$

---

### QR Decomposition

Decompose $A$ into orthogonal and upper triangular matrices:

$$\boxed{A = QR}$$

Where $Q$ is orthogonal ($Q^TQ = I$) and $R$ is upper triangular.

**Use:** Solve least squares problems, eigenvalue algorithms.

---

### Singular Value Decomposition (SVD)

Any $m \times n$ matrix $A$ can be decomposed:

$$\boxed{A = U\Sigma V^T}$$

Where:
- $U$ is $m \times m$ orthogonal (left singular vectors)
- $\Sigma$ is $m \times n$ diagonal (singular values)
- $V$ is $n \times n$ orthogonal (right singular vectors)

**Applications:**
- Data compression
- Principal Component Analysis (PCA)
- Pseudoinverse
- Matrix approximation

---

### Cholesky Decomposition

For positive definite symmetric matrix $A$:

$$\boxed{A = LL^T}$$

Where $L$ is lower triangular with positive diagonal.

**Use:** Faster than LU for positive definite matrices.

---

## Applications

### 1. Computer Graphics

**Transformations:**
- **Translation:** $\mathbf{v}' = \mathbf{v} + \mathbf{t}$
- **Rotation:** $\mathbf{v}' = R\mathbf{v}$
- **Scaling:** $\mathbf{v}' = S\mathbf{v}$

**2D Rotation by $\theta$:**
$$R(\theta) = \begin{bmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta
\end{bmatrix}$$

**2D Scaling:**
$$S = \begin{bmatrix}
s_x & 0 \\
0 & s_y
\end{bmatrix}$$

**Homogeneous coordinates** (4×4 matrices) allow translation:
$$\begin{bmatrix}
1 & 0 & 0 & t_x \\
0 & 1 & 0 & t_y \\
0 & 0 & 1 & t_z \\
0 & 0 & 0 & 1
\end{bmatrix}$$

---

### 2. Machine Learning

**Linear Regression:**
$$\hat{\boldsymbol{\beta}} = (X^TX)^{-1}X^T\mathbf{y}$$

**Neural Networks:**
- Weight matrices transform inputs
- $\mathbf{h} = \sigma(W\mathbf{x} + \mathbf{b})$

**Principal Component Analysis (PCA):**
- Find eigenvectors of covariance matrix
- Reduce dimensionality

---

### 3. Physics

**Quantum Mechanics:**
- States as vectors, operators as matrices
- Hamiltonian matrix for energy

**Mechanics:**
- Moment of inertia tensor
- Stress-strain relationships

**Electrical Engineering:**
- Impedance matrices in circuits
- Signal processing (Fourier transform)

---

### 4. Economics

**Input-Output Models:**
- Leontief input-output analysis
- $\mathbf{x} = (I - A)^{-1}\mathbf{d}$

**Markov Chains:**
- Transition matrices
- Steady-state probabilities

---

### 5. Graph Theory

**Adjacency Matrix:**
$$A_{ij} = \begin{cases}
1 & \text{if edge from } i \text{ to } j \\
0 & \text{otherwise}
\end{cases}$$

**Applications:**
- Network analysis
- PageRank algorithm
- Shortest paths

---

## Matrix Norms

### Frobenius Norm

$$\boxed{\|A\|_F = \sqrt{\sum_{i=1}^{m}\sum_{j=1}^{n} |a_{ij}|^2}}$$

**Example:**
$$A = \begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}$$

$$\|A\|_F = \sqrt{1 + 4 + 9 + 16} = \sqrt{30}$$

---

### Spectral Norm (2-Norm)

$$\boxed{\|A\|_2 = \sigma_{\max}(A)}$$

Where $\sigma_{\max}$ is the largest singular value.

---

### Infinity Norm

$$\boxed{\|A\|_\infty = \max_{1 \leq i \leq m} \sum_{j=1}^{n} |a_{ij}|}$$

Maximum absolute row sum.

---

## Important Identities

### Matrix Multiplication

$$\boxed{(AB)^T = B^TA^T}$$
$$\boxed{(AB)^{-1} = B^{-1}A^{-1}}$$
$$\boxed{(ABC)^{-1} = C^{-1}B^{-1}A^{-1}}$$

---

### Determinants

$$\boxed{\det(AB) = \det(A)\det(B)}$$
$$\boxed{\det(A^T) = \det(A)}$$
$$\boxed{\det(A^{-1}) = \frac{1}{\det(A)}}$$
$$\boxed{\det(kA) = k^n\det(A)} \quad (n \times n \text{ matrix})$$

---

### Trace

$$\boxed{\text{tr}(A + B) = \text{tr}(A) + \text{tr}(B)}$$
$$\boxed{\text{tr}(kA) = k \cdot \text{tr}(A)}$$
$$\boxed{\text{tr}(AB) = \text{tr}(BA)}$$

---

## Computational Considerations

### Numerical Stability

1. **Avoid direct inversion:** Use LU or QR decomposition
2. **Condition number:** $\kappa(A) = \|A\| \cdot \|A^{-1}\|$
   - Large condition number → ill-conditioned (numerical instability)
3. **Pivoting:** Use partial/full pivoting in Gaussian elimination

---

### Complexity

| Operation | Complexity |
|-----------|-----------|
| Addition | $O(mn)$ |
| Multiplication | $O(n^3)$ (naive), $O(n^{2.807})$ (Strassen) |
| Determinant | $O(n^3)$ |
| Inverse | $O(n^3)$ |
| Eigenvalues | $O(n^3)$ |

---

### Sparse Matrices

Matrices with mostly zeros can be stored efficiently:
- **Compressed Sparse Row (CSR)**
- **Compressed Sparse Column (CSC)**
- Used in large-scale scientific computing

---

## Quick Reference

### Common Matrices

| Type | Definition | Example |
|------|------------|---------|
| Identity | $I$, diagonal of 1s | $\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$ |
| Zero | All elements 0 | $\begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}$ |
| Diagonal | Non-zero only on diagonal | $\begin{bmatrix} a & 0 \\ 0 & b \end{bmatrix}$ |
| Symmetric | $A = A^T$ | $\begin{bmatrix} a & b \\ b & c \end{bmatrix}$ |

---

### Key Formulas

| Concept | Formula |
|---------|---------|
| 2×2 Determinant | $ad - bc$ |
| 2×2 Inverse | $\frac{1}{\det(A)}\begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$ |
| Eigenvalues | $\det(A - \lambda I) = 0$ |
| Trace | $\sum a_{ii}$ |
| Rank | Max linearly independent rows/columns |

---

## See Also
- [[00 - Algebra MOC]] - Algebra topics overview
- [[Complex Numbers]] - Matrix eigenvalues can be complex
- [[00 - Math MOC]] - Mathematics overview
