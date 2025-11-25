---
tags:
  - math/algebra
  - matrices
  - linear-algebra
related:
  - "[[Vectors]]"
  - "[[00 - Algebra MOC]]"
  - "[[00 - Math MOC]]"
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

## Types of Matrices

### Identity Matrix
A square matrix with 1s on the main diagonal and 0s elsewhere:
$
\boxed{I_n = \begin{bmatrix}
1 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 1
\end{bmatrix}}
$
**Property:** $A \cdot I = I \cdot A = A$ for any matrix $A$.

### Zero Matrix
A matrix with all elements equal to zero:
$
\boxed{O = \begin{bmatrix}
0 & 0 & \dots & 0 \\
0 & 0 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 0
\end{bmatrix}}
$

### Diagonal Matrix
A square matrix where all non-diagonal elements are zero:
$
\boxed{D = \begin{bmatrix}
d_1 & 0 & \dots & 0 \\
0 & d_2 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & d_n
\end{bmatrix}}
$

### Triangular Matrices

**Upper Triangular:** All elements below the main diagonal are zero.
$
\boxed{U = \begin{bmatrix}
u_{11} & u_{12} & u_{13} \\
0 & u_{22} & u_{23} \\
0 & 0 & u_{33}
\end{bmatrix}}
$

**Lower Triangular:** All elements above the main diagonal are zero.
$
\boxed{L = \begin{bmatrix}
l_{11} & 0 & 0 \\
l_{21} & l_{22} & 0 \\
l_{31} & l_{32} & l_{33}
\end{bmatrix}}
$

### Orthogonal Matrix
A square matrix $Q$ where $Q^T Q = Q Q^T = I$:
$
\boxed{Q^T = Q^{-1}}
$
**Property:** Preserves lengths and angles (rigid transformations).

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
$
\boxed{A \cdot A^{-1} = I}
$

**For 2×2 matrices:**
$
\boxed{A^{-1} = \frac{1}{\text{det}(A)} \begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}}
$
where $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$ and $\text{det}(A) = ad - bc \neq 0$.

### Trace of a Matrix
The trace is the sum of diagonal elements of a square matrix:
$
\boxed{\text{tr}(A) = \sum_{i=1}^{n} a_{ii}}
$

**Properties:**
- $\text{tr}(A + B) = \text{tr}(A) + \text{tr}(B)$
- $\text{tr}(kA) = k \cdot \text{tr}(A)$
- $\text{tr}(AB) = \text{tr}(BA)$

### Matrix Rank
The rank of a matrix is the maximum number of linearly independent rows (or columns):
$
\boxed{\text{rank}(A) \leq \min(m, n)}
$

**Full rank:** A matrix has full rank if $\text{rank}(A) = \min(m, n)$.

### Positive Definite Matrix
A symmetric matrix $A$ is positive definite if:
$
\boxed{x^T A x > 0 \text{ for all non-zero vectors } x}
$

---

## Matrix Decompositions

### LU Decomposition
Any square matrix $A$ can be decomposed into:
$
\boxed{A = LU}
$
where $L$ is lower triangular and $U$ is upper triangular.

**Use:** Efficiently solving systems of linear equations.

### Eigenvalue Decomposition
For a square matrix $A$:
$
\boxed{A = Q \Lambda Q^{-1}}
$
where $\Lambda$ is a diagonal matrix of eigenvalues and $Q$ contains eigenvectors.

### Singular Value Decomposition (SVD)
Any $m \times n$ matrix $A$ can be decomposed as:
$
\boxed{A = U \Sigma V^T}
$
where:
- $U$: $m \times m$ orthogonal matrix
- $\Sigma$: $m \times n$ diagonal matrix (singular values)
- $V$: $n \times n$ orthogonal matrix

---

## Eigenvalues and Eigenvectors

### Definition
For a square matrix $A$, if there exists a non-zero vector $\mathbf{v}$ and scalar $\lambda$ such that:
$
\boxed{A\mathbf{v} = \lambda\mathbf{v}}
$
Then:
- $\lambda$ is an **eigenvalue**
- $\mathbf{v}$ is an **eigenvector**

### Characteristic Equation
Eigenvalues are found by solving:
$
\boxed{\text{det}(A - \lambda I) = 0}
$

**Example for 2×2 matrix:**
$
A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$
$
\text{det}(A - \lambda I) = (a-\lambda)(d-\lambda) - bc = 0
$
$
\lambda^2 - (a+d)\lambda + (ad-bc) = 0
$

### Properties of Eigenvalues
$
\boxed{\sum_{i=1}^{n} \lambda_i = \text{tr}(A)}
$
$
\boxed{\prod_{i=1}^{n} \lambda_i = \text{det}(A)}
$

---

## Row Operations and Row Echelon Form

### Elementary Row Operations
1. **Row swap:** $R_i \leftrightarrow R_j$
2. **Row multiplication:** $kR_i \to R_i$ (where $k \neq 0$)
3. **Row addition:** $R_i + kR_j \to R_i$

### Row Echelon Form (REF)
A matrix is in REF if:
1. All zero rows are at the bottom
2. The leading entry (pivot) of each row is to the right of the leading entry of the row above
3. All entries below a pivot are zero

**Example:**
$
\begin{bmatrix}
1 & 2 & 3 \\
0 & 1 & 4 \\
0 & 0 & 1
\end{bmatrix}
$

### Reduced Row Echelon Form (RREF)
Additional conditions:
1. All pivots are 1
2. Each pivot is the only non-zero entry in its column

**Example:**
$
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$

---

## Advanced Properties

### Matrix Norms

**Frobenius Norm:**
$
\boxed{\|A\|_F = \sqrt{\sum_{i=1}^{m} \sum_{j=1}^{n} |a_{ij}|^2}}
$

**Spectral Norm:**
$
\boxed{\|A\|_2 = \sigma_{\text{max}}(A)}
$
where $\sigma_{\text{max}}$ is the largest singular value.

### Important Matrix Identities
$
\boxed{(AB)^T = B^T A^T}
$
$
\boxed{(AB)^{-1} = B^{-1} A^{-1}}
$
$
\boxed{\text{det}(AB) = \text{det}(A) \cdot \text{det}(B)}
$
$
\boxed{\text{det}(A^T) = \text{det}(A)}
$
$
\boxed{\text{det}(A^{-1}) = \frac{1}{\text{det}(A)}}
$
$
\boxed{\text{det}(kA) = k^n \text{det}(A) \text{ for } n \times n \text{ matrix}}
$

### Cayley-Hamilton Theorem
Every square matrix satisfies its own characteristic equation:
$
\boxed{p(A) = 0}
$
where $p(\lambda) = \text{det}(A - \lambda I)$ is the characteristic polynomial.

---

## Applications of Matrices

### Systems of Linear Equations
Matrices are used to represent and solve systems of linear equations:
$
\boxed{A\mathbf{x} = \mathbf{b}}
$
$
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
$

**Solution methods:**
1. **Matrix inverse:** $\mathbf{x} = A^{-1}\mathbf{b}$ (if $A$ is invertible)
2. **Gaussian elimination:** Row reduce augmented matrix $[A|\mathbf{b}]$
3. **Cramer's rule:** Use determinants (see below)

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

### Linear Transformations
Matrices represent linear transformations in vector spaces. For transformation $T: \mathbb{R}^n \to \mathbb{R}^m$:
$
\boxed{T(\mathbf{x}) = A\mathbf{x}}
$

**Common 2D transformations:**

**Rotation by angle $\theta$:**
$
R(\theta) = \begin{bmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta
\end{bmatrix}
$

**Scaling by factors $s_x, s_y$:**
$
S = \begin{bmatrix}
s_x & 0 \\
0 & s_y
\end{bmatrix}
$

**Reflection across x-axis:**
$
\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
$

**Shear transformation:**
$
\begin{bmatrix}
1 & k \\
0 & 1
\end{bmatrix}
$

### Computer Graphics
Matrices are fundamental in 3D graphics for:
- **Model transformations:** Position, rotate, scale objects
- **View transformations:** Camera positioning
- **Projection matrices:** 3D to 2D screen mapping
- **Homogeneous coordinates:** $4 \times 4$ matrices for translation

### Data Science & Machine Learning
- **Principal Component Analysis (PCA):** Uses eigenvalue decomposition
- **Dimensionality reduction:** SVD
- **Neural networks:** Weight matrices
- **Recommendation systems:** Matrix factorization
- **Image processing:** Convolution as matrix multiplication

### Physics & Engineering
- **Quantum mechanics:** Operators as matrices, state vectors
- **Structural analysis:** Stiffness matrices
- **Electrical circuits:** Impedance matrices
- **Mechanics:** Moment of inertia tensors

### Graph Theory
The adjacency matrix represents connections in a graph:
$
A_{ij} = \begin{cases}
1 & \text{if edge exists between vertices } i, j \\
0 & \text{otherwise}
\end{cases}
$

**Applications:**
- Network analysis
- Social networks
- Web page ranking (Google's PageRank)

### Markov Chains
Transition matrices describe probability of state changes:
$
\boxed{P = \begin{bmatrix}
p_{11} & p_{12} & \cdots \\
p_{21} & p_{22} & \cdots \\
\vdots & \vdots & \ddots
\end{bmatrix}}
$
where $p_{ij}$ is the probability of transitioning from state $i$ to state $j$.

---

## Computational Considerations

### Matrix Multiplication Complexity
Standard algorithm: $O(n^3)$ for $n \times n$ matrices  
Strassen's algorithm: $O(n^{2.807})$

### Numerical Stability
- Avoid computing $A^{-1}$ directly; use LU decomposition instead
- Use QR decomposition for orthogonalization
- SVD for robust solutions to ill-conditioned systems

### Sparse Matrices
Matrices with mostly zero elements can be stored efficiently:
- **Compressed Sparse Row (CSR)** format
- **Compressed Sparse Column (CSC)** format
- Used in large-scale scientific computing

---

## See Also
- [[Vectors]] - Vector operations (related to matrix operations)
- [[00 - Algebra MOC]] - Algebra topics overview
- [[00 - Math MOC]] - Mathematics overview
