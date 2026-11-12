# Linear Algebra
Linear Algebra is the branch of mathematics that focuses on the study of vectors, vector spaces, matrices and linear transformations.

- Deals with linear equations, linear functions and their representations through matrices and determinants.
- Used in quantum mechanics, computer graphics and optimization
- Basic concept for machine learning and data science.
<br>

### <b>`Why Learn Linear Algebra?`</b>
```bash
1. Machine Learning & AI: Every neural network, regression model and dimensionality reduction algorithm (PCA, SVD) is built on linear algebra operations.

2. Computer Graphics: Rotations, scaling and 3D projections in games and animation are all matrix transformations.

3. Physics & Engineering: Quantum mechanics, structural analysis and control systems all rely on eigenvalues and vector spaces.

4. Data Science: Working with high-dimensional datasets, covariance matrices and feature transformations requires fluency in linear algebra.
```

### `Uses of Linear Algebra`
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

- $$ \hat{v}\ $$ = Unit vector in the direction of \(\vec{v}\)
- $$ \vec{v}\ $$ = Given vector
- $$ |\vec{v}|\ $$ = Magnitude of the vector
</i>

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

### **`1. Vector Components`**

A **vector** is a mathematical quantity that has both **magnitude** and **direction**.

A vector can be represented geometrically as an arrow or algebraically as an ordered collection of numbers called its **components**.

For example,

$$
\vec{v} =
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

contains two components:

- $3$ → component along the $x$-axis
- $4$ → component along the $y$-axis

Vector components are fundamental in Linear Algebra because they allow us to perform operations such as:

- Vector addition
- Vector subtraction
- Scalar multiplication
- Dot product
- Cross product
- Finding magnitude
- Finding direction
- Representing points and movements
- Solving physical and engineering problems

---

**`What are Vector Components?`**

The **components of a vector** are the numerical values that describe the vector along different coordinate axes.

For a two-dimensional vector,

$$
\vec{v} =
\begin{bmatrix}
v_x\\
v_y
\end{bmatrix}
$$

where

- $v_x$ = component along the $x$-axis
- $v_y$ = component along the $y$-axis

For a three-dimensional vector,

$$
\vec{v} =
\begin{bmatrix}
v_x\\
v_y\\
v_z
\end{bmatrix}
$$

where

- $v_x$ = $x$-component
- $v_y$ = $y$-component
- $v_z$ = $z$-component

---

**`Components in 2D`**

A vector in two-dimensional space has two components.

$$
\vec{v} =
\begin{bmatrix}
x\\
y
\end{bmatrix}
$$

It can also be written as

$$
\vec{v}=x\hat{i}+y\hat{j}
$$

where

- $\hat{i}$ = unit vector along the $x$-axis
- $\hat{j}$ = unit vector along the $y$-axis

---

**Example**

Consider

$$
\vec{v} =
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

Then

$$
\vec{v}=3\hat{i}+4\hat{j}
$$

Therefore,

$$
v_x=3
$$

and

$$
v_y=4
$$

---

**`Components in 3D`**

A vector in three-dimensional space has three components.

$$
\vec{v} =
\begin{bmatrix}
x\\
y\\
z
\end{bmatrix}
$$

or

$$
\vec{v}=x\hat{i}+y\hat{j}+z\hat{k}
$$

where

- $\hat{i}$ = unit vector along the $x$-axis
- $\hat{j}$ = unit vector along the $y$-axis
- $\hat{k}$ = unit vector along the $z$-axis

**Example**

$$
\vec{v} =
\begin{bmatrix}
2\\
3\\
5
\end{bmatrix}
$$

Therefore,

$$
\vec{v}=2\hat{i}+3\hat{j}+5\hat{k}
$$

The components are

$$
v_x=2
$$

$$
v_y=3
$$

$$
v_z=5
$$

---

**`Horizontal and Vertical Components`**

In a two-dimensional coordinate system, a vector can be separated into two perpendicular components:

- Horizontal component
- Vertical component

If a vector has magnitude $V$ and makes an angle $\theta$ with the positive $x$-axis, then:

$$
V_x=V\cos\theta
$$

and

$$
V_y=V\sin\theta
$$

Therefore,

$$
\boxed{
\vec{V} =
V\cos\theta\hat{i} +
V\sin\theta\hat{j}
}
$$

---

**Example**

Suppose a vector has magnitude

$$
V=10
$$

and makes an angle

$$
\theta=30^\circ
$$

with the positive $x$-axis.

The horizontal component is

$$
V_x =
10\cos30^\circ
$$

Since

$$
\cos30^\circ=\frac{\sqrt{3}}{2}
$$

we get

$$
V_x=5\sqrt{3}
$$

The vertical component is

$$
V_y =
10\sin30^\circ
$$

Since

$$
\sin30^\circ=\frac12
$$

we get

$$
V_y=5
$$

Therefore,

$$
\vec{V} =
5\sqrt{3}\hat{i} +
5\hat{j}
$$

---

**`Finding Components from Initial and Terminal Points`**

Suppose a vector starts at

$$
P(x_1,y_1)
$$

and ends at

$$
Q(x_2,y_2)
$$

Then the vector components are obtained by subtracting the coordinates of the initial point from the terminal point.

$$
\boxed{
\vec{PQ} =
\begin{bmatrix}
x_2-x_1\\
y_2-y_1
\end{bmatrix}
}
$$

---

**Example**

Let

$$
P=(2,3)
$$

and

$$
Q=(7,8)
$$

Then

$$
\vec{PQ} =
\begin{bmatrix}
7-2\\
8-3
\end{bmatrix}
$$

Therefore,

$$
\vec{PQ} =
\begin{bmatrix}
5\\
5
\end{bmatrix}
$$

So the vector has components

$$
(5,5)
$$

---

**`Vector Components in 3D`**

Suppose

$$
P(x_1,y_1,z_1)
$$

is the initial point and

$$
Q(x_2,y_2,z_2)
$$

is the terminal point.

Then

$$
\boxed{
\vec{PQ} =
\begin{bmatrix}
x_2-x_1\\
y_2-y_1\\
z_2-z_1
\end{bmatrix}
}
$$

---

**Example**

Let

$$
P=(1,2,3)
$$

and

$$
Q=(5,7,9)
$$

Then

$$
\vec{PQ} =
\begin{bmatrix}
5-1\\
7-2\\
9-3
\end{bmatrix}
$$

Therefore,

$$
\vec{PQ} =
\begin{bmatrix}
4\\
5\\
6
\end{bmatrix}
$$

---

**`Magnitude from Vector Components`**

The magnitude of a vector can be calculated directly from its components.

For a 2D vector

$$
\vec{v} =
\begin{bmatrix}
x\\
y
\end{bmatrix}
$$

the magnitude is

$$
\boxed{
|\vec{v}|=\sqrt{x^2+y^2}
}
$$

---

**Example**

For

$$
\vec{v} =
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

we have

$$
|\vec{v}| =
\sqrt{3^2+4^2}
$$

$$
= \sqrt{9+16}
$$

$$
=\sqrt{25}
$$

$$
=5
$$

---

**`Magnitude of a 3D Vector`**

For

$$
\vec{v} =
\begin{bmatrix}
x\\
y\\
z
\end{bmatrix}
$$

the magnitude is

$$
\boxed{
|\vec{v}| =
\sqrt{x^2+y^2+z^2}
}
$$

**Example**

For

$$
\vec{v} =
\begin{bmatrix}
2\\
3\\
6
\end{bmatrix}
$$

$$
|\vec{v}| =
\sqrt{2^2+3^2+6^2}
$$

$$
= \sqrt{4+9+36}
$$

$$
=\sqrt{49}
$$

$$
=7
$$

---

**`Direction from Vector Components`**

For a 2D vector

$$
\vec{v} =
\begin{bmatrix}
x\\
y
\end{bmatrix}
$$

the direction angle $\theta$ can be calculated using

$$
\boxed{
\theta=\tan^{-1}\left(\frac{y}{x}\right)
}
$$

However, when determining the correct quadrant, it is better to use the two-argument function

$$
\theta=\mathrm{atan2}(y,x)
$$

because it considers the signs of both components.

---

**Example**

For

$$
\vec{v} =
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

$$
\theta =
\tan^{-1}\left(\frac43\right)
$$

Therefore,

$$
\theta\approx53.13^\circ
$$

---

**`Unit Vector from Components`**

A **Unit Vector** is a vector whose magnitude is exactly $1$.

For a non-zero vector $\vec{v}$, its unit vector is

$$
\boxed{
\hat{v} =
\frac{\vec{v}}{|\vec{v}|}
}
$$

---

**Example**

Let

$$
\vec{v} =
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

We already know

$$
|\vec{v}|=5
$$

Therefore,

$$
\hat{v} =
\frac15
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

Thus,

$$
\boxed{
\hat{v} =
\begin{bmatrix}
\frac35\\
\frac45
\end{bmatrix}
}
$$

The magnitude of this vector is $1$.

---

**`Vector Components and Addition`**

Vector addition is performed by adding corresponding components.

Suppose

$$
\vec{u} =
\begin{bmatrix}
u_x\\
u_y
\end{bmatrix}
$$

and

$$
\vec{v} =
\begin{bmatrix}
v_x\\
v_y
\end{bmatrix}
$$

Then

$$
\boxed{
\vec{u}+\vec{v} =
\begin{bmatrix}
u_x+v_x\\
u_y+v_y
\end{bmatrix}
}
$$

---

**Example**

$$
\vec{u} =
\begin{bmatrix}
2\\
3
\end{bmatrix}
$$

$$
\vec{v} =
\begin{bmatrix}
4\\
5
\end{bmatrix}
$$

Then

$$
\vec{u}+\vec{v} =
\begin{bmatrix}
2+4\\
3+5
\end{bmatrix}
$$

$$
= \begin{bmatrix}
6\\
8
\end{bmatrix}
$$

---

**`Vector Components and Subtraction`**

Vector subtraction is also performed component by component.

$$
\boxed{
\vec{u}-\vec{v} =
\begin{bmatrix}
u_x-v_x\\
u_y-v_y
\end{bmatrix}
}
$$

**Example**

$$
\vec{u} =
\begin{bmatrix}
7\\
5
\end{bmatrix}
$$

$$
\vec{v} =
\begin{bmatrix}
2\\
3
\end{bmatrix}
$$

Therefore,

$$
\vec{u}-\vec{v} =
\begin{bmatrix}
7-2\\
5-3
\end{bmatrix}
$$

$$
= \begin{bmatrix}
5\\
2
\end{bmatrix}
$$

---

**`Scalar Multiplication of Components`**

When a vector is multiplied by a scalar, every component is multiplied by that scalar.

$$
k
\begin{bmatrix}
x\\
y
\end{bmatrix} =
\begin{bmatrix}
kx\\
ky
\end{bmatrix}
$$

**Example**

$$
3
\begin{bmatrix}
2\\
4
\end{bmatrix} =
\begin{bmatrix}
6\\
12
\end{bmatrix}
$$

---

**`Vector Components and Dot Product`**

The **dot product** of two vectors is calculated using their corresponding components.

For

$$
\vec{u} =
\begin{bmatrix}
u_x\\
u_y
\end{bmatrix}
$$

and

$$
\vec{v} =
\begin{bmatrix}
v_x\\
v_y
\end{bmatrix}
$$

the dot product is

$$
\boxed{
\vec{u}\cdot\vec{v} =
u_xv_x+u_yv_y
}
$$

For three-dimensional vectors,

$$
\boxed{
\vec{u}\cdot\vec{v} =
u_xv_x+u_yv_y+u_zv_z
}
$$

---

**Example**

$$
\vec{u} =
\begin{bmatrix}
2\\
3
\end{bmatrix}
$$

and

$$
\vec{v} =
\begin{bmatrix}
4\\
5
\end{bmatrix}
$$

Then

$$
\vec{u}\cdot\vec{v} =
(2)(4)+(3)(5)
$$

$$
=8+15
$$

$$
=23
$$

---

**`Components and Angle Between Vectors`**

The dot product can also be used to find the angle between two vectors.

$$
\boxed{
\vec{u}\cdot\vec{v} =
|\vec{u}||\vec{v}|\cos\theta
}
$$

Therefore,

$$
\boxed{
\cos\theta =
\frac{\vec{u}\cdot\vec{v}}
{|\vec{u}||\vec{v}|}
}
$$

and

$$
\boxed{
\theta =
\cos^{-1}
\left(
\frac{\vec{u}\cdot\vec{v}}
{|\vec{u}||\vec{v}|}
\right)
}
$$

---

**`Orthogonal Vectors`**

Two vectors are **orthogonal** if they are perpendicular to each other.

For orthogonal vectors,

$$
\vec{u}\cdot\vec{v}=0
$$

**Example**

$$
\vec{u} =
\begin{bmatrix}
1\\
0
\end{bmatrix}
$$

and

$$
\vec{v} =
\begin{bmatrix}
0\\
1
\end{bmatrix}
$$

Then

$$
\vec{u}\cdot\vec{v} =
(1)(0)+(0)(1)
=0
$$

Therefore, the vectors are orthogonal.

---

**`Components and Linear Combination`**

A vector can be represented as a linear combination of basis vectors.

In $\mathbb{R}^2$,

$$
\vec{v} =
x\hat{i}+y\hat{j}
$$

where $x$ and $y$ are the components.

For example,

$$
\vec{v} =
\begin{bmatrix}
3\\
5
\end{bmatrix}
$$

can be written as

$$
\vec{v}=3\hat{i}+5\hat{j}
$$

Similarly, in $\mathbb{R}^3$,

$$
\vec{v} =
x\hat{i}+y\hat{j}+z\hat{k}
$$

---

**`Negative Components`**

A component can be positive, negative, or zero.

`Positive Component`

$$
v_x>0
$$

means the vector has a component in the positive $x$ direction.

`Negative Component`

$$
v_x<0
$$

means the vector has a component in the negative $x$ direction.

`Zero Component`

$$
v_x=0
$$

means there is no component in the $x$ direction.

---

**`Components and Quadrants`**

For a two-dimensional vector, the signs of its components determine its quadrant.

| Quadrant | $x$ Component | $y$ Component |
|---|---:|---:|
| I | $+$ | $+$ |
| II | $-$ | $+$ |
| III | $-$ | $-$ |
| IV | $+$ | $-$ |

**Example**

If

$$
\vec{v} =
\begin{bmatrix}
-3\\
4
\end{bmatrix}
$$

then

$$
x<0
$$

and

$$
y>0
$$

Therefore, the vector lies in **Quadrant II**.

---

**`Components of the Zero Vector`**

The zero vector has every component equal to zero.

In $\mathbb{R}^2$,

$$
\vec{0} =
\begin{bmatrix}
0\\
0
\end{bmatrix}
$$

In $\mathbb{R}^3$,

$$
\vec{0} =
\begin{bmatrix}
0\\
0\\
0
\end{bmatrix}
$$

Its magnitude is

$$
|\vec{0}|=0
$$

The zero vector does not have a unique direction.

---

**`Vector Components in Different Dimensions`**

The number of components depends on the dimension of the vector space.

| Vector Space | Number of Components |
|---|---:|
| $\mathbb{R}$ | 1 |
| $\mathbb{R}^2$ | 2 |
| $\mathbb{R}^3$ | 3 |
| $\mathbb{R}^4$ | 4 |
| $\mathbb{R}^n$ | $n$ |

For example,

$$
\vec{v}\in\mathbb{R}^4
$$

has the form

$$
\vec{v} =
\begin{bmatrix}
v_1\\
v_2\\
v_3\\
v_4
\end{bmatrix}
$$

---

**`Components of a Vector vs Magnitude`**

It is important to distinguish between **components** and **magnitude**.

For

$$
\vec{v} =
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

the components are

$$
3,\quad4
$$

while the magnitude is

$$
|\vec{v}|=5
$$

Therefore,

> **Components describe the vector along coordinate directions, while magnitude describes the overall length of the vector.**

---

**`Components and Direction Cosines in 3D`**

For a three-dimensional vector

$$
\vec{v} =
\begin{bmatrix}
x\\
y\\
z
\end{bmatrix}
$$

with magnitude

$$
|\vec{v}| =
\sqrt{x^2+y^2+z^2}
$$

the direction cosines are

$$
\cos\alpha=\frac{x}{|\vec{v}|}
$$

$$
\cos\beta=\frac{y}{|\vec{v}|}
$$

$$
\cos\gamma=\frac{z}{|\vec{v}|}
$$

where

- $\alpha$ = angle with the $x$-axis
- $\beta$ = angle with the $y$-axis
- $\gamma$ = angle with the $z$-axis

They satisfy

$$
\boxed{
\cos^2\alpha+\cos^2\beta+\cos^2\gamma=1
}
$$

---

**Example**

Given

$$
\vec{v} =
\begin{bmatrix}
2\\
3\\
6
\end{bmatrix}
$$

find:

1. Components
2. Magnitude
3. Unit vector

`Step 1: Components`

The components are

$$
v_x=2,\qquad
v_y=3,\qquad
v_z=6
$$

---

`Step 2: Magnitude`

$$
|\vec{v}| =
\sqrt{2^2+3^2+6^2}
$$

$$
= \sqrt{4+9+36}
$$

$$
=\sqrt{49}
$$

$$
=7
$$

---

`Step 3: Unit Vector`

$$
\hat{v} =
\frac{\vec{v}}{|\vec{v}|}
$$

Therefore,

$$
\hat{v} =
\frac17
\begin{bmatrix}
2\\
3\\
6
\end{bmatrix}
$$

$$
\boxed{
\hat{v} =
\begin{bmatrix}
\frac27\\
\frac37\\
\frac67
\end{bmatrix}
}
$$

---

**`Important Formulas`**

`2D Vector`

$$
\boxed{
\vec{v} =
\begin{bmatrix}
x\\
y
\end{bmatrix}
}
$$

---

`3D Vector`

$$
\boxed{
\vec{v} =
\begin{bmatrix}
x\\
y\\
z
\end{bmatrix}
}
$$

---

`Vector from Two Points`

$$
\boxed{
\vec{PQ} =
\begin{bmatrix}
x_2-x_1\\
y_2-y_1
\end{bmatrix}
}
$$

---

`Magnitude of 2D Vector`

$$
\boxed{
|\vec{v}|=\sqrt{x^2+y^2}
}
$$

---

`Magnitude of 3D Vector`

$$
\boxed{
|\vec{v}|=\sqrt{x^2+y^2+z^2}
}
$$

---

`Unit Vector`

$$
\boxed{
\hat{v} =
\frac{\vec{v}}{|\vec{v}|}
}
$$

---

**`Components from Magnitude and Angle`**

$$
\boxed{
V_x=V\cos\theta
}
$$

$$
\boxed{
V_y=V\sin\theta
}
$$

---

**`Direction Angle`**

$$
\boxed{
\theta =
\tan^{-1}
\left(
\frac{y}{x}
\right)
}
$$

For correct quadrant handling:

$$
\boxed{
\theta=\mathrm{atan2}(y,x)
}
$$

---

**`Dot Product`**

$$
\boxed{
\vec{u}\cdot\vec{v} =
u_xv_x+u_yv_y
}
$$

---

**`Angle Between Vectors`**

$$
\boxed{
\theta =
\cos^{-1}
\left(
\frac{\vec{u}\cdot\vec{v}}
{|\vec{u}||\vec{v}|}
\right)
}
$$

---

### **`2. Vector Projection`**

**Vector Projection** is the process of finding the component of one vector that lies in the direction of another vector.

In simple words, projection tells us:

> **How much of one vector points in the direction of another vector.**

Vector projection is closely related to the **dot product** and is an important concept in Linear Algebra.

It is used in:

- Geometry
- Physics
- Computer Graphics
- Robotics
- Machine Learning
- Data Science
- Signal Processing
- Computer Vision

---

**`What is Vector Projection?`**

Suppose we have two vectors:

$$
\vec{a}
$$

and

$$
\vec{b}
$$

We want to find the projection of $\vec{a}$ onto $\vec{b}$.

The projection represents the part of $\vec{a}$ that points in the direction of $\vec{b}$.

It is written as:

$$
\mathrm{proj}_{\vec{b}}\vec{a}
$$

and is read as:

> **Projection of $\vec{a}$ onto $\vec{b}$.**

---

**`Geometrical Meaning`**

Suppose $\vec{a}$ and $\vec{b}$ form an angle $\theta$.

The projection of $\vec{a}$ onto $\vec{b}$ is the "shadow" of $\vec{a}$ on the direction of $\vec{b}$.

The length of this projection is:

$$
|\vec{a}|\cos\theta
$$

Therefore,

$$
\boxed{
\text{Scalar Projection} =
|\vec{a}|\cos\theta
}
$$

The direction of the projection is along $\vec{b}$.

---

**`Scalar Projection`**

The **Scalar Projection** gives only the length of the projection.

The scalar projection of $\vec{a}$ onto $\vec{b}$ is:

$$
\boxed{
\mathrm{comp}_{\vec{b}}\vec{a} =
\frac{\vec{a}\cdot\vec{b}}
{|\vec{b}|}
}
$$

Using the dot product formula:

$$
\vec{a}\cdot\vec{b} =
|\vec{a}||\vec{b}|\cos\theta
$$

we get:

$$
\mathrm{comp}_{\vec{b}}\vec{a} =
|\vec{a}|\cos\theta
$$

---

**`Vector Projection`**

The **Vector Projection** gives both the magnitude and direction of the projected vector.

The formula is:

$$
\boxed{
\mathrm{proj}_{\vec{b}}\vec{a} =
\frac{\vec{a}\cdot\vec{b}}
{|\vec{b}|^2}
\vec{b}
}
$$

Since

$$
|\vec{b}|^2 =
\vec{b}\cdot\vec{b}
$$

we can also write:

$$
\boxed{
\mathrm{proj}_{\vec{b}}\vec{a} =
\frac{\vec{a}\cdot\vec{b}}
{\vec{b}\cdot\vec{b}}
\vec{b}
}
$$

---

**`Why Do We Divide by $|\vec{b}|^2$?`**

This is an important part of understanding projection.

Suppose we want a vector in the direction of $\vec{b}$.

Any vector in the direction of $\vec{b}$ can be written as:

$$
k\vec{b}
$$

for some scalar $k$.

The projection must have the correct component of $\vec{a}$ along $\vec{b}$.

The required scalar is:

$$
k=
\frac{\vec{a}\cdot\vec{b}}
{|\vec{b}|^2}
$$

Therefore,

$$
\mathrm{proj}_{\vec{b}}\vec{a} =
k\vec{b}
$$

which gives:

$$
\boxed{
\mathrm{proj}_{\vec{b}}\vec{a} =
\frac{\vec{a}\cdot\vec{b}}
{|\vec{b}|^2}
\vec{b}
}
$$

---

**Example of Vector Projection**

Let

$$
\vec{a} =
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

and

$$
\vec{b} =
\begin{bmatrix}
1\\
0
\end{bmatrix}
$$

Find the projection of $\vec{a}$ onto $\vec{b}$.

---

`Step 1: Find the Dot Product`

$$
\vec{a}\cdot\vec{b} =
(3)(1)+(4)(0)
$$

$$
=3
$$

---

`Step 2: Find $|\vec{b}|^2$`

$$
|\vec{b}|^2 =
1^2+0^2
$$

$$
=1
$$

---

`Step 3: Apply the Projection Formula`

$$
\mathrm{proj}_{\vec{b}}\vec{a} =
\frac{3}{1}
\begin{bmatrix}
1\\
0
\end{bmatrix}
$$

Therefore,

$$
\boxed{
\mathrm{proj}_{\vec{b}}\vec{a} =
\begin{bmatrix}
3\\
0
\end{bmatrix}
}
$$

The vector $\vec{a}$ has a horizontal component of $3$ in the direction of $\vec{b}$.

---

**Example**

Let

$$
\vec{a} =
\begin{bmatrix}
2\\
3
\end{bmatrix}
$$

and

$$
\vec{b} =
\begin{bmatrix}
4\\
1
\end{bmatrix}
$$

Find the projection of $\vec{a}$ onto $\vec{b}$.

---

`Step 1: Calculate the Dot Product`

$$
\vec{a}\cdot\vec{b} =
(2)(4)+(3)(1)
$$

$$
=8+3
$$

$$
=11
$$

---

`Step 2: Calculate $|\vec{b}|^2$`

$$
|\vec{b}|^2 =
4^2+1^2
$$

$$
=16+1
$$

$$
=17
$$

---

`Step 3: Apply the Formula`

$$
\mathrm{proj}_{\vec{b}}\vec{a} =
\frac{11}{17}
\begin{bmatrix}
4\\
1
\end{bmatrix}
$$

Therefore,

$$
\boxed{
\mathrm{proj}_{\vec{b}}\vec{a} =
\begin{bmatrix}
\frac{44}{17}\\
\frac{11}{17}
\end{bmatrix}
}
$$

---

**`Scalar Projection vs Vector Projection`**

These two concepts are related but different.

| Scalar Projection | Vector Projection |
|---|---|
| Gives a scalar | Gives a vector |
| Gives only magnitude along a direction | Gives magnitude and direction |
| $\frac{\vec{a}\cdot\vec{b}}{|\vec{b}|}$ | $\frac{\vec{a}\cdot\vec{b}}{|\vec{b}|^2}\vec{b}$ |
| Can be positive or negative | Points along or opposite to $\vec{b}$ |

---

**`Projection Using a Unit Vector`**

Suppose $\hat{b}$ is a **unit vector** in the direction of $\vec{b}$.

Since

$$
|\hat{b}|=1
$$

the projection becomes:

$$
\boxed{
\mathrm{proj}_{\hat{b}}\vec{a} =
(\vec{a}\cdot\hat{b})\hat{b}
}
$$

The scalar projection is:

$$
\boxed{
\mathrm{comp}_{\hat{b}}\vec{a} =
\vec{a}\cdot\hat{b}
}
$$

This form is often easier to use.

---

**`Finding a Unit Vector`**

If $\vec{b}$ is not already a unit vector, we can normalize it.

The unit vector in the direction of $\vec{b}$ is:

$$
\boxed{
\hat{b} =
\frac{\vec{b}}{|\vec{b}|}
}
$$

Then:

$$
\mathrm{proj}_{\vec{b}}\vec{a} =
(\vec{a}\cdot\hat{b})\hat{b}
$$

---

**`Projection and the Dot Product`**

Vector projection is directly based on the **dot product**.

Recall:

$$
\vec{a}\cdot\vec{b} =
|\vec{a}||\vec{b}|\cos\theta
$$

Therefore,

$$
\mathrm{proj}_{\vec{b}}\vec{a} =
\frac{
|\vec{a}||\vec{b}|\cos\theta
}{
|\vec{b}|^2
}
\vec{b}
$$

Simplifying:

$$
= \frac{|\vec{a}|\cos\theta}{|\vec{b}|}
\vec{b}
$$

Since

$$
\frac{\vec{b}}{|\vec{b}|}
$$

is the unit vector in the direction of $\vec{b}$, the projection is simply the component of $\vec{a}$ along that direction.

---

**`Projection and Angle Between Vectors`**

The scalar projection can also be written as:

$$
\boxed{
\mathrm{comp}_{\vec{b}}\vec{a} =
|\vec{a}|\cos\theta
}
$$

where $\theta$ is the angle between the vectors.

Therefore:

If

$$
0^\circ<\theta<90^\circ
$$

then

$$
\cos\theta>0
$$

and the scalar projection is positive.

---

If

$$
\theta=90^\circ
$$

then

$$
\cos90^\circ=0
$$

so:

$$
\mathrm{comp}_{\vec{b}}\vec{a}=0
$$

---

If

$$
90^\circ<\theta<180^\circ
$$

then

$$
\cos\theta<0
$$

and the scalar projection is negative.

---

**`Important Special Cases`**

`1. Same Direction`

If

$$
\theta=0^\circ
$$

then

$$
\cos0^\circ=1
$$

Therefore:

$$
\mathrm{comp}_{\vec{b}}\vec{a} =
|\vec{a}|
$$

when $\vec{a}$ points in the same direction as $\vec{b}$.

---

`2. Perpendicular Vectors`

If

$$
\theta=90^\circ
$$

then

$$
\cos90^\circ=0
$$

Therefore:

$$
\boxed{
\mathrm{proj}_{\vec{b}}\vec{a} =
\vec{0}
}
$$

This means a vector has no component in a direction perpendicular to it.

---

`3. Opposite Direction`

If

$$
\theta=180^\circ
$$

then

$$
\cos180^\circ=-1
$$

Therefore, the scalar projection is negative.

The projection points opposite to $\vec{b}$.

---

`Orthogonal Decomposition`

One of the most important applications of projection is **orthogonal decomposition**.

A vector $\vec{a}$ can be divided into two parts:

1. Component parallel to $\vec{b}$
2. Component perpendicular to $\vec{b}$

Therefore,

$$
\boxed{
\vec{a} =
\vec{a}_{\parallel} +
\vec{a}_{\perp}
}
$$

where

$$
\vec{a}_{\parallel} =
\mathrm{proj}_{\vec{b}}\vec{a}
$$

and

$$
\vec{a}_{\perp} =
\vec{a} -
\mathrm{proj}_{\vec{b}}\vec{a}
$$

---

**`Perpendicular Component`**

The component of $\vec{a}$ perpendicular to $\vec{b}$ is:

$$
\boxed{
\vec{a}_{\perp} =
\vec{a} -
\mathrm{proj}_{\vec{b}}\vec{a}
}
$$

Using the projection formula:

$$
\boxed{
\vec{a}_{\perp} =
\vec{a} -
\frac{\vec{a}\cdot\vec{b}}
{|\vec{b}|^2}
\vec{b}
}
$$

---

**Example of Orthogonal Decomposition**

Let

$$
\vec{a} =
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

and

$$
\vec{b} =
\begin{bmatrix}
1\\
0
\end{bmatrix}
$$

We already found:

$$
\mathrm{proj}_{\vec{b}}\vec{a} =
\begin{bmatrix}
3\\
0
\end{bmatrix}
$$

Therefore:

$$
\vec{a}_{\perp} =
\begin{bmatrix}
3\\
4
\end{bmatrix} -
\begin{bmatrix}
3\\
0
\end{bmatrix}
$$

$$
\boxed{
\vec{a}_{\perp} =
\begin{bmatrix}
0\\
4
\end{bmatrix}
}
$$

Therefore:

$$
\vec{a} =
\begin{bmatrix}
3\\
0
\end{bmatrix} +
\begin{bmatrix}
0\\
4
\end{bmatrix}
$$

The first vector is parallel to $\vec{b}$ and the second is perpendicular to $\vec{b}$.

---

**`Checking Orthogonality`**

The perpendicular component must satisfy:

$$
\vec{a}_{\perp}\cdot\vec{b}=0
$$

For the previous example:

$$
\begin{bmatrix}
0\\
4
\end{bmatrix}
\cdot
\begin{bmatrix}
1\\
0
\end{bmatrix}
$$

$$
=(0)(1)+(4)(0)
$$

$$
=0
$$

Therefore, the two vectors are perpendicular.

---

**`Projection onto a Coordinate Axis`**

Projection onto the $x$-axis is particularly simple.

For

$$
\vec{a} =
\begin{bmatrix}
x\\
y
\end{bmatrix}
$$

the projection onto the $x$-axis is:

$$
\boxed{
\mathrm{proj}_{x}\vec{a} =
\begin{bmatrix}
x\\
0
\end{bmatrix}
}
$$

Similarly, projection onto the $y$-axis is:

$$
\boxed{
\mathrm{proj}_{y}\vec{a} =
\begin{bmatrix}
0\\
y
\end{bmatrix}
}
$$

---

**`Projection in 3D`**

The same formula works in three dimensions.

Suppose:

$$
\vec{a} =
\begin{bmatrix}
a_1\\
a_2\\
a_3
\end{bmatrix}
$$

and

$$
\vec{b} =
\begin{bmatrix}
b_1\\
b_2\\
b_3
\end{bmatrix}
$$

Then:

$$
\vec{a}\cdot\vec{b} =
a_1b_1+a_2b_2+a_3b_3
$$

and:

$$
|\vec{b}|^2 =
b_1^2+b_2^2+b_3^2
$$

Therefore:

$$
\boxed{
\mathrm{proj}_{\vec{b}}\vec{a} =
\frac{
a_1b_1+a_2b_2+a_3b_3
}{
b_1^2+b_2^2+b_3^2
}
\begin{bmatrix}
b_1\\
b_2\\
b_3
\end{bmatrix}
}
$$

---

**`Projection onto a Subspace`**

Projection is not limited to a single vector.

We can also project a vector onto a **subspace**.

Suppose $W$ is a subspace.

The projection of $\vec{v}$ onto $W$ is the vector in $W$ that is closest to $\vec{v}$.

It can be written as:

$$
\vec{v} =
\vec{v}_W +
\vec{v}_{W^\perp}
$$

where

- $\vec{v}_W$ lies in $W$.
- $\vec{v}_{W^\perp}$ lies in the orthogonal complement of $W$.

---

**`Projection Matrix`**

Projection can also be represented using a **matrix**.

Suppose $\vec{b}$ is a non-zero column vector.

The projection matrix onto the direction of $\vec{b}$ is:

$$
\boxed{
P =
\frac{\vec{b}\vec{b}^T}
{\vec{b}^T\vec{b}}
}
$$

Then the projection of any vector $\vec{a}$ onto $\vec{b}$ can be calculated as:

$$
\boxed{
P\vec{a} =
\mathrm{proj}_{\vec{b}}\vec{a}
}
$$

This is particularly important in advanced Linear Algebra, numerical methods, computer graphics, and machine learning.

---

**Example of Projection Matrix**

Let

$$
\vec{b} =
\begin{bmatrix}
1\\
0
\end{bmatrix}
$$

Then:

$$
\vec{b}\vec{b}^T =
\begin{bmatrix}
1\\
0
\end{bmatrix}
\begin{bmatrix}
1&0
\end{bmatrix}
$$

Therefore:

$$
\vec{b}\vec{b}^T =
\begin{bmatrix}
1&0\\
0&0
\end{bmatrix}
$$

Also,

$$
\vec{b}^T\vec{b}=1
$$

Therefore:

$$
\boxed{
P=
\begin{bmatrix}
1&0\\
0&0
\end{bmatrix}
}
$$

Applying this to

$$
\vec{a} =
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

gives:

$$
P\vec{a} =
\begin{bmatrix}
1&0\\
0&0
\end{bmatrix}
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

$$
= \begin{bmatrix}
3\\
0
\end{bmatrix}
$$

which is exactly the projection of $\vec{a}$ onto the $x$-axis.

---

**`Properties of Projection`**

`1. Projection Lies in the Target Direction`

The projection of $\vec{a}$ onto $\vec{b}$ is always a scalar multiple of $\vec{b}$.

$$
\mathrm{proj}_{\vec{b}}\vec{a} =
k\vec{b}
$$

---

`2. Perpendicular Component is Orthogonal`

$$
\left(
\vec{a} -
\mathrm{proj}_{\vec{b}}\vec{a}
\right)
\cdot
\vec{b} =
0
$$

---

`3. Projection of a Vector onto Itself`

For a non-zero vector $\vec{a}$:

$$
\boxed{
\mathrm{proj}_{\vec{a}}\vec{a} =
\vec{a}
}
$$

---

`4. Projection of a Perpendicular Vector`

If

$$
\vec{a}\cdot\vec{b}=0
$$

then:

$$
\boxed{
\mathrm{proj}_{\vec{b}}\vec{a} =
\vec{0}
}
$$

---

`5. Projection Matrix is Idempotent`

For a projection matrix $P$:

$$
\boxed{
P^2=P
}
$$

This means applying the same projection twice produces the same result as applying it once.

---

`6. Projection Matrix is Symmetric`

For an orthogonal projection matrix:

$$
\boxed{
P^T=P
}
$$

---

**`Vector Projection vs Scalar Projection`**

It is important not to confuse these concepts.

`Scalar Projection`

$$
\boxed{
\mathrm{comp}_{\vec{b}}\vec{a} =
\frac{\vec{a}\cdot\vec{b}}
{|\vec{b}|}
}
$$

Result:

$$
\text{Scalar}
$$

---

`Vector Projection`

$$
\boxed{
\mathrm{proj}_{\vec{b}}\vec{a} =
\frac{\vec{a}\cdot\vec{b}}
{|\vec{b}|^2}
\vec{b}
}
$$

Result:

$$
\text{Vector}
$$

---

**`Important Formulas`**

`Scalar Projection`

$$
\boxed{
\mathrm{comp}_{\vec{b}}\vec{a} =
\frac{\vec{a}\cdot\vec{b}}
{|\vec{b}|}
}
$$

---

`Vector Projection`

$$
\boxed{
\mathrm{proj}_{\vec{b}}\vec{a} =
\frac{\vec{a}\cdot\vec{b}}
{|\vec{b}|^2}
\vec{b}
}
$$

---

`Projection Using a Unit Vector`

$$
\boxed{
\mathrm{proj}_{\hat{b}}\vec{a} =
(\vec{a}\cdot\hat{b})\hat{b}
}
$$

---

`Perpendicular Component`

$$
\boxed{
\vec{a}_{\perp} =
\vec{a} -
\mathrm{proj}_{\vec{b}}\vec{a}
}
$$

---

`Orthogonal Decomposition`

$$
\boxed{
\vec{a} =
\vec{a}_{\parallel} +
\vec{a}_{\perp}
}
$$

---

`Projection Matrix`

$$
\boxed{
P=
\frac{\vec{b}\vec{b}^T}
{\vec{b}^T\vec{b}}
}
$$

---

`Projection Using a Matrix`

$$
\boxed{
P\vec{a} =
\mathrm{proj}_{\vec{b}}\vec{a}
}
$$

---

## `3. Introduction to Matrices`
Matrices are rectangular arrays of numbers, symbols, or characters where all of these elements are arranged in each row and column.

- A matrix is identified by its order, which is given in the form of rows ⨯ columns, and the location of each element is given by the row and column it belongs to.
- A matrix is represented as ([P]m⨯n), where P is the matrix, m is the number of rows, and n is the number of columns.

<b> `Example` </b>

`1. Matrix A (2×2) :`

$$
A = \begin{bmatrix}
1 & 2\\
3 & 4
\end{bmatrix}_{2\times2}
$$

`2. Matrix B (3×3) :`

$$
B = \begin{bmatrix}
1 & -1 & 2\\
3 & 2 & 6\\
4 & -2 & 5
\end{bmatrix}_{3\times3}
$$

Here, A is a 2×2 matrix (2 rows and 2 columns) and B is a 3×3 matrix (3 rows and 3 columns).
<hr>


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

**`3. Matrix Multiplication`**

**Matrix multiplication** combines two matrices to produce a new matrix. Unlike addition and subtraction, multiplication follows the **row-by-column rule**.

---

**`Condition for Matrix Multiplication`**

If

$$
A_{m\times n}
$$

and

$$
B_{n\times p}
$$

then

$$
AB=C_{m\times p}
$$

> The **number of columns** of the first matrix must equal the **number of rows** of the second matrix.

---

**`Formula`**

$$
(AB)_{ij} =
\sum_{k=1}^{n}a_{ik}b_{kj}
$$

---

**Example**

$$
A=
\begin{bmatrix}
1 & 2\\
3 & 4
\end{bmatrix}
$$

$$
B=
\begin{bmatrix}
5 & 6\\
7 & 8
\end{bmatrix}
$$

$$
AB=
\begin{bmatrix}
19 & 22\\
43 & 50
\end{bmatrix}
$$

---

**`Properties`**

`1. Associative Property`

$$
(AB)C=A(BC)
$$

`2. Distributive Property`

$$
A(B+C)=AB+AC
$$

$$
(A+B)C=AC+BC
$$

`3. Not Commutative`

$$
AB \neq BA
$$

`4. Identity Matrix`

$$
AI=IA=A
$$

---

**`Scalar Multiplication of Matrices`**

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

**`4. Transpose of a Matrix`**

The **transpose** of a matrix is a new matrix obtained by **interchanging the rows and columns** of the original matrix. Every row of the original matrix becomes a column in the transpose, and every column becomes a row.

The transpose is one of the most important operations in linear algebra and is widely used in mathematics, engineering, computer science, statistics, machine learning, and computer graphics.

> **Note:** The transpose can be found for **any matrix**, whether it is square or rectangular.

---

Let

$$
A=[a_{ij}]
$$

be an $m \times n$ matrix.

The transpose of matrix $A$ is denoted by

$$
A^T
$$

or sometimes

$$
A'
$$

and is defined as

$$
A^T=[a_{ji}]
$$

This means the element at the **i-th row** and **j-th column** of the original matrix becomes the element at the **j-th row** and **i-th column** of the transpose.

---

**`Order of Transpose Matrix`**

If a matrix

$$
A
$$

has order

$$
m \times n
$$

then its transpose

$$
A^T
$$

has order

$$
n \times m
$$

Thus, the number of rows becomes the number of columns, and the number of columns becomes the number of rows.

**`Examples`**

| Original Matrix | Order | Transpose | Order |
|-----------------|-------|-----------|-------|
| $A$ | $2\times3$ | $A^T$ | $3\times2$ |
| $A$ | $3\times2$ | $A^T$ | $2\times3$ |
| $A$ | $4\times5$ | $A^T$ | $5\times4$ |
| $A$ | $3\times3$ | $A^T$ | $3\times3$ |

---

**`How to Find the Transpose of a Matrix?`**

The transpose of a matrix is obtained by converting every **row into a column**.

**Steps**

1. Write the first row as the first column.
2. Write the second row as the second column.
3. Continue until every row becomes a corresponding column.

**Shortcut:**

> **Rows → Columns**  
> **Columns → Rows**

**Example**

Given

$$
A=
\begin{bmatrix}
1 & 2 & 3\\
4 & 5 & 6
\end{bmatrix}
$$

The first row

$$
[1\;\;2\;\;3]
$$

becomes the first column.

The second row

$$
[4\;\;5\;\;6]
$$

becomes the second column.

Therefore,

$$
A^T=
\begin{bmatrix}
1 & 4\\
2 & 5\\
3 & 6
\end{bmatrix}
$$

---

**`Transpose of Row and Column Matrix`**

`1. Transpose of a Row Matrix`

A **row matrix** contains only one row.

Example

$$
A=
\begin{bmatrix}
2 & 5 & 8 & 9
\end{bmatrix}
$$

Order:

$$
1\times4
$$

Transpose:

$$
A^T=
\begin{bmatrix}
2\\
5\\
8\\
9
\end{bmatrix}
$$

Order:

$$
4\times1
$$

Hence,

> The transpose of a **row matrix** is a **column matrix**.

---

`2. Transpose of a Column Matrix`

A **column matrix** contains only one column.

Example

$$
A=
\begin{bmatrix}
4\\
7\\
9
\end{bmatrix}
$$

Order:

$$
3\times1
$$

Transpose:

$$
A^T=
\begin{bmatrix}
4 & 7 & 9
\end{bmatrix}
$$

Order:

$$
1\times3
$$

Hence,

> The transpose of a **column matrix** is a **row matrix**.

---

`Transpose of Horizontal and Vertical Matrices`

A **horizontal matrix** is another name for a **row matrix**, while a **vertical matrix** is another name for a **column matrix**.

**Horizontal Matrix**

$$
A=
\begin{bmatrix}
3 & 6 & 9 & 12
\end{bmatrix}
$$

Transpose

$$
A^T=
\begin{bmatrix}
3\\
6\\
9\\
12
\end{bmatrix}
$$

Thus, a horizontal matrix becomes a vertical matrix.

---

`Vertical Matrix`

$$
B=
\begin{bmatrix}
5\\
8\\
11
\end{bmatrix}
$$

Transpose

$$
B^T=
\begin{bmatrix}
5 & 8 & 11
\end{bmatrix}
$$

Thus, a vertical matrix becomes a horizontal matrix.

---

**`Transpose of a Symmetric Matrix`**

A **symmetric matrix** is a square matrix whose transpose is equal to the original matrix.

Mathematically,

$$
A=A^T
$$

**Example**

$$
A=
\begin{bmatrix}
2 & 4 & 6\\
4 & 5 & 7\\
6 & 7 & 9
\end{bmatrix}
$$

Transpose

$$
A^T=
\begin{bmatrix}
2 & 4 & 6\\
4 & 5 & 7\\
6 & 7 & 9
\end{bmatrix}
$$

Since

$$
A=A^T
$$

the matrix is **symmetric**.

**Important Points**

- Every symmetric matrix is a **square matrix**.
- Elements on opposite sides of the main diagonal are equal.
- The transpose of a symmetric matrix is always the matrix itself.

---

**`Transpose of a Diagonal Matrix`**

A **diagonal matrix** is a square matrix in which all the elements outside the main diagonal are zero.

General form:

$$
A=
\begin{bmatrix}
a_1 & 0 & 0\\
0 & a_2 & 0\\
0 & 0 & a_3
\end{bmatrix}
$$

When we transpose a diagonal matrix, the rows become columns. Since all the non-diagonal elements are already zero, the transpose remains exactly the same.

Mathematically,

$$
A^T=A
$$

**Example**

$$
A=
\begin{bmatrix}
4 & 0 & 0\\
0 & 7 & 0\\
0 & 0 & 9
\end{bmatrix}
$$

Transpose:

$$
A^T=
\begin{bmatrix}
4 & 0 & 0\\
0 & 7 & 0\\
0 & 0 & 9
\end{bmatrix}
$$

Since

$$
A^T=A
$$

the transpose of every diagonal matrix is the matrix itself.

**Important Points**

- Every diagonal matrix is a **square matrix**.
- Every diagonal matrix is also a **symmetric matrix**.
- The transpose of a diagonal matrix never changes the position of its non-zero elements.

---

**`Transpose of a Transposed Matrix`**

When the transpose operation is applied **twice**, we obtain the original matrix.

This property is called the **Double Transpose Property**.

Mathematically,

$$
(A^T)^T=A
$$

**Why?**

- First transpose changes rows into columns.
- Second transpose changes those columns back into rows.
- Therefore, the original arrangement is restored.

**Example**

Let

$$
A=
\begin{bmatrix}
1 & 2 & 3\\
4 & 5 & 6
\end{bmatrix}
$$

First transpose:

$$
A^T=
\begin{bmatrix}
1 & 4\\
2 & 5\\
3 & 6
\end{bmatrix}
$$

Transpose again:

$$
(A^T)^T=
\begin{bmatrix}
1 & 2 & 3\\
4 & 5 & 6
\end{bmatrix}
$$

Hence,

$$
(A^T)^T=A
$$

**Important Points**

- This property is valid for **every matrix**.
- It does not matter whether the matrix is square or rectangular.
- Applying transpose twice always returns the original matrix.

---

**`Transpose of a Square Matrix`**

A **square matrix** has the same number of rows and columns.

If

$$
A
$$

is of order

$$
n\times n
$$

then its transpose is also of order

$$
n\times n
$$

Unlike rectangular matrices, the order of a square matrix does **not** change after taking the transpose.

**Example**

$$
A=
\begin{bmatrix}
2 & 4 & 6\\
1 & 3 & 5\\
7 & 8 & 9
\end{bmatrix}
$$

Transpose:

$$
A^T=
\begin{bmatrix}
2 & 1 & 7\\
4 & 3 & 8\\
6 & 5 & 9
\end{bmatrix}
$$

Original order:

$$
3\times3
$$

Transpose order:

$$
3\times3
$$

Only the positions of the elements change.

**Important Points**

- A square matrix always remains a square matrix after transpose.
- The order remains unchanged.
- A square matrix may or may not be symmetric.

---

**`Properties of Matrix Transpose`**

The transpose operation satisfies several important algebraic properties.

---

`1. Double Transpose Property`

Taking the transpose twice gives the original matrix.

$$
(A^T)^T=A
$$

---

`2. Addition Property`

The transpose of the sum of two matrices equals the sum of their transposes.

$$
(A+B)^T=A^T+B^T
$$

`Example`

$$
A=
\begin{bmatrix}
1 & 2\\
3 & 4
\end{bmatrix},
\quad
B=
\begin{bmatrix}
5 & 6\\
7 & 8
\end{bmatrix}
$$

Then

$$
(A+B)^T=A^T+B^T
$$

---

`3. Subtraction Property`

The transpose of the difference of two matrices equals the difference of their transposes.

$$
(A-B)^T=A^T-B^T
$$

---

`4. Scalar Multiplication Property`

If $k$ is any scalar,

$$
(kA)^T=kA^T
$$

**Example**

If

$$
k=5
$$

then

$$
(5A)^T=5A^T
$$

---

`5. Matrix Multiplication Property`

The transpose of the product of two matrices is equal to the product of their transposes in the **reverse order**.

$$
(AB)^T=B^TA^T
$$

Notice that the order changes.

It is **not**

$$
A^TB^T
$$

This is one of the most important properties of transpose.

---

`6. Identity Matrix Property`

The transpose of an identity matrix is the identity matrix itself.

$$
I^T=I
$$

Example

$$
I=
\begin{bmatrix}
1 & 0\\
0 & 1
\end{bmatrix}
$$

---

`7. Zero Matrix Property`

The transpose of a zero matrix is also a zero matrix.

$$
O^T=O
$$

---

`8. Symmetric Matrix Property`

If a matrix is symmetric,

$$
A=A^T
$$

then taking its transpose does not change the matrix.

---

`9. Diagonal Matrix Property`

Every diagonal matrix satisfies

$$
A^T=A
$$

Therefore, every diagonal matrix is symmetric.

---

`10. Determinant Property`

For every square matrix,

$$
|A^T|=|A|
$$

This means the determinant of a matrix remains unchanged after taking the transpose.

---

`11. Inverse Property`

If a matrix is invertible,

$$
(A^{-1})^T=(A^T)^{-1}
$$

This means the transpose of the inverse is equal to the inverse of the transpose.

---

**`5. Inverse of a Matrix`**

The **inverse of a matrix** is a matrix that, when multiplied by the original matrix, produces the **identity matrix**. The inverse of a matrix plays the same role in matrix algebra as the reciprocal of a number in arithmetic.

For example,

- The reciprocal (inverse) of the number **5** is

$$
\frac{1}{5}
$$

because

$$
5\times\frac{1}{5}=1
$$

Similarly, if a matrix $A$ has an inverse $A^{-1}$, then

$$
AA^{-1}=A^{-1}A=I
$$

where $I$ is the **identity matrix**.

The inverse of a matrix is widely used in solving systems of linear equations, computer graphics, machine learning, cryptography, engineering, and scientific computing.

> **Note:** Only **square matrices** having a **non-zero determinant** possess an inverse.

---

Let

$$
A
$$

be a square matrix.

If there exists another matrix

$$
A^{-1}
$$

such that

$$
AA^{-1}=A^{-1}A=I
$$

then

$$
A^{-1}
$$

is called the **inverse of matrix $A$**.

---

**`Conditions for the Existence of an Inverse`**

A matrix has an inverse only if:

- It is a **square matrix**.
- Its determinant is **non-zero**.

Mathematically,

$$
|A|\neq0
$$

If

$$
|A|=0
$$

then the matrix has **no inverse**.

---

**`Formula for the Inverse of a 2×2 Matrix`**

Let

$$
A=
\begin{bmatrix}
a & b\\
c & d
\end{bmatrix}
$$

Then,

$$
A^{-1} =
\frac{1}{ad-bc}
\begin{bmatrix}
d & -b\\
-c & a
\end{bmatrix}
$$

provided

$$
ad-bc\neq0
$$

---

**Example**

Find the inverse of

$$
A=
\begin{bmatrix}
2 & 3\\
1 & 4
\end{bmatrix}
$$

`Step 1: Find the determinant`

$$
|A|
=(2)(4)-(3)(1)
=8-3
=5
$$

Since

$$
|A|\neq0
$$

the inverse exists.

`Step 2: Apply the formula`

$$
A^{-1} =
\frac{1}{5}
\begin{bmatrix}
4 & -3\\
-1 & 2
\end{bmatrix}
$$

Therefore,

$$
A^{-1} =
\begin{bmatrix}
\frac45 & -\frac35\\
-\frac15 & \frac25
\end{bmatrix}
$$

---

**`Finding the Inverse of a Matrix`**

There are several methods for finding the inverse of a matrix.

`1. Formula Method (2×2 Matrix)`

Used only for matrices of order

$$
2\times2
$$

Formula:

$$
A^{-1} =
\frac{1}{|A|}
\mathrm{adj}(A)
$$

---

`2. Adjoint (Adjugate) Method`

This method can be used for higher-order square matrices.

**Steps**

1. Find the determinant.
2. Find the matrix of minors.
3. Convert minors into cofactors.
4. Find the transpose of the cofactor matrix (Adjoint).
5. Divide the adjoint by the determinant.

Formula

$$
A^{-1} =
\frac{1}{|A|}
\mathrm{adj}(A)
$$

---

`3. Gauss-Jordan Elimination Method`

Steps

1. Form the augmented matrix

$$
[A|I]
$$

2. Apply elementary row operations.
3. Convert the left side into the identity matrix.
4. The right side becomes the inverse matrix.

This method is commonly used for matrices of order

$$
3\times3
$$

or higher.

---

**`Terms Related to Inverse of a Matrix`**

`1. Identity Matrix`

An identity matrix is a square matrix whose diagonal elements are 1 and all other elements are 0.

Example

$$
I=
\begin{bmatrix}
1&0\\
0&1
\end{bmatrix}
$$

It satisfies

$$
AI=IA=A
$$

---

`2. Singular Matrix`

A square matrix whose determinant is zero.

$$
|A|=0
$$

A singular matrix **does not have an inverse**.

---

`3. Non-Singular Matrix`

A square matrix having a non-zero determinant.

$$
|A|\neq0
$$

A non-singular matrix **always has an inverse**.

---

`4. Adjoint (Adjugate) Matrix`

The transpose of the cofactor matrix is called the **adjoint** of the matrix.

It is denoted by

$$
\mathrm{adj}(A)
$$

---

`5. Determinant`

The determinant determines whether the inverse exists.

- If

$$
|A|\neq0
$$

Inverse exists.

- If

$$
|A|=0
$$

Inverse does not exist.

---

**`Properties of Inverse Matrix`**

The inverse operation satisfies several important properties.

---

`1. Inverse of the Identity Matrix`

$$
I^{-1}=I
$$

---

`2. Inverse of an Inverse Matrix`

$$
(A^{-1})^{-1}=A
$$

---

`3. Product Property`

The inverse of a product is

$$
(AB)^{-1}=B^{-1}A^{-1}
$$

Notice that the order is reversed.

---

`4. Transpose Property`

$$
(A^T)^{-1}=(A^{-1})^T
$$

---

`5. Scalar Multiplication Property`

If

$$
k\neq0
$$

then

$$
(kA)^{-1} =
\frac1kA^{-1}
$$

---

`6. Determinant Property`

$$
|A^{-1}| =
\frac1{|A|}
$$

provided

$$
|A|\neq0
$$

---

`7. Inverse of a Diagonal Matrix`

The inverse of a diagonal matrix is another diagonal matrix whose diagonal entries are reciprocals of the original diagonal entries.

Example

$$
A=
\begin{bmatrix}
2&0\\
0&5
\end{bmatrix}
$$

$$
A^{-1} =
\begin{bmatrix}
\frac12&0\\
0&\frac15
\end{bmatrix}
$$

---

`8. Inverse of a Symmetric Matrix`

If

$$
A=A^T
$$

and the inverse exists, then

$$
A^{-1}
$$

is also symmetric.

---

**`Determinant of Inverse Matrix`**

If

$$
A
$$

is an invertible matrix, then

$$
|A^{-1}| =
\frac1{|A|}
$$

This means the determinant of the inverse is simply the reciprocal of the determinant of the original matrix.

**Example**

If

$$
|A|=8
$$

then

$$
|A^{-1}| =
\frac18
$$

**Important Points**

- Applicable only for invertible matrices.
- If

$$
|A|=0
$$

then the inverse does not exist.

---


**`Important Formulas`**

$$
AA^{-1}=I
$$

---

`Formula`

$$
A^{-1} =
\frac1{|A|}
\mathrm{adj}(A)
$$

---

`2×2 Matrix`

$$
A^{-1} =
\frac1{ad-bc}
\begin{bmatrix}
d&-b\\
-c&a
\end{bmatrix}
$$

---

`Product Property`

$$
(AB)^{-1}=B^{-1}A^{-1}
$$

---

`Transpose Property`

$$
(A^T)^{-1}=(A^{-1})^T
$$

---

`Determinant Property`

$$
|A^{-1}| =
\frac1{|A|}
$$

---


## `4. Systems of linear equations`

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
\underbrace{\begin{bmatrix} x \\ y \end{bmatrix}}_{\mathbf{x}}
=
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


## `5. Elimination and Matrix Multiplication`

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
| Replacement | $\begin{bmatrix} 1&0&0\\-3&1&0\\0&0&1 \end{bmatrix}$ | Row 2 $\leftarrow$ row 2 $- 3 \times$ row 1 |
| Exchange | $\begin{bmatrix} 0&1&0\\1&0&0\\0&0&1 \end{bmatrix}$ | Swap rows 1 and 2 |
| Scaling | $\begin{bmatrix} 1&0&0\\0&\tfrac12&0\\0&0&1 \end{bmatrix}$ | Row 2 $\leftarrow \tfrac12 \times$ row 2 |

Example with the running matrix:

$$
E_{21}A =
\begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}
\begin{bmatrix} 1 & 2 & 1 \\ 3 & 8 & 1 \\ 0 & 4 & 1 \end{bmatrix}
=
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

### `9. Matrix Multiplication in Elimination`

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
E = \begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 6 & -2 & 1 \end{bmatrix},
\qquad
EA = U
$$

Check, row 3 of $EA$: $6(1,2,1) - 2(3,8,1) + (0,4,1) = (0,\ 0,\ 5)$ ✓.

The same $E$ acts on the right-hand side:

$$
E\mathbf{b} =
\begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 6 & -2 & 1 \end{bmatrix}
\begin{bmatrix} 2 \\ 12 \\ 2 \end{bmatrix}
=
\begin{bmatrix} 2 \\ 6 \\ -10 \end{bmatrix} = \mathbf{c}
$$

So $A\mathbf{x} = \mathbf{b}$ becomes $EA\mathbf{x} = E\mathbf{b}$, i.e. $U\mathbf{x} = \mathbf{c}$.

Note the $6$ in $E$: it equals $\ell_{21}\ell_{32} = 3 \times 2$. The steps interact, so $E$ is messier than the individual multipliers. Section 12 shows how $L$ avoids this.

---

### **`10. Permutation Matrices`**

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

### **`11. Row Exchanges and Column Exchanges`**

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

### `12. Inverse of Elimination Matrices`

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

### **`14. Non-Commutative Property of Matrix Multiplication (AB ≠ BA)`**

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
