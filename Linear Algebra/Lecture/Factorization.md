## `1. Inverse of a Product`

### `Idea`

If $A$ and $B$ are both invertible $n \times n$ matrices, then the product $AB$ is also invertible. Its inverse is the product of the individual inverses **in reverse order**:

$$(AB)^{-1} = B^{-1}A^{-1}$$

### `Proof`

Multiply $AB$ by the proposed inverse and watch the middle cancel:

$$(AB)(B^{-1}A^{-1}) = A\,(BB^{-1})\,A^{-1} = A\,I\,A^{-1} = AA^{-1} = I$$

The same works from the other side:

$$(B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B = B^{-1}B = I$$

### `Intuition`

Putting on socks and then shoes is the operation $AB$ (socks first, shoes second). To undo it you must remove the shoes first, then the socks. The last operation applied is the first one undone.

### `Why the order matters`

Matrix multiplication is generally not commutative, so $A^{-1}B^{-1} \neq B^{-1}A^{-1}$ in general.

### `Example`

Let

$$A = \begin{bmatrix} 1 & 2 \\ 0 & 1 \end{bmatrix}, \qquad B = \begin{bmatrix} 1 & 0 \\ 3 & 1 \end{bmatrix}$$

**Step 1: Compute the product.**

$$AB = \begin{bmatrix} 1\cdot1+2\cdot3 & 1\cdot0+2\cdot1 \\ 0\cdot1+1\cdot3 & 0\cdot0+1\cdot1 \end{bmatrix} = \begin{bmatrix} 7 & 2 \\ 3 & 1 \end{bmatrix}$$

**Step 2: Invert $AB$ directly.** Here $\det(AB) = 7\cdot1 - 2\cdot3 = 1$, so

$$(AB)^{-1} = \frac{1}{1}\begin{bmatrix} 1 & -2 \\ -3 & 7 \end{bmatrix} = \begin{bmatrix} 1 & -2 \\ -3 & 7 \end{bmatrix}$$

**Step 3: Invert each factor.**

$$A^{-1} = \begin{bmatrix} 1 & -2 \\ 0 & 1 \end{bmatrix}, \qquad B^{-1} = \begin{bmatrix} 1 & 0 \\ -3 & 1 \end{bmatrix}$$

**Step 4: Multiply in reverse order.**

$$B^{-1}A^{-1} = \begin{bmatrix} 1 & 0 \\ -3 & 1 \end{bmatrix}\begin{bmatrix} 1 & -2 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} 1 & -2 \\ -3 & 7 \end{bmatrix} \checkmark$$

This matches Step 2.

**Step 5: Show the wrong order fails.**

$$A^{-1}B^{-1} = \begin{bmatrix} 1 & -2 \\ 0 & 1 \end{bmatrix}\begin{bmatrix} 1 & 0 \\ -3 & 1 \end{bmatrix} = \begin{bmatrix} 7 & -2 \\ -3 & 1 \end{bmatrix} \neq (AB)^{-1}$$

### Extension to many factors

$$(ABC)^{-1} = C^{-1}B^{-1}A^{-1}, \qquad (A_1A_2\cdots A_k)^{-1} = A_k^{-1}\cdots A_2^{-1}A_1^{-1}$$

---

## `2. Transpose and Inverse`

### `The transpose`

The transpose $A^T$ swaps rows and columns: $(A^T)_{ij} = A_{ji}$.

Useful rules:

- $(A^T)^T = A$
- $(A + B)^T = A^T + B^T$
- $(AB)^T = B^T A^T$ (order reverses, just like inverses)

### `The key result`

$$(A^T)^{-1} = (A^{-1})^T$$

The inverse of a transpose equals the transpose of the inverse. So transposing and inverting can be done in either order.

### Proof

Start with $A^{-1}A = I$ and transpose both sides, using $(AB)^T = B^TA^T$:

$$(A^{-1}A)^T = I^T \;\Longrightarrow\; A^T (A^{-1})^T = I$$

So $(A^{-1})^T$ is the matrix that multiplies $A^T$ to give $I$. By definition, that is $(A^T)^{-1}$.

### `Example`

$$A = \begin{bmatrix} 1 & 2 \\ 3 & 7 \end{bmatrix}$$

**Compute $A^{-1}$.** $\det A = 7 - 6 = 1$, so

$$A^{-1} = \begin{bmatrix} 7 & -2 \\ -3 & 1 \end{bmatrix}$$

**Route 1: transpose of the inverse.**

$$(A^{-1})^T = \begin{bmatrix} 7 & -3 \\ -2 & 1 \end{bmatrix}$$

**Route 2: inverse of the transpose.**

$$A^T = \begin{bmatrix} 1 & 3 \\ 2 & 7 \end{bmatrix}, \qquad (A^T)^{-1} = \frac{1}{1}\begin{bmatrix} 7 & -3 \\ -2 & 1 \end{bmatrix} = \begin{bmatrix} 7 & -3 \\ -2 & 1 \end{bmatrix}$$

Both routes agree. **Verification:**

$$A^T(A^{-1})^T = \begin{bmatrix} 1 & 3 \\ 2 & 7 \end{bmatrix}\begin{bmatrix} 7 & -3 \\ -2 & 1 \end{bmatrix} = \begin{bmatrix} 7-6 & -3+3 \\ 14-14 & -6+7 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} \checkmark$$

### Special case: symmetric matrices

If $A = A^T$ (symmetric) and $A$ is invertible, then $A^{-1}$ is also symmetric, because $(A^{-1})^T = (A^T)^{-1} = A^{-1}$.

---

## `3. Elimination Matrices`

### `What they are`

Gaussian elimination turns $A$ into an upper triangular matrix by row operations of the form:

> Subtract $\ell_{ij}$ times row $j$ from row $i$.

Each such step is carried out by multiplying on the left by an **elementary elimination matrix** $E_{ij}$.

### `Multipliers`

The multiplier is

$$\ell_{ij} = \frac{\text{entry to eliminate in row } i,\ \text{column } j}{\text{pivot in row } j,\ \text{column } j}$$

The pivot must be nonzero.

### `Form of $E_{ij}$`

$E_{ij}$ is the identity matrix with $-\ell_{ij}$ placed in position $(i,j)$. For a $3 \times 3$ system:

$$E_{21} = \begin{bmatrix} 1 & 0 & 0 \\ -\ell_{21} & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}, \quad E_{31} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ -\ell_{31} & 0 & 1 \end{bmatrix}, \quad E_{32} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & -\ell_{32} & 1 \end{bmatrix}$$

### `Inverse of an elimination matrix`

To undo "subtract $\ell_{ij}$ times row $j$ from row $i$", you **add** it back. So the inverse just flips the sign of the off-diagonal entry:

$$E_{21}^{-1} = \begin{bmatrix} 1 & 0 & 0 \\ \ell_{21} & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$$

### `Worked example`

$$A = \begin{bmatrix} 2 & 1 & 1 \\ 4 & -6 & 0 \\ -2 & 7 & 2 \end{bmatrix}$$

**Step 1: eliminate the $(2,1)$ entry.** Pivot is $2$, entry is $4$, so $\ell_{21} = 4/2 = 2$. Row 2 becomes $\text{row}_2 - 2\,\text{row}_1 = [0,\,-8,\,-2]$.

$$E_{21} = \begin{bmatrix} 1 & 0 & 0 \\ -2 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}, \qquad E_{21}A = \begin{bmatrix} 2 & 1 & 1 \\ 0 & -8 & -2 \\ -2 & 7 & 2 \end{bmatrix}$$

**Step 2: eliminate the $(3,1)$ entry.** Entry is $-2$, so $\ell_{31} = -2/2 = -1$. Row 3 becomes $\text{row}_3 + \text{row}_1 = [0,\,8,\,3]$.

$$E_{31} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 1 & 0 & 1 \end{bmatrix}, \qquad E_{31}E_{21}A = \begin{bmatrix} 2 & 1 & 1 \\ 0 & -8 & -2 \\ 0 & 8 & 3 \end{bmatrix}$$

**Step 3: eliminate the $(3,2)$ entry.** The pivot is now $-8$ and the entry is $8$, so $\ell_{32} = 8/(-8) = -1$. Row 3 becomes $\text{row}_3 + \text{row}_2 = [0,\,0,\,1]$.

$$E_{32} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 1 & 1 \end{bmatrix}, \qquad E_{32}E_{31}E_{21}A = \begin{bmatrix} 2 & 1 & 1 \\ 0 & -8 & -2 \\ 0 & 0 & 1 \end{bmatrix} = U$$

**Inverses of the three elimination matrices** (flip the sign of the off-diagonal entry):

$$E_{21}^{-1} = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}, \quad E_{31}^{-1} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ -1 & 0 & 1 \end{bmatrix}, \quad E_{32}^{-1} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & -1 & 1 \end{bmatrix}$$

These will be used in Section 5 to build $L$.

---

## 4. `LU Factorization`

### `Meaning`

LU factorization writes a square matrix as a product of two triangular matrices:

$$A = LU$$

- **$L$ (lower triangular):** zeros above the diagonal, **1s on the diagonal**, and the elimination multipliers below the diagonal.
- **$U$ (upper triangular):** zeros below the diagonal. It is the end result of elimination, and its diagonal holds the **pivots**.

$$L = \begin{bmatrix} 1 & 0 & 0 \\ \ell_{21} & 1 & 0 \\ \ell_{31} & \ell_{32} & 1 \end{bmatrix}, \qquad U = \begin{bmatrix} u_{11} & u_{12} & u_{13} \\ 0 & u_{22} & u_{23} \\ 0 & 0 & u_{33} \end{bmatrix}$$

### `Why it is useful`

- Triangular systems are very cheap to solve (Section 6).
- $A$ is factored once, then reused for many right-hand sides.
- The factorization records everything elimination did.

### `Small example`

$$A = \begin{bmatrix} 2 & 1 \\ 6 & 8 \end{bmatrix}$$

The multiplier is $\ell_{21} = 6/2 = 3$. Subtracting $3\times$ row 1 from row 2 gives $[0,\ 8-3] = [0,\ 5]$.

$$U = \begin{bmatrix} 2 & 1 \\ 0 & 5 \end{bmatrix}, \qquad L = \begin{bmatrix} 1 & 0 \\ 3 & 1 \end{bmatrix}$$

**Check:**

$$LU = \begin{bmatrix} 1 & 0 \\ 3 & 1 \end{bmatrix}\begin{bmatrix} 2 & 1 \\ 0 & 5 \end{bmatrix} = \begin{bmatrix} 2 & 1 \\ 6 & 3+5 \end{bmatrix} = \begin{bmatrix} 2 & 1 \\ 6 & 8 \end{bmatrix} = A \checkmark$$

### `When row exchanges are needed`

If a zero appears in a pivot position, rows must be swapped. This is recorded in a permutation matrix $P$, and the factorization becomes

$$PA = LU$$

Example: $A = \begin{bmatrix} 0 & 1 \\ 2 & 3 \end{bmatrix}$ has a zero pivot. With $P = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}$,

$$PA = \begin{bmatrix} 2 & 3 \\ 0 & 1 \end{bmatrix} = \underbrace{\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}}_{L}\underbrace{\begin{bmatrix} 2 & 3 \\ 0 & 1 \end{bmatrix}}_{U}$$

---

## `5. Finding L and U`

### `The method`

**Step 1: Reduce $A$ to $U$ by elimination.** Apply elimination matrices one by one:

$$E_{32}E_{31}E_{21}A = U$$

Let $E = E_{32}E_{31}E_{21}$, so $EA = U$.

**Step 2: Invert $E$ to get $L$.** Multiply both sides by $E^{-1}$:

$$A = E^{-1}U = LU \qquad\text{where}\qquad L = E^{-1}$$

Using the inverse-of-a-product rule from Section 1:

$$L = E^{-1} = E_{21}^{-1}\,E_{31}^{-1}\,E_{32}^{-1}$$

Notice the order is the reverse of how the $E$'s were applied.

**Step 3: Read off $L$.** The multipliers go straight into their positions.

### Continuing the $3 \times 3$ example from Section 3

We found $U$ already:

$$U = \begin{bmatrix} 2 & 1 & 1 \\ 0 & -8 & -2 \\ 0 & 0 & 1 \end{bmatrix}$$

The multipliers were $\ell_{21} = 2$, $\ell_{31} = -1$, $\ell_{32} = -1$. Place them below the diagonal:

$$L = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ -1 & -1 & 1 \end{bmatrix}$$

**Verification by multiplication $LU$:**

- Row 1: $[2,\ 1,\ 1]$
- Row 2: $2[2,1,1] + [0,-8,-2] = [4,\ -6,\ 0]$
- Row 3: $-1[2,1,1] - 1[0,-8,-2] + [0,0,1] = [-2,\ 7,\ 2]$

This reproduces $A$ exactly. $\checkmark$

### `Relationship between E and L`

Multiplying the three elimination matrices together gives

$$E = E_{32}E_{31}E_{21} = \begin{bmatrix} 1 & 0 & 0 \\ -2 & 1 & 0 \\ -1 & 1 & 1 \end{bmatrix}$$

Its $(3,1)$ entry is $-1$, which is **not** simply $-\ell_{31} = 1$. The multipliers have mixed: that entry equals $-\ell_{31} + \ell_{32}\ell_{21} = 1 + (-1)(2) = -1$. So $E$ is messy.

But $L = E^{-1}$ has no mixing:

$$L = E^{-1} = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ -1 & -1 & 1 \end{bmatrix}$$

You can confirm $LE = I$ by multiplying them. This is why LU is convenient: **we never need to compute $E$**. We just store each multiplier in its slot as elimination proceeds.

| Matrix | Contents | Clean? |
|--------|----------|--------|
| $E$ | Negated multipliers that interact with each other | No, entries mix |
| $L = E^{-1}$ | Multipliers exactly as computed, in position $(i,j)$ | Yes |

### `Algorithm summary`

For each column $k = 1, \dots, n-1$, and each row $i > k$:

1. Compute $\ell_{ik} = u_{ik}/u_{kk}$ and store it in $L$.
2. Update row $i$ of $U$: $\text{row}_i \leftarrow \text{row}_i - \ell_{ik}\cdot\text{row}_k$.

---

## `6. Solving Linear Systems Using LU`

### `The two-step process`

To solve $Ax = b$, replace $A$ with $LU$:

$$LUx = b$$

Introduce an intermediate vector $y = Ux$. Then:

1. **Solve $Ly = b$** by forward substitution.
2. **Solve $Ux = y$** by backward substitution.

### Forward substitution (for $L$)

Since $L$ is lower triangular, solve from the top row down:

$$y_i = b_i - \sum_{j=1}^{i-1} \ell_{ij}\,y_j$$

(The diagonal of $L$ is 1, so no division is needed.)

### Backward substitution (for $U$)

Since $U$ is upper triangular, solve from the bottom row up:

$$x_i = \frac{1}{u_{ii}}\left(y_i - \sum_{j=i+1}^{n} u_{ij}\,x_j\right)$$

### `Worked example`

Use the factorization of the $3 \times 3$ matrix from Section 5, and solve $Ax = b$ with

$$b = \begin{bmatrix} 5 \\ -2 \\ 9 \end{bmatrix}$$

**Stage 1: Forward substitution, $Ly = b$.**

$$\begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ -1 & -1 & 1 \end{bmatrix}\begin{bmatrix} y_1 \\ y_2 \\ y_3 \end{bmatrix} = \begin{bmatrix} 5 \\ -2 \\ 9 \end{bmatrix}$$

- Row 1: $y_1 = 5$
- Row 2: $2(5) + y_2 = -2 \Rightarrow y_2 = -12$
- Row 3: $-5 - (-12) + y_3 = 9 \Rightarrow y_3 = 2$

$$y = \begin{bmatrix} 5 \\ -12 \\ 2 \end{bmatrix}$$

**Stage 2: Backward substitution, $Ux = y$.**

$$\begin{bmatrix} 2 & 1 & 1 \\ 0 & -8 & -2 \\ 0 & 0 & 1 \end{bmatrix}\begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} 5 \\ -12 \\ 2 \end{bmatrix}$$

- Row 3: $x_3 = 2$
- Row 2: $-8x_2 - 2(2) = -12 \Rightarrow x_2 = 1$
- Row 1: $2x_1 + 1 + 2 = 5 \Rightarrow x_1 = 1$

$$x = \begin{bmatrix} 1 \\ 1 \\ 2 \end{bmatrix}$$

**Check against the original system:**

$$Ax = \begin{bmatrix} 2+1+2 \\ 4-6+0 \\ -2+7+4 \end{bmatrix} = \begin{bmatrix} 5 \\ -2 \\ 9 \end{bmatrix} = b \checkmark$$

### `Reusing the factorization for a second right-hand side`

Now solve for $b = \begin{bmatrix} 2 \\ 4 \\ -2 \end{bmatrix}$ with the **same** $L$ and $U$, with no new elimination.

- Forward: $y_1 = 2$; $2(2)+y_2 = 4 \Rightarrow y_2 = 0$; $-2 - 0 + y_3 = -2 \Rightarrow y_3 = 0$
- Backward: $x_3 = 0$; $-8x_2 = 0 \Rightarrow x_2 = 0$; $2x_1 = 2 \Rightarrow x_1 = 1$

$$x = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}$$

This makes sense: $b$ is the first column of $A$, so $x = e_1$. $\checkmark$

---

## `7. Computational Cost of Elimination`

Costs are counted in basic operations (a multiply-and-subtract pair counts as one).

### `Cost of elimination (factoring $A = LU$)`

At step $k$ the remaining submatrix has size about $(n-k+1)\times(n-k+1)$. Clearing the first column of an $n \times n$ matrix needs about $n$ row operations, each touching about $n$ entries, so roughly $n^2$ operations. The next step works on an $(n-1)\times(n-1)$ block, and so on:

$$n^2 + (n-1)^2 + \cdots + 2^2 + 1^2 = \frac{n(n+1)(2n+1)}{6} \approx \frac{n^3}{3}$$

So elimination costs about $\dfrac{n^3}{3}$ operations, which is $O(n^3)$.

### Cost of solving with $L$ and $U$

| Task | Approximate operations | Complexity |
|------|------------------------|------------|
| Factor $A = LU$ | $\tfrac{n^3}{3}$ | $O(n^3)$ |
| Forward substitution ($Ly=b$) | $\tfrac{n^2}{2}$ | $O(n^2)$ |
| Backward substitution ($Ux=y$) | $\tfrac{n^2}{2}$ | $O(n^2)$ |
| **One new right-hand side (after factoring)** | $n^2$ | $O(n^2)$ |

### `Concrete numbers`

| $n$ | Factoring ($\approx n^3/3$) | Each extra solve ($\approx n^2$) |
|-----|------------------------------|----------------------------------|
| 10 | about 333 | 100 |
| 100 | about 333,000 | 10,000 |
| 1,000 | about 333,000,000 | 1,000,000 |

### `Takeaways`

- **Doubling $n$ multiplies the factoring cost by 8**, since $2^3 = 8$.
- Once $L$ and $U$ are known, each additional right-hand side costs only about $n^2$, a factor of roughly $n/3$ cheaper than refactoring.
- Example: solving 100 systems with a $1000 \times 1000$ matrix costs about $3.3\times10^8 + 100\times10^6 \approx 4.3\times10^8$ operations with LU, versus about $3.3\times10^{10}$ if elimination were repeated each time.
- Explicitly computing $A^{-1}$ costs about $n^3$ operations, so it is generally avoided. Factor with LU and solve instead.

---