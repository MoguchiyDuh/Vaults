---
tags:
  - math/algebra
  - calculus
  - limits
related:
  - '[[Algebra MOC]]'
status: stub
---
# Limits

## Definition
A **limit** describes the value that a function approaches as the input approaches some value.

### $$\boxed{\lim_{x \to a} f(x) = L}$$

Means: "As $x$ gets arbitrarily close to $a$, $f(x)$ gets arbitrarily close to $L$."

---

## Basic Limit Laws

### Sum/Difference
### $$\boxed{\lim_{x \to a} [f(x) \pm g(x)] = \lim_{x \to a} f(x) \pm \lim_{x \to a} g(x)}$$

### Product
### $$\boxed{\lim_{x \to a} [f(x) \cdot g(x)] = \lim_{x \to a} f(x) \cdot \lim_{x \to a} g(x)}$$

### Quotient
### $$\boxed{\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{\lim_{x \to a} f(x)}{\lim_{x \to a} g(x)}, \quad \text{if } \lim_{x \to a} g(x) \neq 0}$$

### Constant Multiple
### $$\boxed{\lim_{x \to a} [c \cdot f(x)] = c \cdot \lim_{x \to a} f(x)}$$

### Power
### $$\boxed{\lim_{x \to a} [f(x)]^n = \left[\lim_{x \to a} f(x)\right]^n}$$

---

## Common Limits

### Polynomial
For any polynomial $p(x)$:
### $$\boxed{\lim_{x \to a} p(x) = p(a)}$$

### Constant
### $$\boxed{\lim_{x \to a} c = c}$$

### Identity
### $$\boxed{\lim_{x \to a} x = a}$$

---

## Indeterminate Forms

Common indeterminate forms that require special techniques:
- $\frac{0}{0}$
- $\frac{\infty}{\infty}$
- $0 \cdot \infty$
- $\infty - \infty$
- $0^0$, $1^\infty$, $\infty^0$

---

## Techniques for Evaluating Limits

### 1. Direct Substitution
Try substituting the value directly into the function.

**Example:**
$$\lim_{x \to 2} (x^2 + 3x) = 2^2 + 3(2) = 10$$

### 2. Factoring
Factor and cancel common terms.

**Example:**
$$\lim_{x \to 3} \frac{x^2 - 9}{x - 3} = \lim_{x \to 3} \frac{(x-3)(x+3)}{x-3} = \lim_{x \to 3} (x+3) = 6$$

### 3. Rationalization
Multiply by conjugate to eliminate radicals.

**Example:**
$$\lim_{x \to 0} \frac{\sqrt{x+1} - 1}{x}$$

### 4. L'Hôpital's Rule
For $\frac{0}{0}$ or $\frac{\infty}{\infty}$ forms:
### $$\boxed{\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}}$$

---

## One-Sided Limits

### Left-Hand Limit
### $$\boxed{\lim_{x \to a^-} f(x)}$$
Approaches $a$ from values less than $a$.

### Right-Hand Limit
### $$\boxed{\lim_{x \to a^+} f(x)}$$
Approaches $a$ from values greater than $a$.

**A limit exists if and only if:**
### $$\boxed{\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x)}$$

---

## Limits at Infinity

### $$\boxed{\lim_{x \to \infty} f(x), \quad \lim_{x \to -\infty} f(x)}$$

**Common limits:**
- $\lim_{x \to \infty} \frac{1}{x} = 0$
- $\lim_{x \to \infty} \frac{1}{x^n} = 0$ (for $n > 0$)
- $\lim_{x \to \infty} e^x = \infty$
- $\lim_{x \to -\infty} e^x = 0$

---

## Special Limits

### $$\boxed{\lim_{x \to 0} \frac{\sin x}{x} = 1}$$

### $$\boxed{\lim_{x \to \infty} \left(1 + \frac{1}{x}\right)^x = e}$$

### $$\boxed{\lim_{x \to 0} \frac{e^x - 1}{x} = 1}$$

---

## Continuity
A function $f(x)$ is **continuous** at $x = a$ if:
### $$\boxed{\lim_{x \to a} f(x) = f(a)}$$

This requires:
1. $f(a)$ is defined
2. $\lim_{x \to a} f(x)$ exists
3. The limit equals the function value

---

## See Also
- [[Algebra MOC]] - Algebra topics overview
