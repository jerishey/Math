## `1. Systems of linear equations`

A **system of linear equations** is a collection of equations in which every unknown appears only to the first power and is never multiplied by another unknown.

A general system of $m$ equations in $n$ unknowns looks like this:

$$
\begin{aligned}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n &= b_1 \\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n &= b_2 \\
&\ \vdots \\
a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n &= b_m
\end{aligned}
$$

A **solution** is a set of values for $x_1, \dots, x_n$ that satisfies every equation at once. A system can have:

- exactly one solution,
- no solution, or
- infinitely many solutions.

**Example** used throughout:

$$
\begin{aligned}
2x - y &= 0 \\
-x + 2y &= 3
\end{aligned}
$$

Its solution is $x = 1,\ y = 2$.

---

### `Matrix representation`

The same system can be packed into a compact form using a coefficient matrix, a vector of unknowns, and a right-hand side vector:

$$
\underbrace{\begin{bmatrix} 2 & -1 \\ -1 & 2 \end{bmatrix}}_{A}
\underbrace{\begin{bmatrix} x \\ y \end{bmatrix}}_{\mathbf{x}} =
\underbrace{\begin{bmatrix} 0 \\ 3 \end{bmatrix}}_{\mathbf{b}}
$$

This is written as

$$
A\mathbf{x} = \mathbf{b}
$$

| Symbol | Name | Size |
|--------|------|------|
| $A$ | Coefficient matrix | $m \times n$ |
| $\mathbf{x}$ | Vector of unknowns | $n \times 1$ |
| $\mathbf{b}$ | Right-hand side | $m \times 1$ |

The **augmented matrix** $[A \mid \mathbf{b}]$ is often used for elimination:

$$
\left[\begin{array}{cc|c} 2 & -1 & 0 \\ -1 & 2 & 3 \end{array}\right]
$$

---

### `Row picture`

In the **row picture**, we look at one equation at a time. Each equation describes a geometric object:

- In 2 unknowns, each equation is a **line**.
- In 3 unknowns, each equation is a **plane**.
- In $n$ unknowns, each equation is a **hyperplane**.

The solution is the point where all of these objects intersect.

For the running example:

- Row 1: $2x - y = 0$ is a line through the origin with slope 2.
- Row 2: $-x + 2y = 3$ is a line with slope $\tfrac{1}{2}$.
- The two lines cross at $(1, 2)$, which is the solution.

Check: $2(1) - 2 = 0$ and $-1 + 2(2) = 3$.

---

### `Column picture`

In the **column picture**, we look at the columns of $A$ as vectors and ask:

> Can $\mathbf{b}$ be built as a combination of the columns of $A$?

The system $A\mathbf{x} = \mathbf{b}$ is the same as

$$
x \begin{bmatrix} 2 \\ -1 \end{bmatrix} + y \begin{bmatrix} -1 \\ 2 \end{bmatrix} = \begin{bmatrix} 0 \\ 3 \end{bmatrix}
$$

The unknowns $x$ and $y$ are the **weights** of a **linear combination**. With $x = 1$ and $y = 2$:

$$
1 \begin{bmatrix} 2 \\ -1 \end{bmatrix} + 2 \begin{bmatrix} -1 \\ 2 \end{bmatrix} = \begin{bmatrix} 0 \\ 3 \end{bmatrix}
$$

Key ideas:

- The set of all combinations of the columns is the **column space** of $A$.
- $A\mathbf{x} = \mathbf{b}$ is solvable exactly when $\mathbf{b}$ lies in the column space.

---

### `Matrix picture`

The **matrix picture** treats $A$ as a function that acts on vectors:

$$
\mathbf{x} \longmapsto A\mathbf{x}
$$

Solving $A\mathbf{x} = \mathbf{b}$ means finding the input $\mathbf{x}$ that $A$ sends to $\mathbf{b}$.

- If $A$ is square and **invertible**, the solution is unique:

  $$
  \mathbf{x} = A^{-1}\mathbf{b}
  $$

- In practice, we usually solve by **Gaussian elimination** rather than computing $A^{-1}$.
- Elimination factors the matrix as $A = LU$, where $L$ is lower triangular and $U$ is upper triangular.

Elimination on the running example:

$$
\begin{bmatrix} 2 & -1 \\ -1 & 2 \end{bmatrix}
\longrightarrow
\begin{bmatrix} 2 & -1 \\ 0 & \tfrac{3}{2} \end{bmatrix}
$$

Back substitution then gives $y = 2$ and $x = 1$.

---

### `Geometry of lines and planes`

The three possible outcomes of a system have a clear geometric meaning.

**`In 2D (two equations, two unknowns)`**

| Outcome | Row picture | Column picture |
|---------|-------------|----------------|
| One solution | Lines intersect at a single point | $\mathbf{b}$ is reachable; columns are independent |
| No solution | Lines are parallel and distinct | $\mathbf{b}$ is outside the column space |
| Infinitely many solutions | Lines coincide | Columns are dependent, and $\mathbf{b}$ is on their line |

**`In 3D (three equations, three unknowns)`**

- **One solution:** three planes meet at a single point.
- **No solution:** the planes have no common point. For example, two planes are parallel, or the three planes form a "triangular prism" with no shared intersection.
- **Infinitely many solutions:** the planes meet along a common line, or all three coincide.

**`Singular vs. nonsingular`**

A square matrix $A$ is **singular** when its columns are linearly dependent, which means:

- $\det(A) = 0$
- $A$ has no inverse
- $A\mathbf{x} = \mathbf{b}$ has either no solution or infinitely many solutions

A **nonsingular** matrix has independent columns, $\det(A) \neq 0$, and gives exactly one solution for every $\mathbf{b}$.

---


## `2. Elimination and Matrix Multiplication`

### `1. Gaussian Elimination`

**Gaussian elimination** turns $A\mathbf{x} = \mathbf{b}$ into an equivalent system that is easy to solve. It works column by column: one equation (the pivot row) is used to remove an unknown from all the equations below it.

**`The algorithm`**

For each column $j = 1, 2, \dots, n-1$:

1. Find the **pivot** in position $(j, j)$. If it is zero, exchange with a lower row that has a nonzero entry in column $j$.
2. For each row $i$ below the pivot, compute the **multiplier** $\ell_{ij}$.
3. Subtract $\ell_{ij} \times$ (pivot row) from row $i$, so the entry in column $j$ becomes zero.

After the last column, the matrix is **upper triangular**. The right-hand side $\mathbf{b}$ must go through the same operations, which gives $\mathbf{c}$. Then **back substitution** finds $\mathbf{x}$.

**`Example`**

Start with the augmented matrix $[A \mid \mathbf{b}]$:

$$
\left[\begin{array}{ccc|c} 1 & 2 & 1 & 2 \\ 3 & 8 & 1 & 12 \\ 0 & 4 & 1 & 2 \end{array}\right]
$$

**Step 1** (column 1): row 2 $\leftarrow$ row 2 $-\ 3 \times$ row 1.

$$
\left[\begin{array}{ccc|c} 1 & 2 & 1 & 2 \\ 0 & 2 & -2 & 6 \\ 0 & 4 & 1 & 2 \end{array}\right]
$$

**Step 2** (column 2): row 3 $\leftarrow$ row 3 $-\ 2 \times$ row 2.

$$
\left[\begin{array}{ccc|c} 1 & 2 & 1 & 2 \\ 0 & 2 & -2 & 6 \\ 0 & 0 & 5 & -10 \end{array}\right]
$$

The system is now triangular and ready for back substitution.

**`Cost`**

For an $n \times n$ system, elimination takes roughly $n^3/3$ multiplications, while back substitution takes only about $n^2/2$. Elimination is the expensive part, which is why it is worth saving its work (see $A = LU$ in section 12).

---

### `2. Row Operations`

Elimination uses only operations that do **not** change the solution set:

| Operation | Description | Used for |
|-----------|-------------|----------|
| Replacement | Subtract a multiple of one row from another row | Creating zeros (the main step) |
| Exchange | Swap two rows | Fixing a zero pivot |
| Scaling | Multiply a row by a nonzero number | Making pivots equal to 1 (optional) |

Why the solution is preserved: each operation is reversible. Subtracting $3 \times$ row 1 from row 2 can be undone by adding it back, so any $(x, y, z)$ that solves the old system solves the new one and vice versa.

Operations that are **not** allowed: multiplying a row by zero (it destroys information and cannot be undone), or changing a row without applying the same operation to the right-hand side $\mathbf{b}$.

---

### `3. Pivot Elements`

A **pivot** is the first nonzero entry in a row at the moment that row is used to eliminate the entries below it.

In the running example:

- Pivot 1 is $1$ (row 1, column 1).
- Pivot 2 is $2$ (row 2, column 2, after step 1).
- Pivot 3 is $5$ (row 3, column 3, after step 2).

Pivots are found **during** elimination, not read from $A$ directly. Notice that the original $(2,2)$ entry of $A$ was $8$, but the pivot is $2$.

**`When elimination breaks down`**

**Temporary failure (fixable).** A zero lands in a pivot position, but a lower row has a nonzero entry. Exchange rows and continue:

$$
\begin{bmatrix} 0 & 2 \\ 3 & 4 \end{bmatrix}
\xrightarrow{\text{swap rows}}
\begin{bmatrix} 3 & 4 \\ 0 & 2 \end{bmatrix}
$$

The matrix is still nonsingular, with pivots $3$ and $2$.

**Permanent failure (singular).** No row below has a nonzero entry to use:

$$
\begin{bmatrix} 1 & 2 \\ 2 & 4 \end{bmatrix}
\xrightarrow{\text{row 2} - 2\,\text{row 1}}
\begin{bmatrix} 1 & 2 \\ 0 & 0 \end{bmatrix}
$$

There is no second pivot. The matrix is **singular**, so $A\mathbf{x} = \mathbf{b}$ has either no solution or infinitely many, depending on $\mathbf{b}$.

**`Facts about pivots`**

- An $n \times n$ matrix is nonsingular exactly when elimination gives $n$ nonzero pivots.
- If no row exchanges were used, $\det(A)$ is the product of the pivots. For the example, $1 \cdot 2 \cdot 5 = 10$.
- In numerical work, **partial pivoting** picks the largest available entry in the column as the pivot, even if the current one is nonzero but tiny. This keeps rounding errors small.

---

### `4. Elimination Multipliers`

The **multiplier** $\ell_{ij}$ says how many copies of row $j$ to subtract from row $i$:

$$
\ell_{ij} = \frac{\text{entry to eliminate in row } i,\ \text{column } j}{\text{pivot in row } j}
$$

For the running example:

| Multiplier | Calculation | Meaning |
|------------|-------------|---------|
| $\ell_{21}$ | $3 / 1 = 3$ | Subtract $3 \times$ row 1 from row 2 |
| $\ell_{31}$ | $0 / 1 = 0$ | Row 3 already has a zero, nothing to do |
| $\ell_{32}$ | $4 / 2 = 2$ | Subtract $2 \times$ row 2 from row 3 |

Notes:

- The multiplier uses the **pivot** in the denominator, so it can only be computed when the pivot is nonzero.
- Multipliers are not wasted: they are stored as the entries of $L$ in $A = LU$.
- Subscript convention: $\ell_{ij}$ goes with the entry in row $i$, column $j$ that it eliminates.

---

### `5. Upper Triangular Matrices (U)`

An **upper triangular** matrix has zeros below the diagonal. Elimination produces one:

$$
U = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 2 & -2 \\ 0 & 0 & 5 \end{bmatrix}
$$

Properties:

- The **pivots** $1, 2, 5$ are on the diagonal.
- A triangular system is easy to solve from the bottom up (back substitution).
- $\det(U)$ is the product of the diagonal entries. Row replacement does not change the determinant, so $\det(A) = \det(U) = 10$.
- The product of upper triangular matrices is upper triangular, and so is the inverse of an invertible one.

The **lower triangular** counterpart, with zeros above the diagonal, is the matrix $L$ in $A = LU$.

---

### `6. Back Substitution`

Once the system is $U\mathbf{x} = \mathbf{c}$, solve from the **last equation upward**:

$$
\begin{aligned}
x + 2y + z &= 2 \\
2y - 2z &= 6 \\
5z &= -10
\end{aligned}
$$

1. Last equation: $z = -2$.
2. Middle equation: $2y - 2(-2) = 6$, so $y = 1$.
3. First equation: $x + 2(1) + (-2) = 2$, so $x = 2$.

**`General formula`**

For an upper triangular $U$ and right-hand side $\mathbf{c}$, working from $i = n$ down to $i = 1$:

$$
x_i = \frac{c_i - \sum_{j=i+1}^{n} u_{ij}\,x_j}{u_{ii}}
$$

This divides by each pivot $u_{ii}$, which is why every pivot must be nonzero.

**Where does $\mathbf{c}$ come from?**

$\mathbf{c}$ is $\mathbf{b}$ after the same row operations as $A$:

- Step 1: $12 - 3(2) = 6$
- Step 2: $2 - 2(6) = -10$

So $\mathbf{c} = (2,\ 6,\ -10)$. In matrix form, $\mathbf{c} = E\mathbf{b}$ (section 9).

**`Cost`**

Back substitution takes about $n^2/2$ multiplications, which is far cheaper than elimination.

---

### `7. Elementary Matrices`

An **elementary matrix** is the identity matrix with **one** row operation applied. Multiplying a matrix on the **left** by it performs that same row operation.

There is one type for each row operation:

| Type | Example ($3 \times 3$) | Effect of $EA$ |
|------|------------------------|----------------|
| Replacement | A = $\begin{bmatrix} 1&0&0\\-3&1&0\\0&0&1 \end{bmatrix}$ | Row 2 $\leftarrow$ row 2 $- 3 \times$ row 1 |
| Exchange | A = $\begin{bmatrix} 0&1&0\\1&0&0\\0&0&1 \end{bmatrix}$ | Swap rows 1 and 2 |
| Scaling | A = $\begin{bmatrix} 1&0&0\\0&\tfrac12&0\\0&0&1 \end{bmatrix}$ | Row 2 $\leftarrow \tfrac12 \times$ row 2 |

Example with the running matrix:

$$
E_{21}A =
\begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}
\begin{bmatrix} 1 & 2 & 1 \\ 3 & 8 & 1 \\ 0 & 4 & 1 \end{bmatrix} =
\begin{bmatrix} 1 & 2 & 1 \\ 0 & 2 & -2 \\ 0 & 4 & 1 \end{bmatrix}
$$

Every elementary matrix is invertible, because every row operation can be undone.

---

### `8. Elimination Matrices`

An **elimination matrix** $E_{ij}$ is an elementary matrix of the replacement type. It is the identity matrix with $-\ell_{ij}$ in position $(i, j)$.

The running example needs two (since $\ell_{31} = 0$, no $E_{31}$ is needed):

$$
E_{21} = \begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix},
\qquad
E_{32} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & -2 & 1 \end{bmatrix}
$$

Applying them in order gives $U$:

$$
E_{21}A = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 2 & -2 \\ 0 & 4 & 1 \end{bmatrix}
\quad\Rightarrow\quad
E_{32}(E_{21}A) = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 2 & -2 \\ 0 & 0 & 5 \end{bmatrix} = U
$$

Key points:

- $E_{ij}$ is **lower triangular** with ones on the diagonal.
- The subscripts tell you which entry is being eliminated: $E_{32}$ makes the $(3,2)$ entry zero.
- For an $n \times n$ matrix with no row exchanges, at most $n(n-1)/2$ elimination matrices are needed (3 for a $3 \times 3$).

---

## `3. Matrix Multiplication in Elimination`

**`1. Four ways to see a product`**

For $A$ of size $m \times n$ and $B$ of size $n \times p$, the product $AB$ is $m \times p$.

1. **Entry by entry:** $(AB)_{ij} = \text{(row } i \text{ of } A) \cdot (\text{column } j \text{ of } B)$.
2. **Column by column:** each column of $AB$ is $A$ times the corresponding column of $B$.
3. **Row by row:** each row of $AB$ is the corresponding row of $A$ times $B$.
4. **Columns times rows:** $AB = \sum_k (\text{column } k \text{ of } A)(\text{row } k \text{ of } B)$.

Small example of view 1, with $A = \begin{bmatrix} 1&1\\0&1 \end{bmatrix}$ and $B = \begin{bmatrix} 1&0\\1&1 \end{bmatrix}$:

$$
(AB)_{11} = (1)(1) + (1)(1) = 2
$$

**`2. Left multiplication acts on rows`**

By view 3, each row of $EA$ is a combination of the **rows** of $A$. That is why row operations are performed by multiplying on the **left**.

Row 3 of $E_{32}E_{21}$ in the running example, applied to $A$:

$$
\text{new row 3} = 6\,(\text{row 1}) - 2\,(\text{row 2}) + 1\,(\text{row 3})
$$

`Combining all steps`

All the elimination steps collapse into one matrix $E = E_{32}E_{21}$:

$$
E = \begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 6 & -2 & 1 \end{bmatrix}, \qquad EA = U
$$

Check, row 3 of $EA$: $6(1,2,1) - 2(3,8,1) + (0,4,1) = (0,\ 0,\ 5)$ ✓.

The same $E$ acts on the right-hand side:

$$
E\mathbf{b} =
\begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 6 & -2 & 1 \end{bmatrix}
\begin{bmatrix} 2 \\ 12 \\ 2 \end{bmatrix} =
\begin{bmatrix} 2 \\ 6 \\ -10 \end{bmatrix} = \mathbf{c}
$$

So $A\mathbf{x} = \mathbf{b}$ becomes $EA\mathbf{x} = E\mathbf{b}$, i.e. $U\mathbf{x} = \mathbf{c}$.

Note the $6$ in $E$: it equals $\ell_{21}\ell_{32} = 3 \times 2$. The steps interact, so $E$ is messier than the individual multipliers. Section 12 shows how $L$ avoids this.

---

### **`1. Permutation Matrices`**

A **permutation matrix** $P$ is the identity matrix with its rows reordered. It has exactly one $1$ in each row and each column.

All six $3 \times 3$ permutation matrices come from reordering the rows of $I$: the identity itself, three single swaps ($P_{12}$, $P_{13}$, $P_{23}$), and two cyclic shifts.

$$
P_{12} = \begin{bmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix},
\qquad
P_{23} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 1 & 0 \end{bmatrix}
$$

**`Properties`**

- There are $n!$ permutation matrices of size $n \times n$.
- The inverse is the transpose: $P^{-1} = P^{T}$. For a single swap, $P^2 = I$.
- A product of permutation matrices is a permutation matrix.
- $\det(P) = \pm 1$ (it is $+1$ for an even number of swaps and $-1$ for an odd number).

**Why they matter: $PA = LU$**

When a zero pivot appears, row exchanges are needed. Collect all the exchanges into one matrix $P$ and elimination becomes

$$
PA = LU
$$

**Example.** Take

$$
A = \begin{bmatrix} 1 & 2 & 1 \\ 2 & 4 & 5 \\ 0 & 3 & 1 \end{bmatrix}
$$

Step 1: row 2 $-\ 2 \times$ row 1 gives $\begin{bmatrix} 0 & 0 & 3 \end{bmatrix}$ for row 2, so the $(2,2)$ pivot position holds a zero. Row 3 has a nonzero entry there, so **exchange rows 2 and 3**:

$$
U = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 0 & 0 & 3 \end{bmatrix},
\qquad
P = P_{23},
\qquad
PA = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 2 & 4 & 5 \end{bmatrix},
\qquad
L = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 2 & 0 & 1 \end{bmatrix}
$$

Check, row 3 of $LU$: $2(1,2,1) + 0 + 1(0,0,3) = (2,4,5)$ ✓.

For every nonsingular matrix there is some permutation $P$ that makes $PA = LU$ possible.

---

### **`2. Row Exchanges and Column Exchanges`**

Where $P$ is placed decides what gets swapped. With $P = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}$ and $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$:

$$
PA = \begin{bmatrix} c & d \\ a & b \end{bmatrix}
\quad \text{(rows swapped)},
\qquad
AP = \begin{bmatrix} b & a \\ d & c \end{bmatrix}
\quad \text{(columns swapped)}
$$

| Product | Effect | Effect on $A\mathbf{x} = \mathbf{b}$ |
|---------|--------|--------------------------------------|
| $PA$ | Exchanges **rows** of $A$ | Reorders the equations; same solution (also swap entries of $\mathbf{b}$) |
| $AP$ | Exchanges **columns** of $A$ | Reorders the unknowns; entries of $\mathbf{x}$ trade places |

Why it works this way:

- Rows of $PA$ are combinations of **rows** of $A$ (left multiplication), so $P$ reorders rows.
- Columns of $AP$ are combinations of **columns** of $A$ (right multiplication), so $P$ reorders columns.

In elimination, only **row** exchanges are used, because they never change the solution. Column exchanges are used in some advanced methods (complete pivoting), but then the unknowns must be reordered back at the end.

---

### `3. Inverse of Elimination Matrices`

Each elimination step can be undone. The inverse of an elimination matrix **adds back** the multiple that was subtracted, so the sign of the multiplier flips:

$$
E_{21}^{-1} = \begin{bmatrix} 1 & 0 & 0 \\ 3 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix},
\qquad
E_{32}^{-1} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 2 & 1 \end{bmatrix}
$$

Check: $E_{21}E_{21}^{-1} = I$ (subtract $3\times$ row 1, then add it back).

**`Inverse of a product reverses the order`**

$$
(AB)^{-1} = B^{-1}A^{-1}
$$

Like taking off shoes and socks: whatever was done last must be undone first. From $E_{32}E_{21}A = U$, undo the steps in reverse order:

$$
A = E_{21}^{-1}E_{32}^{-1}\,U = LU,
\qquad
L = E_{21}^{-1}E_{32}^{-1} = \begin{bmatrix} 1 & 0 & 0 \\ 3 & 1 & 0 \\ 0 & 2 & 1 \end{bmatrix}
$$

**Why $L$ is cleaner than $E$**

| Matrix | Product | Result | Mixed? |
|--------|---------|--------|--------|
| $E$ | $E_{32}E_{21}$ | has the entry $6 = 3 \times 2$ | Yes |
| $L$ | $E_{21}^{-1}E_{32}^{-1}$ | multipliers $3, 0, 2$ appear directly | No |

In $L$, the multipliers are placed exactly where they were used, with no sign change and no mixing. That is why elimination is usually recorded as $A = LU$ rather than $EA = U$.

Check, row 2 of $LU$: $3\,(1,2,1) + 1\,(0,2,-2) = (3,8,1)$, which matches row 2 of $A$ ✓.

**Why $A = LU$ is useful**

Solving $A\mathbf{x} = \mathbf{b}$ becomes two cheap triangular solves:

1. **Forward substitution:** solve $L\mathbf{c} = \mathbf{b}$ (top to bottom).
2. **Back substitution:** solve $U\mathbf{x} = \mathbf{c}$ (bottom to top).

For the example: $L\mathbf{c} = \mathbf{b}$ gives $c_1 = 2$, then $3(2) + c_2 = 12$ so $c_2 = 6$, then $2(6) + c_3 = 2$ so $c_3 = -10$. This matches the $\mathbf{c}$ found earlier.

The expensive elimination is done **once**. For any new right-hand side $\mathbf{b}$, only the cheap triangular solves are repeated.

---

### **`13. Associative Property of Matrix Multiplication`**

Matrix multiplication is **associative**:

$$
(AB)C = A(BC)
$$

The grouping does not matter, as long as the **order** of the matrices stays the same.

**`Why it matters in elimination`**

It lets us combine steps into one matrix:

$$
(E_{32}E_{21})A = E_{32}(E_{21}A)
$$

- **Right side:** apply $E_{21}$ to $A$, then $E_{32}$ to the result (step by step).
- **Left side:** multiply $E_{32}E_{21}$ into a single matrix $E$ first, then apply it to $A$.

Both give $U$. The same idea justifies the formula $A = LU$ and the rule $(AB)^{-1} = B^{-1}A^{-1}$.

**`Associativity and efficiency`**

The grouping does not change the answer, but it can change the **cost**. For a matrix $A$ and vectors $\mathbf{u}, \mathbf{v}$:

$$
(A\mathbf{u})\mathbf{v}^T \quad \text{vs.} \quad A(\mathbf{u}\mathbf{v}^T)
$$

The first multiplies a matrix by a vector, then forms an outer product. The second builds a full $n \times n$ matrix first, then multiplies, which is much more work.

**`What is 'not' allowed`**

Associativity lets you regroup, but not reorder. $(AB)C = A(BC)$ is fine, while $(AB)C = (BA)C$ is generally false (next section).

---

### **`4. Non-Commutative Property of Matrix Multiplication (AB ≠ BA)`**

Matrix multiplication is **not commutative**: in general,

$$
AB \neq BA
$$

**Example:**

$$
A = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix},
\quad
B = \begin{bmatrix} 1 & 0 \\ 1 & 1 \end{bmatrix}
\qquad\Rightarrow\qquad
AB = \begin{bmatrix} 2 & 1 \\ 1 & 1 \end{bmatrix},
\quad
BA = \begin{bmatrix} 1 & 1 \\ 1 & 2 \end{bmatrix}
$$

Reasons:

- $AB$ means "apply $B$ first, then $A$", and the order of two transformations usually matters.
- Even the sizes can prevent it: a $2\times3$ times a $3\times2$ is $2\times2$, but reversing gives $3\times3$.
- $AB$ combines **rows of $B$**, while $BA$ combines **columns of $B$**, which are different things.

**`In elimination: order of steps matters`**

$$
E_{32}E_{21} = \begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 6 & -2 & 1 \end{bmatrix}
\;\neq\;
E_{21}E_{32} = \begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 0 & -2 & 1 \end{bmatrix}
$$

Only $E_{32}E_{21}$ (apply $E_{21}$ first) correctly reduces $A$ to $U$, because $E_{32}$ needs the zero that $E_{21}$ created.

**`When matrices do commute`**

- $AI = IA = A$ for the identity matrix.
- A matrix and its inverse: $AA^{-1} = A^{-1}A = I$.
- Powers of the same matrix: $A^2A^3 = A^3A^2$.
- Diagonal matrices of the same size.
- Elimination matrices that use the **same pivot row** to change different rows, such as $E_{21}$ and $E_{31}$. They affect different rows independently, so $E_{21}E_{31} = E_{31}E_{21}$.

**`Related rules to remember`**

| Rule | Statement |
|------|-----------|
| Transpose of a product | $(AB)^T = B^TA^T$ |
| Inverse of a product | $(AB)^{-1} = B^{-1}A^{-1}$ |
| Distributive | $A(B+C) = AB + AC$ |

Both the transpose and inverse rules **reverse the order**, a direct consequence of non-commutativity.

---
