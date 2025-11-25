---
tags:
  - math/algebra
  - complex-numbers
related:
  - "[[Trigonometry Basics]]"
  - "[[Vectors]]"
  - "[[00 - Algebra MOC]]"
status: stub
---
# Complex Numbers

## Definition
A **complex number** is a number of the form:
### $$\boxed{z = a + bi}$$

Where:
- $a$ is the **real part**: $\text{Re}(z) = a$
- $b$ is the **imaginary part**: $\text{Im}(z) = b$
- $i$ is the **imaginary unit**: $i^2 = -1$

---

## Imaginary Unit
### $$\boxed{i = \sqrt{-1}, \quad i^2 = -1}$$

**Powers of $i$:**
- $i^0 = 1$
- $i^1 = i$
- $i^2 = -1$
- $i^3 = -i$
- $i^4 = 1$ (pattern repeats)

---

## Complex Plane (Argand Diagram)
Complex numbers can be represented as points or vectors in the complex plane:
- **Real axis** (horizontal): represents the real part
- **Imaginary axis** (vertical): represents the imaginary part
- Point $(a, b)$ represents $z = a + bi$

---

## Operations

### Addition
### $$\boxed{(a + bi) + (c + di) = (a + c) + (b + d)i}$$

### Subtraction
### $$\boxed{(a + bi) - (c + di) = (a - c) + (b - d)i}$$

### Multiplication
### $$\boxed{(a + bi)(c + di) = (ac - bd) + (ad + bc)i}$$

### Division
To divide complex numbers, multiply numerator and denominator by the conjugate:
### $$\boxed{\frac{a + bi}{c + di} = \frac{(a + bi)(c - di)}{(c + di)(c - di)} = \frac{(ac + bd) + (bc - ad)i}{c^2 + d^2}}$$

---

## Complex Conjugate
The complex conjugate of $z = a + bi$ is:
### $$\boxed{\bar{z} = a - bi}$$

**Properties:**
- $z \cdot \bar{z} = a^2 + b^2$ (always real and non-negative)
- $\overline{z_1 + z_2} = \bar{z_1} + \bar{z_2}$
- $\overline{z_1 \cdot z_2} = \bar{z_1} \cdot \bar{z_2}$

---

## Modulus (Absolute Value)
The modulus of $z = a + bi$ is its distance from the origin:
### $$\boxed{|z| = \sqrt{a^2 + b^2}}$$

---

## Polar Form
A complex number can be written in polar form:
### $$\boxed{z = r(\cos\theta + i\sin\theta) = r \text{cis}(\theta)}$$

Where:
- $r = |z| = \sqrt{a^2 + b^2}$ (modulus)
- $\theta = \arg(z) = \tan^{-1}\left(\frac{b}{a}\right)$ (argument/angle)

---

## Euler's Formula
### $$\boxed{e^{i\theta} = \cos\theta + i\sin\theta}$$

Therefore:
### $$\boxed{z = re^{i\theta}}$$

---

## De Moivre's Theorem
For any integer $n$:
### $$\boxed{(\cos\theta + i\sin\theta)^n = \cos(n\theta) + i\sin(n\theta)}$$

Or in exponential form:
### $$\boxed{(re^{i\theta})^n = r^n e^{in\theta}}$$

---

## See Also
- [[Trigonometry Basics]] - Euler's formula connection
- [[Vectors]] - Geometric interpretation
- [[00 - Algebra MOC]] - Algebra topics overview
