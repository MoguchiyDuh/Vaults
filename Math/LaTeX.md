### Inline(\$): $E = mc^2$
### Multi line(\$\$):
$$
\int_a^b f(x) \, dx = F(b) - F(a)
$$
---
### Font Styles
$\textbf{Bold Font}$
$\textit{Italic}$
$\underline{Underline}$
$\vec{a}$
$\cancel{5}$
$\boxed{\pi=\frac c d}$
---
### Font Sizes
$\tiny{This\ is\ tiny\ text}$
$\scriptsize{This\ is\ scriptsize}$
$\footnotesize{This\ is\ footnotesize}$
$\small{This\ is\ small\ text}$
$\normalsize{This\ is\ normal\ text}$
$\large{This\ is\ large\ text}$
$\Large{This\ is\ Large\ text}$
$\LARGE{This\ is\ LARGE\ text}$
$\huge{This\ is\ huge\ text}$
$\Huge{This\ is\ Huge\ text}$
---
### Font Families
$\texttt{typewriter (monospace) Sample Text 0123}$
$\textrm{serif (roman) Sample Text 0123}$
$\textsf{sans serif Sample Text 0123}$
---
### Letters and Styles
- **Greek:** $\alpha, \beta, \Gamma, \gamma, \Delta, \delta, \epsilon, \zeta, \eta, \Theta, \theta, \iota, \kappa, \lambda, \mu, \nu, \Xi, \xi, \omicron, \Pi, \pi, \rho, \Sigma, \sigma, \upsilon, \chi, \Psi, \psi, \omega$
- **Blackboard Bold Font:** $\mathbb{N} - natural (0,1,2,3), \mathbb{R} - real, \mathbb{C} - complex, \mathbb{Z} - integers$
- **Calligraphic Font:** $\mathcal{A}, \mathcal{B}, \mathcal{C}, \mathcal{O} (big O)$
- **Boldface:** $\mathbf{A}, \boldsymbol{\alpha}$
---
### Operators
- **Simple Operations:** $\sum, \int, \sqrt{x}, \sqrt[3]{x}, \frac{a}{b}$
- **Brackets** $\left( \frac{a}{b} \right), \left[ \frac{a}{b} \right], \left\{ \frac{a}{b} \right\}$
- **Spec Symbols:** $\infty, \emptyset, \varnothing, \forall, \exists, \nexists, \subset, \supset, \in, \notin, \cap, \cup, \parallel, \perp$ 
- **Logic:** $\not=, =, \equiv, \approx, \pm, \gt, \lt, \ge, \le, \ngtr, \nless, \ngeq, \nleq, \land, \lor, \lnot, \to, \gets, \leftrightarrow, \leftrightarrows, \implies, \impliedby, \uparrow, \downarrow, \times, \cdot$
- **Functions:** $\sin, \cos, \tan, \cot, \arcsin, \arccos, \arctan, \log, \lg, \ln, \det, \min, \max, \lim, \exp, \deg, x \mod a$
- **Punctuation:** $\checkmark, \angle, \degree, \triangle, \square$
- space - \quad
---
### Subscript and Superscript: $a_1^2 + b_1^2 = c_1^2$

---
### \Begin block
$$
f(x) = \begin{cases}
x^2 & \text{if } x \geq 0 \\
-x & \text{if } x < 0
\end{cases}
$$

$$
\begin{matrix}
a & b \\
c & d 
\end{matrix}
$$


$$
\begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}
\quad
\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}
\quad
\begin{vmatrix} 1 & 2 \\ 3 & 4 \end{vmatrix}
$$

$$
\begin{array}{c|c|c}
x & f(x) & f'(x) \\
\hline
0 & 1 & 0 \\
1 & 2 & 2 \\
2 & 4 & 4 \\
\end{array}
$$

$$
\begin{gather}
a^2 + b^2 = c^2 \\
e^{i\pi} + 1 = 0 \\
F = ma
\end{gather}
$$

$$
\begin{multline}
( a + b + c + d + e + f + g + h + i + j + k + l + m + n + o + p + q + r + s + t + u + v + w + x + y + z )^2 \\
= \text{very long expansion...}
\end{multline}
$$

<p style="text-align: center">aligned to "&"</p>

$$
\begin{align}
f(x) &= x^2 + 2x + 1 \\
g(x) &= 3x^3 - 4x^2 + 5x - 2 \\
h(x) &= \sin(x) + \cos(x)
\end{align}
$$

$$
\begin{equation}
E = mc^2
\end{equation}
$$

$$
\left(
\begin{array}{cc|c}
1 & 2 & 3 \\
4 & 5 & 6 \\
\hline
7 & 8 & 9
\end{array}
\right)
$$


---
### Examples:
1. $\int_0^\infty e^{-x^2} dx$
<br>
2. $\sum_{i=1}^n i^2$
<br>
3. $\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}$
<br>
4. $\begin{vmatrix}
   a & b \\
   c & d
\end{vmatrix}$
<br>
5. $\begin{align*}
    x + y &= 5 \\
    2x - y &= 1 \\
    x - 3y &= -4
\end{align*}$
<br>
6. $\begin{equation}
\begin{cases}
    x + y = 5 \\
    2x - y = 1 \\
    x - 3y = -4
\end{cases}
\end{equation}$
<br>
7. $\begin{equation}
\left[
\begin{array}{c}
    x + y = 5 \\
    2x - y = 1 \\
    x - 3y = -4
\end{array}
\right.
\end{equation}$
<br>
8. $\begin{gather*} 
2x - 5y =  8 \\ 
3x^2 + 9y =  3a + c
\end{gather*}$
<br>
9. $\lim_{h \to 0 } \frac{f(x+h)-f(x)}{h}$