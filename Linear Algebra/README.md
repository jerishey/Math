# Linear Algebra
Linear Algebra is the branch of mathematics that focuses on the study of vectors, vector spaces, matrices and linear transformations.

- Deals with linear equations, linear functions and their representations through matrices and determinants.
- Used in quantum mechanics, computer graphics and optimization
- Basic concept for machine learning and data science.
<br>

## <b>`Why Learn Linear Algebra?`</b>
```bash
1. Machine Learning & AI: Every neural network, regression model and dimensionality reduction algorithm (PCA, SVD) is built on linear algebra operations.

2. Computer Graphics: Rotations, scaling and 3D projections in games and animation are all matrix transformations.

3. Physics & Engineering: Quantum mechanics, structural analysis and control systems all rely on eigenvalues and vector spaces.

4. Data Science: Working with high-dimensional datasets, covariance matrices and feature transformations requires fluency in linear algebra.
```

## `Uses of Linear Algebra`
```bash
1. Machine Learning: Used to represent and process data using vectors and matrices in algorithms.

2. Artificial Intelligence: Helps in building and optimizing neural networks using matrix operations.

3. Data Science: Used to organize, analyze, and reduce large datasets efficiently.

4. Computer Graphics: Used to perform transformations like rotation, scaling, and translation of objects.

5. Image Processing: Represents images as matrices to apply filters and enhancements.

6. Search Engines: Used to measure similarity between data using vector representations.
```

## `1. Scalar`
Scalar is a single numerical value that conveys magnitude but no direction or dimension. It is a zero-dimensional entity, meaning it cannot be decomposed into smaller parts or represented along any axis. 
<br>
Scalars serve as the fundamental units of computation in mathematics, physics and computer science.

**`Features of Scalar`**
```bash
1. Represents a single quantity such as temperature, accuracy or cost.

2. Serves as the building block for forming higher-dimensional data structures like vectors and matrices.

3. Use Case: Used in machine learning to represent loss functions, accuracy values or statistical measures such as mean and variance.

4. Advantage: Simple to store and compute; forms the foundation for complex mathematical models.

5. Disadvantage: Cannot represent any direction, relationship or multidimensional structure.
```
---
**`Scalar Quantities :`** 
A scalar quantity is a physical quantity that has only magnitude and no direction.
```bash
1. It is described by a single numerical value, typically with units.

2. Scalars represent quantities where direction is not relevant, such as temperature, mass, time, and energy.

3. They can be added, subtracted, multiplied, and divided using standard arithmetic operations.

4. Scalars are easier to work with compared to vector quantities since they don’t require considering directions or components.
```

<b>`Example:` </b>
```bash
Temperature
Mass
Time
Distance
Speed
Energy
Area
Volume
```
---

## `2. Vector`

In mathematics, vectors are fundamental objects that represent quantities with both magnitude and direction. They are widely used in various branches of mathematics, physics, engineering, computer science, and other disciplines.

**`Key Features of Vectors:`**

`1. Magnitude :` A vector has a size or length called its magnitude.
- The size or length of the vector.
- Denoted by $|\vec{v}|$ or $\|\vec{v}\|$

`2. Direction :` A vector always points in a specific direction.
- The direction of the vector in space.
- Represented by the arrowhead that indicates where the vector points.

---

**`Real-life analogy of Vectors`**

To better understand vectors, consider a situation where a football coach is training a goalkeeper to pass the ball. The coach needs to instruct the goalkeeper:
- `Direction:` Where to send the ball (toward another player or a specific region).
- `Magnitude:` How hard to kick the ball (the strength of the pass).

---

**`Representation of Vector`**

Vectors are represented by taking an arrow above the quantity to indicate that it has both magnitude and direction.
<br>
The Force vector is represented $\vec{F}$ where the arrow above F represents that it is a vector quantity. 
<br>


<i> Vectors can also be represented by taking their respective magnitude in x, y, and z-directions.
- The x-direction is represented by $\hat{i}$.
- The y-direction is represented by $\hat{j}$.
- The z-direction is represented by $\hat{k}$.
<br>

Thus, a vector $\vec{A}$ can be written as :

$$
\vec{A} = x\hat{i} + y\hat{j} + z\hat{k}
$$

```bash
Explanation:

1. x : Magnitude of the vector along the x-axis,
2. y : Magnitude along the y-axis,
3. z : Magnitude along the z-axis.

- The point where the vector starts is called the tail of the vector and the endpoint of the vector is called the head of the vector. We can also denote the vector as the coordinate point in 3-Dimensions. 
```
</i>
---

**`Types of Vectors`**
Vectors can be classified into different categories on the basis of their magnitude and direction.

`The various types of vectors are :` 

`1. Row Vector`

A **row vector** is a vector written **horizontally**, as a single row of numbers. In matrix terms, it is a **1 × n** matrix (1 row, n columns).

**General form:**
```
v = [ v1  v2  v3  ...  vn ]
```

**Example:**
```
v = [ 2  5  7 ]
```

This is a 1 × 3 row vector.

**Key point :**  Row vectors are often used when a vector needs to be multiplied *on the left* in matrix multiplication, since matrix dimensions must match (m × n) × (n × p).

---

`2. Column Vector`

A **column vector** is a vector written **vertically**, as a single column of numbers. In matrix terms, it is an **n × 1** matrix (n rows, 1 column).

**General form:**
```
    | v1 |
v = | v2 |
    | v3 |
    | .. |
    | vn |
```

**Example:**
```
    | 2 |
v = | 5 |
    | 7 |
```

This is a 3 × 1 column vector.

**Key point :** Column vectors are the standard/default form used in linear algebra, physics, and most vector operations (especially when multiplying a matrix by a vector: `A · v`).

**Relationship :** A row vector can be converted to a column vector (and vice versa) using the **transpose** operation, denoted `vᵀ`.

```
If v = [ 2  5  7 ], then vᵀ = | 2 |
                               | 5 |
                               | 7 |
```
---
`3. Zero Vector :` 
A zero vector is the vector that has no magnitude and no direction. A zero vector is written as $\vec{0}$ or 0 and looks like:
- In 2D: (0, 0)
- In 3D: (0, 0, 0)

<b>Feature :</b>
```bash
1. Its magnitude is 0.
2. It does not point in any direction.
3. It acts like the additive identity for vectors. (Adding it to any vector leaves the vector unchanged.)
```
---

`4. Unit Vector :` 
Unit vectors are the vectors that have a magnitude (length) of exactly 1.

- It shows direction only, not size.
- Any vector can be converted into a unit vector by dividing it by its magnitude.
- Represented by the symbol '^' such as $\hat{a}$.


We define a unit vector in each 3-D axis as,
- Unit vector in the x-direction is i
- Unit vector in the y-direction is j
- Unit vector in the z-direction is k

Also, the magnitude of this vector is,

|i| = 1, |j| = 1, |k| = 1


`Unit Vector Formula :` The formula to calculate the unit vector is,

$$
\
\hat{v} = \frac{\vec{v}}{|\vec{v}|}
\
$$

Where:

- $ \hat{v}\ $ = Unit vector in the direction of \(\vec{v}\)
- $ \vec{v}\ $ = Given vector
- $ |\vec{v}|\ $ = Magnitude of the vector
</i>

<br>
---
`5. Equal Vectors `

**Equal vectors** are vectors that have the same magnitude and direction. In simple words, two vectors are said to be equal if they have the same length and direction; otherwise, they are unequal vectors.

<b>`Equal Vector Formula :`</b>
For Two Vectors A and B to be equal, the following two conditions must be met:

- Same Magnitude: Length of A must be equal to the length of B.
- Same Direction: Direction of A must be the same as the direction of B.

---
`6. Position Vector`

A **position vector** represents the location of a specific point in space **relative to a fixed origin** (usually denoted `O`).

`Definition :`

If a point `P` has coordinates `(x, y, z)`, then the position vector of `P`, denoted `r` or `OP→`, is:

```
    | x |
r = | y |
    | z |
```

`Example :`

If point `P = (4, -2, 6)`, then its position vector relative to the origin `(0,0,0)` is:

```
    | 4  |
r = | -2 |
    | 6  |
```
---

**`Vector Between Two Points`**

Position vectors are especially useful for finding the vector **between two points**. If `A` and `B` are points with position vectors `a` and `b`, the vector from `A` to `B` is:

```
AB→ = b - a
```

**Example:**
```
A = (1, 2),  B = (4, 6)
a = (1, 2),  b = (4, 6)

AB→ = b - a = (4-1, 6-2) = (3, 4)
```

---

`7. Negative Vector`

The **negative** of a vector `v`, written `-v`, is a vector with:
- The **same magnitude** as `v`
- The **exact opposite direction**

`How to Find It`

Negate (flip the sign of) every component of the vector.

```
If v = | v1 |        then  -v = | -v1 |
       | v2 |                   | -v2 |
       | v3 |                   | -v3 |
```

`Example`
```
v = (3, -4)
-v = (-3, 4)
```

`Key Properties`
- `|v| = |-v|` → magnitudes are equal
- `v + (-v) = 0` → a vector added to its negative gives the zero vector
- Geometrically, `-v` is the same arrow as `v`, just **pointing the opposite way**

`Visual Intuition`

If `v` points from the origin to the point `(3, -4)`, then `-v` points from the origin to `(-3, 4)` — the mirror image through the origin.

---


`Properties of Equal Vector`
```bash
1. If Two vectors A and B have same length and point in the same direction they are said to be equal else they would be unequal.

2. Equal Vectors are vectors with equal coordinates and same signs so equal vectors can be called as parallel vectors but the reverse may or may not be true.

3. Equal vectors have same components.

4. Position of the vectors does not affect the equality of vectors, Vectors are considered equal as long as their magnitude and direction matches, irrespective of where they are located in the coordinate system.

5. Equal Vector will still be equal if we add / subtract / divide / multiply both the vectors with the same quantity (can be scalar or vector ). For example say A = B and C is another vector then A - C = B - C.
```
--- 

**`Vector Operations`**

Vector operations are fundamental in linear algebra and are widely used in physics, computer graphics, machine learning, robotics, and engineering.


`1. Vector Addition`

Two vectors are added by adding their corresponding components.

`Formula`


$$
\vec{A}+\vec{B}=
\begin{bmatrix}a_1\\a_2\end{bmatrix}
+
\begin{bmatrix}b_1\\b_2\end{bmatrix} =
\begin{bmatrix}a_1+b_1\\a_2+b_2\end{bmatrix}
$$

**Example**

```
A = (2, 3)
B = (4, 1)

A + B = (6, 4)
```

---

`2. Vector Subtraction`

Subtract corresponding components of two vectors.

`Formula`

$$
\vec{A} - \vec{B} =
\begin{bmatrix}
a_1-b_1 \\
a_2-b_2
\end{bmatrix}
$$

**Example**

```
A = (5, 7)
B = (2, 3)

A - B = (3, 4)
```

---

`3. Scalar Multiplication`

Multiply every component of a vector by a scalar.

`Formula`

$$
k\vec{A} =
k
\begin{bmatrix}
a_1\\
a_2
\end{bmatrix} =
\begin{bmatrix}
ka_1\\
ka_2
\end{bmatrix}
$$

**Example**

```
k = 3
A = (2, 4)

3A = (6, 12)
```

---

`4. Magnitude (Length) of a Vector`

The magnitude represents the length of a vector.

`Formula`

$$
|\vec{A}|=\sqrt{a_1^2+a_2^2}
$$

**Example**

```
A = (3, 4)

|A| = √(3² + 4²)
    = √25
    = 5
```

---

`5. Unit Vector`

A unit vector has a magnitude of **1** and points in the same direction as the original vector.

`Formula`

$$
\hat{A}=\frac{\vec{A}}{|\vec{A}|}
$$

**Example**

```
A = (3, 4)

|A| = 5

Â = (3/5, 4/5)
```

---

`6. Dot Product (Scalar Product)`

The dot product measures how much one vector points in the direction of another.

`Formula`

$$
\vec{A}\cdot\vec{B} =
a_1b_1+a_2b_2
$$

`Example`

```
A = (2, 3)
B = (4, 5)

A · B
= (2×4) + (3×5)
= 8 + 15
= 23
```

`Properties`

- Result is a scalar.
- Commutative:

  ```
  A · B = B · A
  ```
- If
  ```
  A · B = 0
  ```
  then the vectors are perpendicular.

---

`7. Cross Product (3D Vectors Only)`

The cross product produces a vector perpendicular to both input vectors.

`Formula`

$$
\vec{A}\times\vec{B} =
\begin{vmatrix}
\hat{i} & \hat{j} & \hat{k}\\
a_1&a_2&a_3\\
b_1&b_2&b_3
\end{vmatrix}
$$

`Example`

```
A = (1, 0, 0)
B = (0, 1, 0)

A × B = (0, 0, 1)
```

---

## `3. Introduction to Matrices`
Matrices are rectangular arrays of numbers, symbols, or characters where all of these elements are arranged in each row and column.

- A matrix is identified by its order, which is given in the form of rows ⨯ columns, and the location of each element is given by the row and column it belongs to.
- A matrix is represented as ([P]m⨯n), where P is the matrix, m is the number of rows, and n is the number of columns.

<b> `Example` </b>

`1. Matrix A (2×2) :`

A = $$\begin{bmatrix}
1 & 2\\
3 & 4
\end{bmatrix}_{2\times2}$$

`2. Matrix B (3×3) :`

B = $$\begin{bmatrix}
1 & -1 & 2\\
3 & 2 & 6\\
4 & -2 & 5
\end{bmatrix}_{3\times3}$$

Here, A is a 2×2 matrix (2 rows and 2 columns) and B is a 3×3 matrix (3 rows and 3 columns).
<hr>
---

### **`Order of Matrix :`**

The order of a matrix refers to its dimensions, i.e., the number of rows and columns. If a matrix has m rows and n columns, its order is denoted as m × n.
- For example, a matrix with 5 rows and 3 columns has an order of 5 × 3.

<b>`How to Determine the Order of Matrix?`</b>
The order of the matrix is determined by the number of rows and columns present in the matrix.
<br>
For example, if a matrix has "m" rows and "n" columns, then the order of the matrix is said to be "m × n."

<b>`Example`</b>
<i>
```bash
1. Example :

P = [ 2 4 6 8 ]
- We can see that the matrix P has 1 row and 4 columns. So, the order of the matrix P is written as "1 × 4."

2. Example :

Q = | a b c |
    | d e f |
- We can see that the matrix Q has 2 rows and 3 columns. So, the order of the matrix Q is written as "2 × 3."

3. Example :

R = | 1  -1   2 |
    | 3   2   6 |
    | 4  -2   5 |
- We can see that the matrix R has 3 rows and 3 columns. So, the order of the matrix R is written as "3 × 3."
```
</i>
---

### **`Type of Matrices Based on Order of Matrix`**

The order of a matrix indicates its dimension and also defines the various types of matrices. The following are some different matrices that are classified based on the order of a matrix.

---

`1. Singleton Matrix :` 
A singleton matrix is defined as a matrix that has only one element, i.e., it has only one row and one column. So, the order of a singleton matrix is "1 × 1"
- Matrix given below is a singleton matrix.

        A = [ 23 ]

---

`2. Row Matrix :` 
A row matrix is defined as a matrix that has only one row. A matrix "A = [aij]" is said to be a row matrix if the order of the matrix is "1 × n"
- Matrix given below is a row matrix of order "1 × 3"

        B = [ -1 0 1 ]

---

`3. Column Matrix :` 
A column matrix is defined as a matrix that has only one column. The matrix "A = [aij]" is said to be a column matrix if the order of the matrix is "m × 1"
- Matrix given below is a row matrix of order "4 × 1"

            | p |
            | q |
      C =   | r |
            | s |

---

`4. Rectangular Matrix :` 
A rectangular matrix is defined as a matrix that does not have an equal number of rows and columns. The order of a rectangular matrix that has "m" rows and "n" columns is "m × n" 
- Matrix given below is a row matrix of order "2 × 3"

        D = | 12 14 16 |
            | 6   7  8 |

---

`5. Square Matrix :` 
A square matrix is defined as a matrix that has an equal number of rows and columns. The order of a square matrix that has "n" rows and "n" columns is "n × n" 
- Matrix given below is a row matrix of order "2 × 2"

        E = | 3  6 |
            | 9 15 |

---

`6. Diagonal Matrix :` 
A diagonal matrix is a square matrix in which all the elements except the main diagonal are 0.
- Matrix given below is a digonal matrix of order "3 × 3"
```bash
        F = | 5 0 0 |
            | 0 3 0 |
            | 0 0 7 | 

- Key Poinst :
1. Must be a square matrix.
2. Non-diagonal elements are all 0.
3. Diagonal elements can be any number (including 0).           
```
---

`7. Scalar Matrix :` 
A scalar matrix is a diagonal matrix in which all the diagonal elements are equal.
- Matrix given below is a scalar matrix of order "3 × 3"
```bash
        G = | 4 0 0 |
            | 0 4 0 |
            | 0 0 4 |

- Key Points:

1. Must be a square matrix.
2. All off-diagonal elements are 0.
3. All diagonal elements are the same.
```
---

`8. Identity Matrix ( Unit Matrix ) :` 
A square matrix in which elements in the diagonal are all 1 and rest are all zero is called an identity matrix.
- Matrix given below is a identity matrix of order "3 × 3"
```bash
        H = | 1 0 0 |
            | 0 1 0 |
            | 0 0 1 |
```
---

`9. Zero Matrix :` 
A matrix is said to be zero matrix or null matrix if all its elements are zero.
- Matrix given below is a zero matrix of order "3 × 3"
```bash
        I = | 0 0 0 |
            | 0 0 0 |
            | 0 0 0 |
```
---

<b>`Important Points on Order of Matrix`</b>
```bash
1. The first number in the order of a matrix will always represent the number of rows in the matrix, while the second number represents the number of columns in the matrix.

2. The addition or subtraction of any two matrices is possible if the order of the two matrices is the same.

3. Multiplication of any two matrices is possible only when the number of columns in the first matrix is equal to the number of rows in the second matrix.

4. If the order of a matrix is "m × n," then the order of its transpose matrix will be "n × m," where a transpose matrix is formed by changing the rows of a matrix into columns and its columns into rows.
```
---

### **`Operation on Matrix`**

**Matrix Operations** are basic calculations performed on matrices to solve problems or manipulate their structure. Common operations include:

- Addition: Add two matrices of the same size.
- Subtraction: Subtract two matrices of the same size.
- Scalar Multiplication: Multiply each element of a matrix by a constant.
- Matrix Multiplication: Multiply two matrices to create a new matrix.
- Transpose: Flip the rows and columns of a matrix.
- Inverse: Find the inverse of a Matrix.
---

**`1. Matrix Addition`**

**Matrix addition** is the process of adding two matrices by adding their corresponding elements. Matrix addition is one of the most fundamental operations in linear algebra.

> **Note:** Two matrices can only be added if they have the **same order** (same number of rows and columns).

---

If

$$
A=[a_{ij}]
$$

and

$$
B=[b_{ij}]
$$

are matrices of the same order, then

$$
A+B=[a_{ij}+b_{ij}]
$$

---

**`Condition for Matrix Addition`**

Two matrices can be added only when:

- They have the same number of rows.
- They have the same number of columns.

If the orders are different, matrix addition is **not defined**.

---

**Example**

Let

$$
A =\begin{bmatrix}
1 & 2\\
3 & 4
\end{bmatrix}
$$

and

$$
B =\begin{bmatrix}
5 & 6\\
7 & 8
\end{bmatrix}
$$

Then,

$$
A+B = \begin{bmatrix}
1+5 & 2+6\\
3+7 & 4+8
\end{bmatrix} =
\begin{bmatrix}
6 & 8\\
10 & 12
\end{bmatrix}
$$

---

**`Properties of Matrix Addition`**

`1. Closure Property`

If matrices have the same order,

$$
A+B
$$

is also a matrix of the same order.

`2. Commutative Property`

$$
A+B=B+A
$$

`3. Associative Property`

$$
(A+B)+C=A+(B+C)
$$

`4. Additive Identity`

$$
A+O=A
$$

where $O$ is the zero matrix.

`5. Additive Inverse`

$$
A+(-A)=O
$$

---

**`2. Matrix Subtraction`**

**Matrix subtraction** is the process of subtracting the corresponding elements of one matrix from another.

> **Note:** Matrix subtraction is possible only when both matrices have the same order.

---

If

$$
A=[a_{ij}]
$$

and

$$
B=[b_{ij}]
$$

have the same order, then

$$
A-B=[a_{ij}-b_{ij}]
$$

---

**Condition**

Matrices must have the same number of rows and columns.

---

**Example**

$$
A=
\begin{bmatrix}
8 & 7\\
6 & 5
\end{bmatrix}
$$

$$
B=
\begin{bmatrix}
2 & 3\\
4 & 1
\end{bmatrix}
$$

$$
A-B=
\begin{bmatrix}
6 & 4\\
2 & 4
\end{bmatrix}
$$

---

**`Properties`**

`1. Not Commutative`

$$
A-B \neq B-A
$$

`2. Not Associative`

$$
(A-B)-C \neq A-(B-C)
$$

`3. Identity Property`

$$
A-O=A
$$

`4. Self Subtraction`

$$
A-A=O
$$

where $O$ is the zero matrix.

---

### `3. Multiplying Matrices`
Matrix multiplication is a binary operation that produces a new matrix from two matrices.
- For multiplication, the number of columns in the first matrix must equal the number of rows in the second matrix. 
- The resulting matrix (matrix product) has the same number of rows as the first matrix and the same number of columns as the second matrix.
- For example, If matrix A is of order m × p and matrix B is of order p × n, then their product AB exists and is of order m × n.

`Rules and Conditions for Matrix Multiplication`
```bash
1. If "A = [aij]m×n" and "B = [bij]n×o" are two matrices, then the product of A and B is denoted as AB, whose order is "m × o".

2. Matrix multiplication is not commutative, i.e., AB ≠ BA, or, in simple words, the product of A and B matrices is AB, and AB is not equal to BA; it is even possible that AB exists but BA does not exist.

3. Compatibility Conditions for Matrix Multiplication : We can multiply two matrices if the number of columns in the 1st matrix is equal to the number of rows in the 2nd matrix, otherwise, the given matrices cannot be multiplied.

Example:
- A 2×3 matrix can be multiplied by a 3×2 matrix, resulting in a 2×2 matrix.
- A 3×3 matrix cannot be multiplied by a 4×2 matrix because their dimensions are incompatible.

4. Special Properties of Matrix Multiplication : 
- Both AB and BA matrix multiplication are defined if both A and B are square matrices.
- One of the matrices doesn't need to be a zero matrix if the product of two matrices A and B is zero.
- French mathematicianJacques Philippe Marie Binet was the first to perform matrix multiplication in 1812.
```

`Step-by-Step Process for Matrix Multiplication :`
To multiply two matrices, A and B, ensure that the number of columns in A equals the number of rows in B.
```bash
1. Calculate Elements: Multiply each element in a row of the first matrix by the corresponding element in a column of the second matrix, and sum these products to compute each element of the product matrix. Repeat this process for all rows and columns.

2. Form the Product Matrix: Place the computed elements in their respective positions to construct the resulting matrix.'
```

`Properties of multiplication of matrices :`
```bash
1.  The associative law For any three matrices A, B and C. We have
(AB) C = A (BC), whenever both sides of the equality are defined.

2. The distributive law For three matrices A, B and C.
- A (B+C) = AB + AC
- (A+B) C = AC + BC, whenever both sides of equality are defined.

3. The existence of multiplicative identity For every square matrix A, there
exist an identity matrix of same order such that IA = AI = A.
```
`Example :`
```bash
A = | 1 2 |
    | 3 4 |

B = | 5 6 |
    | 7 8 |

A × B = | (1×5 + 2×7)   (1×6 + 2×8) |
        | (3×5 + 4×7)   (3×6 + 4×8) |

      = | 19 22 |
        | 43 50 |
```

### `4. Scalar Multiplication of Matrices`
Scalar multiplication is performed by multiplying every element of a matrix by a scalar (constant).

**Example:**

A = | 1 2 |
    | 3 4 |

Scalar = 3

3 × A = | 3×1  3×2 |
        | 3×3  3×4 |

      = | 3  6 |
        | 9 12 |

---

### `4. Transpose`
Transpose of a matrix is a new matrix that is obtained by swapping the rows and columns of the given matrix or vice versa, i.e., for the given matrix, the elements in rows are interchanged with the elements in columns.

- For any given matrix A, its transpose is denoted as AT, or Aᵀ.
- To find Aᵀ, take each row of A and rewrite it as a column.

<br>

`Transpose of a Matrix (Aᵀ or AT) :` The transpose of a matrix is obtained by interchanging its rows and columns.

**Example:**
```bash
A = | 1 2 3 |
    | 4 5 6 | 2 X 3

Aᵀ = | 1 4 |
     | 2 5 |
     | 3 6 | 3 X 2
```
<br>

`Order of Transpose Matrix :` The order of a matrix represents the number of rows and columns it contains, written as m × n, where m is the number of rows, and n is the number of columns.

For any matrix **A<sub>m×n</sub>**:

- The transpose of **A**, denoted as **Aᵀ** (or **AT**), is obtained by interchanging its rows and columns.
- If **A** is of order **m × n**, then **Aᵀ** is of order **n × m** (i.e., **Aᵀ** has **n** rows and **m** columns).

`Example`
```bash
A (2 × 3)

A = | 1 2 3 |
    | 4 5 6 |

Aᵀ (3 × 2)

Aᵀ =  | 1 4 |
      | 2 5 |
      | 3 6 |
```

