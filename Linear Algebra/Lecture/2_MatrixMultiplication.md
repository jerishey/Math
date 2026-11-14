## `1. Matrix Multiplication`

A **matrix** is a rectangular grid of numbers arranged in rows (horizontal) and columns (vertical). A matrix with $m$ rows and $n$ columns has size $m \times n$ (read "m by n").

Multiplying matrices is **not** done entry by entry. It uses a "row times column" method.

### `1.1 Dimensions and compatibility (can I multiply these?)`

Before multiplying, check the sizes. To compute $AB$:

> The number of **columns in $A$** must equal the number of **rows in $B$**.

If $A$ is $m \times n$ and $B$ is $n \times p$, then:

- the product $AB$ **exists**, and
- the result has size $m \times p$ (the "outer" numbers).

$$
\underbrace{A}_{m \times n} \cdot \underbrace{B}_{n \times p} = \underbrace{AB}_{m \times p}
$$

**Memory trick:** write the sizes side by side, like $(2 \times \mathbf{3})(\mathbf{3} \times 4)$. If the two inner numbers match, you can multiply. The outer numbers give the answer's size: $2 \times 4$.

| Size of $A$ | Size of $B$ | Can we compute $AB$? | Size of $AB$ |
|-------------|-------------|----------------------|--------------|
| $2 \times 3$ | $3 \times 4$ | Yes (3 = 3) | $2 \times 4$ |
| $3 \times 3$ | $3 \times 1$ | Yes (3 = 3) | $3 \times 1$ |
| $1 \times 4$ | $4 \times 1$ | Yes (4 = 4) | $1 \times 1$ |
| $2 \times 3$ | $2 \times 3$ | No (3 ≠ 2) | n/a |

### `1.2 Row-by-column multiplication (how it works)`

Each entry of the answer is built from **one row of $A$** and **one column of $B$**:

1. Pick a row from $A$ and a column from $B$.
2. Multiply the first numbers together, the second numbers together, and so on.
3. Add up all those products.

The result goes in the answer at that row's position and that column's position. In symbols, the entry in row $i$, column $j$ of $AB$ is:

$$
(AB)_{ij} = a_{i1}b_{1j} + a_{i2}b_{2j} + \dots + a_{in}b_{nj}
$$

This is called a **dot product** of the row and the column.

### `1.3 Multiplying two matrices: step-by-step example`

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}, \qquad
B = \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix}
$$

Both are $2 \times 2$, so $AB$ exists and is $2 \times 2$. We need four entries:

| Entry | Row of $A$ | Column of $B$ | Calculation | Result |
|-------|-----------|---------------|-------------|--------|
| Top-left | $[1, 2]$ | $[5, 7]$ | $1 \cdot 5 + 2 \cdot 7 = 5 + 14$ | **19** |
| Top-right | $[1, 2]$ | $[6, 8]$ | $1 \cdot 6 + 2 \cdot 8 = 6 + 16$ | **22** |
| Bottom-left | $[3, 4]$ | $[5, 7]$ | $3 \cdot 5 + 4 \cdot 7 = 15 + 28$ | **43** |
| Bottom-right | $[3, 4]$ | $[6, 8]$ | $3 \cdot 6 + 4 \cdot 8 = 18 + 32$ | **50** |

$$
AB = \begin{bmatrix} 19 & 22 \\ 43 & 50 \end{bmatrix}
$$

### `1.4 A non-square example`

$$
A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}_{2\times3}, \qquad
B = \begin{bmatrix} 1 \\ 0 \\ 2 \end{bmatrix}_{3\times1}
$$

The inner sizes match (3 and 3), so $AB$ is $2 \times 1$:

$$
AB = \begin{bmatrix} 1\cdot1 + 2\cdot0 + 3\cdot2 \\ 4\cdot1 + 5\cdot0 + 6\cdot2 \end{bmatrix}
= \begin{bmatrix} 7 \\ 16 \end{bmatrix}
$$

---

## `2. Properties of Matrix Multiplication`

Matrix multiplication follows some familiar rules from ordinary numbers, but **not all of them**. (Assume the sizes are always compatible.)

| Property | Rule | True? |
|----------|------|-------|
| Associative | $A(BC) = (AB)C$ | Always |
| Distributive | $A(B+C) = AB + AC$ | Always |
| Commutative | $AB = BA$ | **Usually false** |

### 2.1 Associative property: $A(BC) = (AB)C$

When multiplying three matrices, it doesn't matter which pair you multiply first, as long as you keep the **order** of the matrices the same. That is why we can write $ABC$ without brackets.

This is like $(2 \cdot 3) \cdot 4 = 2 \cdot (3 \cdot 4)$ for ordinary numbers.

### 2.2 Distributive property: $A(B+C) = AB + AC$

Multiplication spreads over addition. Let's check with an example:

$$
A = \begin{bmatrix} 1 & 2 \\ 0 & 1 \end{bmatrix}, \quad
B = \begin{bmatrix} 1 & 0 \\ 2 & 1 \end{bmatrix}, \quad
C = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}
$$

**Left side:** first add, then multiply.

$$
B + C = \begin{bmatrix} 1 & 1 \\ 3 & 1 \end{bmatrix}, \qquad
A(B+C) = \begin{bmatrix} 7 & 3 \\ 3 & 1 \end{bmatrix}
$$

**Right side:** multiply separately, then add.

$$
AB = \begin{bmatrix} 5 & 2 \\ 2 & 1 \end{bmatrix}, \quad
AC = \begin{bmatrix} 2 & 1 \\ 1 & 0 \end{bmatrix}, \quad
AB + AC = \begin{bmatrix} 7 & 3 \\ 3 & 1 \end{bmatrix}
$$

Both sides match. (The version $(A+B)C = AC + BC$ also holds.)

### 2.3 Non-commutative property: $AB \neq BA$ in general

With ordinary numbers, $3 \times 5 = 5 \times 3$. With matrices, **order matters**.

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}, \qquad
B = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}
$$

$$
AB = \begin{bmatrix} 2 & 1 \\ 4 & 3 \end{bmatrix}, \qquad
BA = \begin{bmatrix} 3 & 4 \\ 1 & 2 \end{bmatrix}
$$

Since $AB \neq BA$, we say these matrices **do not commute**.

**Things to remember:**

- Sometimes $AB$ exists but $BA$ doesn't (try a $2 \times 3$ times a $3 \times 4$).
- "In general" means it is usually false, but a few special pairs do commute (for example, any matrix with the identity matrix, see next section).
- This is why we say "multiply $A$ **on the left** by $B$" or "**on the right**": the side matters.

---

## `3. Identity Matrix`

The **identity matrix**, written $I$ (or $I_n$ for size $n \times n$), is a square matrix with **1s on the main diagonal** (top-left to bottom-right) and **0s everywhere else**:

$$
I_2 = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}, \qquad
I_3 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}
$$

### 3.1 Why it matters: $AI = IA = A$

The identity matrix is the matrix version of the number **1**. Multiplying a number by 1 leaves it unchanged, and multiplying a matrix by $I$ leaves it unchanged:

$$
AI = IA = A
$$

Example:

$$
\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}
\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}
= \begin{bmatrix} 1\cdot1+2\cdot0 & 1\cdot0+2\cdot1 \\ 3\cdot1+4\cdot0 & 3\cdot0+4\cdot1 \end{bmatrix}
= \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}
$$

The matrix came out unchanged. This is one of the few cases where order doesn't matter: $AI$ and $IA$ give the same result.

---

## `4. Inverse Matrix`

### `4.1 The idea`

With numbers, the **inverse** (reciprocal) of 5 is $\frac{1}{5}$, because $5 \cdot \frac15 = 1$. It "undoes" multiplication by 5.

Matrices have something similar. The **inverse** of a matrix $A$ is the matrix that "undoes" $A$, giving the identity matrix.

### `4.2 Definition and notation`

The inverse of $A$ is written $A^{-1}$ ("A inverse") and satisfies:

$$
AA^{-1} = A^{-1}A = I
$$

**Important points:**

- $A^{-1}$ does **not** mean $\frac{1}{A}$. Dividing by a matrix isn't defined; $A^{-1}$ is just the name for the inverse.
- Only **square matrices** ($n \times n$) can have an inverse.
- Not every square matrix has an inverse (see Section 6).
- If an inverse exists, it is **unique** (there is only one).

### `4.3 Example`

$$
A = \begin{bmatrix} 2 & 1 \\ 5 & 3 \end{bmatrix}, \qquad
A^{-1} = \begin{bmatrix} 3 & -1 \\ -5 & 2 \end{bmatrix}
$$

Check by multiplying:

$$
AA^{-1} =
\begin{bmatrix} 2\cdot3 + 1\cdot(-5) & 2\cdot(-1) + 1\cdot2 \\ 5\cdot3 + 3\cdot(-5) & 5\cdot(-1) + 3\cdot2 \end{bmatrix}
= \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} = I \checkmark
$$

### `4.4 Useful facts`

- $(A^{-1})^{-1} = A$ (undoing the undo gives the original)
- $(AB)^{-1} = B^{-1}A^{-1}$ (the order **reverses**, like taking off socks and shoes)

### 4.5 Shortcut for $2 \times 2$ matrices

$$
A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}
\quad\Longrightarrow\quad
A^{-1} = \frac{1}{ad - bc}\begin{bmatrix} d & -b \\ -c & a \end{bmatrix}
$$

Swap $a$ and $d$, flip the signs of $b$ and $c$, then divide everything by $ad - bc$. This only works if $ad - bc \neq 0$. The number $ad - bc$ is called the **determinant**.

For our example: $ad - bc = 2\cdot3 - 1\cdot5 = 1$, so $A^{-1} = \begin{bmatrix} 3 & -1 \\ -5 & 2 \end{bmatrix}$, matching the above.

---

## `5. Finding the Inverse with Gauss-Jordan Elimination`

The $2 \times 2$ shortcut doesn't scale to bigger matrices. **Gauss-Jordan elimination** works for any size.

### `5.1 The big idea`

1. Write $A$ and the identity matrix $I$ side by side. This is the **augmented matrix** $[A \mid I]$.
2. Use **row operations** to turn the **left** side into $I$.
3. Whatever the **right** side becomes is $A^{-1}$.

$$
[A \mid I] \;\xrightarrow{\text{row operations}}\; [I \mid A^{-1}]
$$

Whatever steps turn $A$ into $I$ also turn $I$ into $A^{-1}$.

### `5.2 The three allowed row operations`

| Operation | Notation | Meaning |
|-----------|----------|---------|
| Swap | $R_1 \leftrightarrow R_2$ | Exchange two rows |
| Scale | $R_1 \to 3R_1$ | Multiply a row by a **nonzero** number |
| Add | $R_2 \to R_2 - 5R_1$ | Add a multiple of one row to another row |

Each operation is applied to the **entire** row, across both halves of the augmented matrix.

### `5.3 Strategy`

Work one column at a time, from left to right:

1. Get a **1** on the diagonal (swap or scale rows to do this).
2. Use that 1 to turn all other numbers in the same column into **0** (using the "add" operation).
3. Move to the next column.

### `5.4 Worked example`

Find the inverse of

$$
A = \begin{bmatrix} 2 & 1 \\ 5 & 3 \end{bmatrix}
$$

**Start:** write $[A \mid I]$.

$$
\left[\begin{array}{cc|cc} 2 & 1 & 1 & 0 \\ 5 & 3 & 0 & 1 \end{array}\right]
$$

**Step 1: make the top-left a 1.** Divide row 1 by 2 ($R_1 \to \tfrac12 R_1$).

$$
\left[\begin{array}{cc|cc} 1 & \tfrac12 & \tfrac12 & 0 \\ 5 & 3 & 0 & 1 \end{array}\right]
$$

**Step 2: make the entry below it 0.** Subtract 5 times row 1 from row 2 ($R_2 \to R_2 - 5R_1$).

$$
\left[\begin{array}{cc|cc} 1 & \tfrac12 & \tfrac12 & 0 \\ 0 & \tfrac12 & -\tfrac52 & 1 \end{array}\right]
$$

**Step 3: make the second diagonal entry a 1.** Multiply row 2 by 2 ($R_2 \to 2R_2$).

$$
\left[\begin{array}{cc|cc} 1 & \tfrac12 & \tfrac12 & 0 \\ 0 & 1 & -5 & 2 \end{array}\right]
$$

**Step 4: make the entry above it 0.** Subtract $\tfrac12$ times row 2 from row 1 ($R_1 \to R_1 - \tfrac12R_2$).

$$
\left[\begin{array}{cc|cc} 1 & 0 & 3 & -1 \\ 0 & 1 & -5 & 2 \end{array}\right]
$$

The left side is now $I$. The right side is the inverse:

$$
A^{-1} = \begin{bmatrix} 3 & -1 \\ -5 & 2 \end{bmatrix}
$$

### `5.5 What if it fails?`

If at any point a **row of zeros** appears on the left side, you cannot reach $I$, and the matrix has **no inverse** (see Section 6).

---

## `6. Invertible and Singular Matrices`

### `6.1 Definitions`

- **Invertible matrix** (also called **non-singular**): a square matrix that **has** an inverse.
- **Singular matrix**: a square matrix that has **no** inverse.

This is similar to numbers: 5 has a reciprocal, but 0 does not (you can't compute $\frac10$).

### `6.2 Conditions for a matrix to be invertible`

For a square $n \times n$ matrix $A$, all of these statements say the same thing. If one is true, all are true:

- $A$ is invertible.
- The **determinant** is not zero: $\det(A) \neq 0$.
- Row reducing $A$ gives the identity matrix $I$.
- The rows (and columns) are **linearly independent** (no row is built from the others).
- The system $A\mathbf{x} = \mathbf{b}$ has exactly one solution for every $\mathbf{b}$.

### `6.3 Examples of matrices without inverses`

**Example 1: a row of zeros**

$$
\begin{bmatrix} 1 & 2 \\ 0 & 0 \end{bmatrix}
$$

**Example 2: one row is a multiple of another**

$$
\begin{bmatrix} 1 & 2 \\ 2 & 4 \end{bmatrix}
$$

Row 2 is 2 times row 1. The determinant is $1\cdot4 - 2\cdot2 = 0$, so it is singular.

**Example 3: Gauss-Jordan breaks down**

$$
\left[\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 2 & 4 & 0 & 1 \end{array}\right]
\xrightarrow{R_2 \to R_2 - 2R_1}
\left[\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & 0 & -2 & 1 \end{array}\right]
$$

The left side has a row of zeros and can never become $I$. No inverse exists.

**Example 4: any non-square matrix.** For example, a $2 \times 3$ matrix has no inverse, because inverses exist only for square matrices.

---