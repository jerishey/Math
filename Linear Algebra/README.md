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

### **`Vector Components`**

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

### **`Vector Projection`**

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

## **`4. Determinants in Linear Algebra`**

A **determinant** is a scalar (single numerical value) associated with a **square matrix**. It provides important information about a matrix, such as whether the matrix is invertible, the scaling factor of a linear transformation, and whether a system of linear equations has a unique solution.

Determinants are one of the fundamental concepts in linear algebra and have applications in mathematics, physics, engineering, computer graphics, machine learning, and data science.

> **Note:** Determinants are defined **only for square matrices**.

---

**`Determinants of Different Types of Matrices`**

Different types of matrices have different determinant values and properties.

`1. Determinant of a 1×1 Matrix`

For a matrix

$$
A=
\begin{bmatrix}
a
\end{bmatrix}
$$

The determinant is simply

$$
|A|=a
$$

**Example**

$$
A=
\begin{bmatrix}
7
\end{bmatrix}
$$

$$
|A|=7
$$

---

`2. Determinant of a 2×2 Matrix`

For

$$
A=
\begin{bmatrix}
a & b\\
c & d
\end{bmatrix}
$$

the determinant is

$$
|A|=ad-bc
$$

**Example**

$$
A=
\begin{bmatrix}
2 & 3\\
1 & 4
\end{bmatrix}
$$

$$
|A|
=(2)(4)-(3)(1)
=8-3
=5
$$

---

`3. Determinant of a 3×3 Matrix`

For

$$
A=
\begin{bmatrix}
a & b & c\\
d & e & f\\
g & h & i
\end{bmatrix}
$$

$$
|A| =
a(ei-fh) -
b(di-fg)
+
c(dh-eg)
$$

**Example**

$$
A=
\begin{bmatrix}
1 & 2 & 3\\
0 & 4 & 5\\
1 & 0 & 6
\end{bmatrix}
$$

$$
|A|=22
$$

---

`4. Determinant of an Identity Matrix`

For every identity matrix,

$$
|I|=1
$$

**Example**

$$
I=
\begin{bmatrix}
1&0\\
0&1
\end{bmatrix}
$$

$$
|I|=1
$$

---

`5. Determinant of a Zero Matrix`

If every element of the matrix is zero,

$$
|O|=0
$$

**Example**

$$
O=
\begin{bmatrix}
0&0\\
0&0
\end{bmatrix}
$$

---

`6. Determinant of a Diagonal Matrix`

The determinant of a diagonal matrix is the **product of its diagonal elements**.

For

$$
A=
\begin{bmatrix}
a&0&0\\
0&b&0\\
0&0&c
\end{bmatrix}
$$

$$
|A|=abc
$$

**Example**

$$
A=
\begin{bmatrix}
2&0&0\\
0&5&0\\
0&0&4
\end{bmatrix}
$$

$$
|A|
=2\times5\times4
=40
$$

---

`7. Determinant of a Triangular Matrix`

For both **upper triangular** and **lower triangular** matrices, the determinant equals the product of the diagonal elements.

**Example**

$$
A=
\begin{bmatrix}
2&4&5\\
0&3&7\\
0&0&6
\end{bmatrix}
$$

$$
|A|
=2\times3\times6
=36
$$

---

`8. Determinant of a Symmetric Matrix`

A symmetric matrix satisfies

$$
A=A^T
$$

Its determinant is computed in the same way as any square matrix.

**Example**

$$
A=
\begin{bmatrix}
2&3\\
3&5
\end{bmatrix}
$$

$$
|A|
=(2)(5)-(3)(3)
=1
$$

---

`9. Determinant of a Singular Matrix`

A singular matrix has

$$
|A|=0
$$

Therefore, it has **no inverse**.

---

`10. Determinant of a Non-Singular Matrix`

A non-singular matrix satisfies

$$
|A|\neq0
$$

Therefore, the inverse exists.

---

**`Physical Significance of Determinant`**

The determinant has several important interpretations in mathematics and physical sciences.

`1. Scaling Factor`

The determinant tells how much a linear transformation **stretches or shrinks** an object.

- If

$$
|A|=2
$$

the area or volume doubles.

- If

$$
|A|=\frac12
$$

the area or volume becomes half.

---

`2. Change in Orientation`

- Positive determinant → Orientation remains unchanged.
- Negative determinant → Orientation is reversed (reflection).

---

`3. Area of a Parallelogram`

If two vectors form a parallelogram, the absolute value of their determinant equals its area.

$$
\text{Area}=|\det(A)|
$$

---

`4. Volume of a Parallelepiped`

For three-dimensional vectors,

$$
\text{Volume}=|\det(A)|
$$

---

`5. Testing Linear Independence`

If

$$
|A|\neq0
$$

then the vectors are **linearly independent**.

If

$$
|A|=0
$$

they are **linearly dependent**.

---

`6. Solving Systems of Linear Equations`

A system has a unique solution if

$$
|A|\neq0
$$

Otherwise, it has either infinitely many solutions or no solution.

---

`7. Matrix Invertibility`

A matrix is invertible only if

$$
|A|\neq0
$$

---

**`Laplace Formula for Determinant`**

The **Laplace Expansion Theorem** (also called the **cofactor expansion**) provides a method for calculating the determinant of any square matrix by expanding along **any row or any column**.

It is especially useful for matrices of order **3×3 or higher**.

---

`Expansion Along the First Row`

$$
|A| =
a_{11}C_{11}
+
a_{12}C_{12}
+
a_{13}C_{13}
+\cdots
+
a_{1n}C_{1n}
$$

where

$$
C_{ij} =(-1)^{i+j}M_{ij}
$$

---

`Expansion Along the First Column`

$$
|A| =
a_{11}C_{11}
+
a_{21}C_{21}
+
a_{31}C_{31}
+\cdots
+
a_{n1}C_{n1}
$$

---

**`Steps to Apply Laplace Expansion`**

1. Select any row or column.
2. Find the minor of each element.
3. Calculate the cofactors.
4. Multiply each element by its corresponding cofactor.
5. Add all the products.

---

**Example**

$$
A=
\begin{bmatrix}
1&2&3\\
0&4&5\\
1&0&6
\end{bmatrix}
$$

Expand along the first row.

$$
|A| =
1(24) -
2(-5)
+
3(-4)
$$

$$
|A| =
24+10-12 =22
$$

---

**`Properties of Determinants of a Matrix`**

Determinants satisfy many important algebraic properties.

`1. Determinant Exists Only for Square Matrices`

Only square matrices have determinants.

---

`2. Determinant of Identity Matrix`

$$
|I|=1
$$

---

`3. Determinant of Zero Matrix`

$$
|O|=0
$$

---

`4. Interchanging Two Rows (or Columns)`

Interchanging any two rows (or columns) changes the **sign** of the determinant.

---

`5. Two Equal Rows (or Columns)`

If any two rows or columns are identical,

$$
|A|=0
$$

---

`6. One Row (or Column) is All Zeros`

If any row or column contains only zeros,

$$
|A|=0
$$

---

`7. Multiplying a Row by a Scalar`

If one row is multiplied by a constant $k$, the determinant is also multiplied by $k$.

---

`8. Common Factor`

A common factor from any row or column can be taken outside the determinant.

---

`9. Transpose Property`

The determinant of a matrix equals the determinant of its transpose.

$$
|A^T|=|A|
$$

---

`10. Product Property`

$$
|AB| =
|A||B|
$$

---

`11. Inverse Property`

If the inverse exists,

$$
|A^{-1}| =
\frac1{|A|}
$$

---

`12. Triangular Matrix Property`

For upper or lower triangular matrices,

$$
|A| =
\text{Product of diagonal elements}
$$

---

`13. Singular Matrix Property`

If

$$
|A|=0
$$

the matrix is singular and has no inverse.

---

`14. Non-Singular Matrix Property`

If

$$
|A|\neq0
$$

the matrix is non-singular and has an inverse.

---

## **`5. Vector Spaces in Linear Algebra`**

A **Vector Space** is one of the most fundamental concepts in **Linear Algebra**. It is a collection (or set) of objects called **vectors** together with two operations:

1. **Vector Addition**
2. **Scalar Multiplication**

These operations must satisfy a specific set of mathematical rules known as the **Vector Space Axioms**.

Although vectors are often represented as arrows or ordered lists of numbers, vector spaces can also consist of matrices, polynomials, functions, and many other mathematical objects.

---

Vector spaces provide the foundation for many advanced topics such as:

- Linear Transformations
- Eigenvalues and Eigenvectors
- Machine Learning
- Artificial Intelligence
- Computer Graphics
- Robotics
- Data Science
- Signal Processing
- Quantum Computing


> **Note:** Every vector space is defined over a field of scalars, usually the set of **real numbers ($\mathbb{R}$)** or **complex numbers ($\mathbb{C}$)**.

---

**`What is a Vector?`**

A **vector** is a mathematical object that has both **magnitude** (length) and **direction**.

Examples of vectors are:

$$
\begin{bmatrix}
2\\
5
\end{bmatrix}
,
\qquad
\begin{bmatrix}
1\\
4\\
6
\end{bmatrix}
$$

Unlike ordinary numbers (called **scalars**), vectors can represent displacement, velocity, force, and many other physical quantities.

---

**`Definition of a Vector Space`**

A **Vector Space** is a set of vectors $V$ together with two operations:

- Vector Addition
- Scalar Multiplication

such that all the vector space axioms are satisfied.

If

$$
u,v\in V
$$

then

$$
u+v\in V
$$

and if

$$
k
$$

is any scalar,

$$
ku\in V
$$

where

- $u,v$ are vectors
- $k$ is a scalar

---

**`Understanding the Two Operations`**

`1. Vector Addition`

Two vectors are added by adding their corresponding components.

Example

$$
u=
\begin{bmatrix}
2\\
4
\end{bmatrix}
,
\qquad
v=
\begin{bmatrix}
3\\
5
\end{bmatrix}
$$

Then

$$
u+v=
\begin{bmatrix}
2+3\\
4+5
\end{bmatrix} =
\begin{bmatrix}
5\\
9
\end{bmatrix}
$$

---

`2. Scalar Multiplication`

A scalar multiplies every element of the vector.

Example

$$
3
\begin{bmatrix}
2\\
5
\end{bmatrix} =
\begin{bmatrix}
6\\
15
\end{bmatrix}
$$

---

**`Vector Space Axioms (Properties)`**

A set becomes a **Vector Space** only if it satisfies **all** of the following properties.

---

`1. Closure under Addition`

If two vectors belong to the vector space, then their sum must also belong to the same vector space.

Mathematically,

$$
u,v\in V
\quad\Rightarrow\quad
u+v\in V
$$

**Example**

$$
u=
\begin{bmatrix}
1\\
2
\end{bmatrix}
,
\qquad
v=
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

Then

$$
u+v=
\begin{bmatrix}
4\\
6
\end{bmatrix}
$$

which is also a vector in the same space.

---

`2. Closure under Scalar Multiplication`

If a vector belongs to the vector space, multiplying it by any scalar must produce another vector in the same space.

$$
k\in\mathbb{R},
\quad
u\in V
\quad\Rightarrow\quad
ku\in V
$$

**Example**

$$
2
\begin{bmatrix}
3\\
4
\end{bmatrix} =
\begin{bmatrix}
6\\
8
\end{bmatrix}
$$

---

`3. Commutative Property of Addition`

Changing the order of addition does not affect the result.

$$
u+v=v+u
$$

**Example**

$$
\begin{bmatrix}
1\\
2
\end{bmatrix}
+
\begin{bmatrix}
3\\
4
\end{bmatrix} =
\begin{bmatrix}
3\\
4
\end{bmatrix}
+
\begin{bmatrix}
1\\
2
\end{bmatrix}
$$

---

`4. Associative Property of Addition`

Grouping of vectors does not change the result.

$$
(u+v)+w=u+(v+w)
$$

---

`5. Additive Identity`

There exists a **zero vector** denoted by

$$
0
$$

such that

$$
u+0=u
$$

Example

$$
\begin{bmatrix}
5\\
8
\end{bmatrix}
+
\begin{bmatrix}
0\\
0
\end{bmatrix} =
\begin{bmatrix}
5\\
8
\end{bmatrix}
$$

---

`6. Additive Inverse`

Every vector has an opposite vector.

$$
u+(-u)=0
$$

Example

$$
\begin{bmatrix}
4\\
7
\end{bmatrix}
+
\begin{bmatrix}
-4\\
-7
\end{bmatrix} =
\begin{bmatrix}
0\\
0
\end{bmatrix}
$$

---

`7. Multiplicative Identity`

Multiplying by 1 leaves the vector unchanged.

$$
1u=u
$$

---

`8. Distributive Property over Vector Addition`

$$
k(u+v)=ku+kv
$$

Example

$$
2
\left(
\begin{bmatrix}
1\\
2
\end{bmatrix}
+
\begin{bmatrix}
3\\
4
\end{bmatrix}
\right) =
\begin{bmatrix}
8\\
12
\end{bmatrix}
$$

---

`9. Distributive Property over Scalar Addition`

$$
(a+b)u=au+bu
$$

---

`10. Compatibility of Scalar Multiplication`

$$
(ab)u=a(bu)
$$

---

**`Examples of Vector Spaces`**

The following sets satisfy all the vector space axioms.

---

`1. Real Numbers`

The set

$$
\mathbb{R}
$$

forms a vector space over itself.

Example

$$
2+5=7
$$

$$
3(5)=15
$$

---

`2. Two-Dimensional Space`

$$
\mathbb{R}^2
$$

contains vectors of the form

$$
\begin{bmatrix}
x\\
y
\end{bmatrix}
$$

Example

$$
\begin{bmatrix}
2\\
3
\end{bmatrix}
,
\quad
\begin{bmatrix}
5\\
1
\end{bmatrix}
$$

---

`3. Three-Dimensional Space`

$$
\mathbb{R}^3
$$

contains vectors

$$
\begin{bmatrix}
x\\
y\\
z
\end{bmatrix}
$$

---

`4. Matrix Vector Space`

All matrices of the same order form a vector space.

Example

$$
\begin{bmatrix}
1&2\\
3&4
\end{bmatrix}
$$

---

`5. Polynomial Vector Space`

All polynomials form a vector space.

Example

$$
2x^2+5x+1
$$

---

`6. Function Vector Space`

Continuous functions such as

$$
f(x)=x^2
$$

also form vector spaces.

---

**`Non-Examples of Vector Spaces`**

Some sets fail to satisfy the vector space axioms.

---

`Positive Integers`

Positive integers are **not** a vector space because negative numbers are not included.

Example

$$
5+(-5)=0
$$

but

$$
0
$$

is not a positive integer.

---

`Natural Numbers`

Natural numbers do not contain additive inverses.

Hence they are not vector spaces.

---

`Odd Numbers`

Odd numbers are not closed under addition.

Example

$$
3+5=8
$$

which is not odd.

---

`Positive Real Numbers`

Positive real numbers are not closed under multiplication by negative scalars.

Example

$$
(-2)(5)=-10
$$

which is not positive.

---

**`Subspaces`**

A **Subspace** is a subset of a vector space that is itself a vector space under the same operations of vector addition and scalar multiplication.

Suppose

$$
W\subseteq V
$$

where

- $V$ is a vector space.
- $W$ is a subset of $V$.

Then $W$ is called a **subspace** if it also satisfies all the vector space axioms.

---

**`Conditions for a Subspace`**

A subset $W$ of a vector space $V$ is a subspace if it satisfies the following three conditions:

`1. Zero Vector`

The zero vector must belong to the subset.

$$
0\in W
$$

---

`2. Closure under Addition`

If

$$
u,v\in W
$$

then

$$
u+v\in W
$$

---

`3. Closure under Scalar Multiplication`

If

$$
u\in W
$$

and

$$
k
$$

is any scalar, then

$$
ku\in W
$$

---

**`Example of a Subspace`**

Consider

$$
W=
\left\{
\begin{bmatrix}
x\\
0
\end{bmatrix}
:x\in\mathbb{R}
\right\}
$$

Every vector has the form

$$
\begin{bmatrix}
x\\
0
\end{bmatrix}
$$

This set contains the zero vector,

is closed under addition,

and is closed under scalar multiplication.

Therefore,

$$
W
$$

is a **subspace** of

$$
\mathbb{R}^2.
$$

---

**`Non-Example of a Subspace`**

Consider

$$
W=
\left\{
\begin{bmatrix}
x\\
1
\end{bmatrix}
:x\in\mathbb{R}
\right\}
$$

The zero vector

$$
\begin{bmatrix}
0\\
0
\end{bmatrix}
$$

does **not** belong to this set.

Hence,

$$
W
$$

is **not** a subspace.

---

**`Linear Combination`**

A **Linear Combination** is an expression obtained by multiplying vectors by scalars and then adding the results.

If

$$
v_1,v_2,\ldots,v_n
$$

are vectors and

$$
c_1,c_2,\ldots,c_n
$$

are scalars, then

$$
c_1v_1+c_2v_2+\cdots+c_nv_n
$$

is called a linear combination.

**Example**

Let

$$
v_1=
\begin{bmatrix}
1\\
2
\end{bmatrix},
\qquad
v_2=
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

Take

$$
c_1=2,
\qquad
c_2=-1
$$

Then

$$
2v_1-v_2=
2
\begin{bmatrix}
1\\
2
\end{bmatrix} -
\begin{bmatrix}
3\\
4
\end{bmatrix} =
\begin{bmatrix}
-1\\
0
\end{bmatrix}
$$

---

**`Span of a Set of Vectors`**

The **span** of a set of vectors is the collection of **all possible linear combinations** of those vectors.

If

$$
S=\{v_1,v_2,\ldots,v_n\}
$$

then

$$
\text{Span}(S) =
\left\{
c_1v_1+\cdots+c_nv_n
\right\}
$$

where

$$
c_1,c_2,\ldots,c_n
$$

are scalars.

**Example**

Let

$$
S=
\left\{
\begin{bmatrix}
1\\
0
\end{bmatrix},
\begin{bmatrix}
0\\
1
\end{bmatrix}
\right\}
$$

Every vector in

$$
\mathbb{R}^2
$$

can be written as

$$
a
\begin{bmatrix}
1\\
0
\end{bmatrix}
+
b
\begin{bmatrix}
0\\
1
\end{bmatrix} =
\begin{bmatrix}
a\\
b
\end{bmatrix}
$$

Therefore,

$$
\text{Span}(S)=\mathbb{R}^2
$$

---

**`Linear Independence and Linear Dependence`**

One of the most important concepts in Linear Algebra is determining whether a set of vectors is **independent** or **dependent**. These concepts help us understand whether a vector can be expressed using other vectors in the same set.

They are fundamental in finding the **basis**, **dimension**, and **span** of a vector space.

---

**`Linear Independence`**

A set of vectors is said to be **linearly independent** if **none of the vectors can be written as a linear combination of the remaining vectors**.

In other words, every vector contributes unique information to the vector space.

Mathematically, suppose

$$
v_1,v_2,\ldots,v_n
$$

are vectors.

They are linearly independent if

$$
c_1v_1+c_2v_2+\cdots+c_nv_n=0
$$

has only the **trivial solution**

$$
c_1=c_2=\cdots=c_n=0
$$

where

- $c_1,c_2,\ldots,c_n$ are scalars.
- The **zero vector** is represented by $0$.

**Example**

Consider

$$
v_1=
\begin{bmatrix}
1\\
0
\end{bmatrix},
\qquad
v_2=
\begin{bmatrix}
0\\
1
\end{bmatrix}
$$

These vectors cannot be written using each other.

Therefore,

$$
\{v_1,v_2\}
$$

is a **linearly independent set**.

---

**Example**

Consider

$$
v_1=
\begin{bmatrix}
1\\
2
\end{bmatrix},
\qquad
v_2=
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

Neither vector is a scalar multiple of the other.

Hence,

they are linearly independent.

---

**`Important Characteristics`**

- Every vector contributes new information.
- No vector is redundant.
- Forms a good candidate for a basis.
- Number of vectors cannot exceed the dimension of the vector space.

---

**`Linear Dependence`**

A set of vectors is called **linearly dependent** if **at least one vector can be written as a linear combination of the remaining vectors**.

This means one or more vectors are redundant.

Mathematically,

$$
c_1v_1+c_2v_2+\cdots+c_nv_n=0
$$

has a **non-trivial solution**, meaning

at least one scalar is not zero.

---

**Example**

Consider

$$
v_1=
\begin{bmatrix}
1\\
2
\end{bmatrix},
\qquad
v_2=
\begin{bmatrix}
2\\
4
\end{bmatrix}
$$

Notice

$$
v_2=2v_1
$$

Therefore,

one vector depends on the other.

Hence,

the vectors are **linearly dependent**.

---

**Example**

Consider

$$
v_1=
\begin{bmatrix}
1\\
0
\end{bmatrix},
\qquad
v_2=
\begin{bmatrix}
0\\
1
\end{bmatrix},
\qquad
v_3=
\begin{bmatrix}
1\\
1
\end{bmatrix}
$$

Observe

$$
v_3=v_1+v_2
$$

Thus,

the set is linearly dependent.

---

**Important Characteristics**

- At least one redundant vector exists.
- One vector can be removed without changing the span.
- Cannot be used directly as a basis.

---

`Difference Between Linear Independence and Dependence`

| Linear Independence | Linear Dependence |
|----------------------|-------------------|
| No vector depends on another | At least one vector depends on another |
| Only trivial solution exists | Non-trivial solution exists |
| No redundant vectors | Redundant vectors exist |
| Can form a basis | Cannot directly form a basis |

---

`Basis of a Vector Space`

A **Basis** is one of the most important concepts in Linear Algebra.

A basis is a set of vectors that

- are **linearly independent**, and
- span the entire vector space.

Thus, every vector in the vector space can be written as a unique linear combination of the basis vectors.

Mathematically,

If

$$
B=\{v_1,v_2,\ldots,v_n\}
$$

then

- the vectors are linearly independent.
- they span the vector space.

---

**Example**

The standard basis of

$$
\mathbb{R}^2
$$

is

$$
\left\{
\begin{bmatrix}
1\\
0
\end{bmatrix},
\begin{bmatrix}
0\\
1
\end{bmatrix}
\right\}
$$

Every vector

$$
\begin{bmatrix}
a\\
b
\end{bmatrix}
$$

can be written as

$$
a
\begin{bmatrix}
1\\
0
\end{bmatrix}
+
b
\begin{bmatrix}
0\\
1
\end{bmatrix}
$$

Hence,

these vectors form a basis.

---

`Standard Basis`

The most common basis is called the **Standard Basis**.

For

$$
\mathbb{R}^3
$$

the standard basis is

$$
e_1=
\begin{bmatrix}
1\\
0\\
0
\end{bmatrix},
\qquad
e_2=
\begin{bmatrix}
0\\
1\\
0
\end{bmatrix},
\qquad
e_3=
\begin{bmatrix}
0\\
0\\
1
\end{bmatrix}
$$

Every vector in

$$
\mathbb{R}^3
$$

can be represented using these vectors.

---

`Properties of a Basis`

A basis always satisfies:

- It spans the vector space.
- It is linearly independent.
- Every vector has a unique representation.
- Every finite-dimensional vector space has at least one basis.

---

`Dimension of a Vector Space`

The **Dimension** of a vector space is the **number of vectors in its basis**.

It tells us the minimum number of independent vectors required to describe the entire vector space.

It is denoted by

$$
\dim(V)
$$

---

**Examples**

For

$$
\mathbb{R}
$$

$$
\dim(\mathbb{R})=1
$$

---

For

$$
\mathbb{R}^2
$$

$$
\dim(\mathbb{R}^2)=2
$$

---

For

$$
\mathbb{R}^3
$$

$$
\dim(\mathbb{R}^3)=3
$$

---

**`Finite-Dimensional Vector Space`**

A vector space having a finite number of basis vectors.

Examples

$$
\mathbb{R}^2,\qquad
\mathbb{R}^3
$$

---

**`Infinite-Dimensional Vector Space`**

A vector space requiring infinitely many basis vectors.

Example

All polynomial functions

$$
P(x)
$$

---

**Coordinate Vector**

A **Coordinate Vector** represents a vector with respect to a particular basis.

Suppose

$$
B=\{v_1,v_2\}
$$

is a basis.

If

$$
u =
2v_1+5v_2
$$

then the coordinate vector of

$$
u
$$

relative to the basis

$$
B
$$

is

$$
[u]_B=
\begin{bmatrix}
2\\
5
\end{bmatrix}
$$

Coordinate vectors make computations easier and are widely used in computer graphics and machine learning.

---

**`Row Space`**

The **Row Space** of a matrix is the set of **all possible linear combinations of its rows**.

Suppose

$$
A=
\begin{bmatrix}
1&2\\
3&4
\end{bmatrix}
$$

Its row vectors are

$$
(1,2)
$$

and

$$
(3,4)
$$

The collection of all linear combinations of these rows forms the row space.

---

**`Importance`**

- Used in determining the rank of a matrix.
- Helps solve systems of linear equations.
- Describes information contained in the rows.

---

`Column Space`

The **Column Space** is the collection of **all linear combinations of the columns** of a matrix.

Example

$$
A=
\begin{bmatrix}
1&2\\
3&4
\end{bmatrix}
$$

Columns are

$$
\begin{bmatrix}
1\\
3
\end{bmatrix}
,
\qquad
\begin{bmatrix}
2\\
4
\end{bmatrix}
$$

Their span forms the **column space**.

---

**Importance**

- Determines whether a system

$$
Ax=b
$$

has a solution.

- Used in data science and machine learning.

- Determines the rank of the matrix.

---

**`Null Space (Kernel)`**

The **Null Space**, also called the **Kernel**, is the set of all vectors that satisfy

$$
Ax=0
$$

where

- $A$ is a matrix.
- $x$ is an unknown vector.

The null space contains every solution of the homogeneous system.

Mathematically,

$$
N(A)=
\{x:Ax=0\}
$$

---

**Example**

Consider

$$
A=
\begin{bmatrix}
1&1\\
2&2
\end{bmatrix}
$$

We solve

$$
Ax=0
$$

to find every vector satisfying the equation.

These vectors together form the null space.

---

**`Importance of Null Space`**

- Used to solve homogeneous systems.
- Determines linear dependence.
- Used in the Rank-Nullity Theorem.
- Important in machine learning, signal processing, and computer vision.

---

**`Rank of a Matrix`**

The **Rank** of a matrix is one of the most important concepts in Linear Algebra. It represents the **maximum number of linearly independent rows or columns** in a matrix.

In other words, the rank tells us how much **independent information** is contained in a matrix.

It is denoted by

$$
\mathrm{Rank}(A)
$$

where $A$ is a matrix.

---

The **rank of a matrix** is the dimension of its **row space** or **column space**.

Mathematically,

$$
\mathrm{Rank}(A) =
\dim(\text{Row Space}) =
\dim(\text{Column Space})
$$

The row rank and column rank of every matrix are always equal.

---

**Example**

Consider

$$
A=
\begin{bmatrix}
1&2\\
2&4
\end{bmatrix}
$$

The second row is

$$
2\times
\begin{bmatrix}
1&2
\end{bmatrix}
$$

Since one row depends on the other, there is only **one independent row**.

Therefore,

$$
\mathrm{Rank}(A)=1
$$

---

**Example**

Consider

$$
A=
\begin{bmatrix}
1&2\\
3&4
\end{bmatrix}
$$

Neither row is a multiple of the other.

Hence,

both rows are independent.

Therefore,

$$
\mathrm{Rank}(A)=2
$$

---

**`Properties of Rank`**

- The rank is always a non-negative integer.
- The rank cannot exceed the number of rows or columns.
- Row rank is always equal to column rank.
- A full-rank matrix has the maximum possible rank.
- Rank helps determine whether a system of linear equations has a unique solution.

---

**`Full Rank Matrix`**

A matrix is called a **Full Rank Matrix** if its rank is equal to the smaller of the number of rows and columns.

For a square matrix,

$$
\mathrm{Rank}(A)=n
$$

where

$$
A
$$

is an

$$
n\times n
$$

matrix.

**Example**

$$
A=
\begin{bmatrix}
1&2\\
3&5
\end{bmatrix}
$$

Since both rows are independent,

$$
\mathrm{Rank}(A)=2
$$

The matrix is **full rank**.

---

**`Nullity of a Matrix`**

The **Nullity** of a matrix is the **dimension of its null space (kernel)**.

It tells us the number of independent solutions of

$$
Ax=0
$$

Nullity is denoted by

$$
\mathrm{Nullity}(A)
$$

---

**`Definition`**

If

$$
N(A)
$$

represents the null space of matrix

$$
A
$$

then

$$
\mathrm{Nullity}(A) =
\dim(N(A))
$$

---

**Example**

Suppose

$$
A=
\begin{bmatrix}
1&2\\
2&4
\end{bmatrix}
$$

Its rank is

$$
1
$$

Since the matrix has

$$
2
$$

columns,

its nullity is

$$
2-1=1
$$

Therefore,

$$
\mathrm{Nullity}(A)=1
$$

---

**`Importance of Nullity`**

Nullity helps us determine

- the number of free variables,
- the number of independent solutions,
- whether vectors are linearly dependent,
- the dimension of the kernel of a linear transformation.

---

**`Rank–Nullity Theorem`**

The **Rank–Nullity Theorem** is one of the most fundamental theorems in Linear Algebra.

It establishes the relationship between the rank and nullity of a matrix.

If a matrix has

$$
n
$$

columns,

then

$$
\boxed{
\mathrm{Rank}(A)
+
\mathrm{Nullity}(A) =
n
}
$$

where

- Rank = Number of independent columns.
- Nullity = Dimension of the null space.
- $n$ = Total number of columns.

---

**Example**

Consider

$$
A=
\begin{bmatrix}
1&2&3\\
2&4&6
\end{bmatrix}
$$

There is only one independent row.

Hence,

$$
\mathrm{Rank}(A)=1
$$

The matrix has

$$
3
$$

columns.

Therefore,

$$
\mathrm{Nullity}(A) =
3-1 =
2
$$

Verification:

$$
1+2=3
$$

Thus,

the Rank–Nullity Theorem is satisfied.

---

**`Importance of the Rank–Nullity Theorem`**

The theorem helps us

- determine the number of free variables,
- solve homogeneous systems,
- study linear transformations,
- analyze matrix dimensions,
- understand vector spaces more deeply.

---

**`Properties of Vector Spaces`**

Every vector space satisfies several important properties.

---

`1. Closure Property`

If

$$
u,v\in V
$$

then

$$
u+v\in V
$$

Similarly,

$$
ku\in V
$$

for every scalar

$$
k.
$$

---

`2. Existence of Zero Vector`

Every vector space contains a unique zero vector.

$$
0\in V
$$

such that

$$
u+0=u
$$

---

`3. Existence of Additive Inverse`

For every vector

$$
u
$$

there exists another vector

$$
-u
$$

such that

$$
u+(-u)=0
$$

---

`4. Commutative Law`

$$
u+v=v+u
$$

---

`5. Associative Law`

$$
(u+v)+w=u+(v+w)
$$

---

`6. Scalar Identity`

Multiplying any vector by

$$
1
$$

does not change the vector.

$$
1u=u
$$

---

`7. Distributive Laws`

Vector spaces satisfy

$$
k(u+v)=ku+kv
$$

and

$$
(a+b)u=au+bu
$$

---

`8. Compatibility of Scalar Multiplication`

$$
(ab)u=a(bu)
$$

---

`9. Unique Zero Vector`

Every vector space contains exactly one zero vector.

---

`10. Unique Additive Inverse`

Every vector has exactly one additive inverse.

---

**`Important Formulas`**

`Linear Combination`

$$
v =
c_1v_1
+
c_2v_2
+
\cdots
+
c_nv_n
$$

---

`Span`

$$
\mathrm{Span}(S) =
\{
c_1v_1+\cdots+c_nv_n
\}
$$

---

`Basis`

A basis is a set of vectors that is

- Linearly Independent
- Spans the Vector Space

---

**`Dimension`**

$$
\dim(V) =
\text{Number of Basis Vectors}
$$

---

`Rank`

$$
\mathrm{Rank}(A) =
\dim(\text{Column Space}) =
\dim(\text{Row Space})
$$

---

`Nullity`

$$
\mathrm{Nullity}(A) =
\dim(\text{Null Space})
$$

---

`Rank–Nullity Theorem`

$$
\boxed{
\mathrm{Rank}(A)
+
\mathrm{Nullity}(A) =
n
}
$$

---

**`Key Takeaways`**

- A vector space is a set of vectors satisfying ten fundamental axioms.
- Linear combinations generate new vectors from existing vectors.
- The span of a set contains all possible linear combinations of its vectors.
- Linearly independent vectors provide unique information, while dependent vectors contain redundancy.
- A basis is a minimal set of independent vectors that spans the entire vector space.
- The dimension of a vector space equals the number of vectors in its basis.
- The row space, column space, and null space describe different aspects of a matrix.
- Rank measures the amount of independent information in a matrix.
- Nullity measures the dimension of the null space.
- The Rank–Nullity Theorem connects rank and nullity through the number of columns.
- Vector spaces are fundamental in mathematics, engineering, artificial intelligence, machine learning, computer graphics, robotics, and many other scientific disciplines.

---

## **`6. The Geometry of Linear Equations`**

Linear Algebra is not only about manipulating equations and matrices. One of its most powerful ideas is that **linear equations have geometric meanings**.

A system of linear equations can be understood in several different ways:

- **Algebraically** — as equations involving unknown variables
- **Geometrically** — as lines, planes, and their intersections
- **Vectorially** — as linear combinations of vectors
- **Matrix-wise** — as a matrix equation such as $A\vec{x}=\vec{b}$

For example:

$$
x+y=4
$$

is an algebraic equation, but geometrically it represents a **line** in $\mathbb{R}^2$.

Similarly,

$$
x+y+z=4
$$

represents a **plane** in $\mathbb{R}^3$.

Understanding these connections is essential for studying:

- Matrices
- Gaussian Elimination
- Vector Spaces
- Linear Independence
- Span
- Column Space
- Null Space
- Linear Transformations

---

### **`1. Linear Equation in Two Variables`**

A linear equation in two variables has the general form:

$$
ax+by=c
$$

where $a$, $b$, and $c$ are constants.

For example:

$$
2x+3y=6
$$

This equation contains two variables:

$$
x,\ y
$$

and each variable has a power of $1$.

Therefore, it is a linear equation.

---

**`Geometric Meaning`**

A linear equation in two variables represents a **straight line** in the two-dimensional coordinate plane.

The coordinate plane is represented by:

$$
\mathbb{R}^2
$$

A point $(x,y)$ lies on the line if it satisfies the equation.

For example:

$$
x+y=4
$$

Some solutions are:

$$
(0,4)
$$

$$
(1,3)
$$

$$
(2,2)
$$

$$
(3,1)
$$

and:

$$
(4,0)
$$

All these points lie on the same straight line.

Therefore:

$$
\boxed{x+y=4}
$$

represents a line in $\mathbb{R}^2$.

---

**`Slope-Intercept Form`**

A linear equation can often be written as:

$$
y=mx+c
$$

where:

- $m$ = slope
- $c$ = $y$-intercept

For example:

$$
2x+y=4
$$

Rearrange:

$$
y=-2x+4
$$

Therefore:

$$
m=-2
$$

and:

$$
c=4
$$

---

### **`2. Geometric Meaning of a System`**

A **system of linear equations** consists of two or more equations that must be satisfied simultaneously.

Consider:

$$
\begin{aligned}
x+y&=4\\
x-y&=2
\end{aligned}
$$

We need values of $x$ and $y$ that satisfy **both equations at the same time**.

Adding the equations:

$$
(x+y)+(x-y)=4+2
$$

$$
2x=6
$$

Therefore:

$$
x=3
$$

Substitute into:

$$
x+y=4
$$

$$
3+y=4
$$

Thus:

$$
y=1
$$

Therefore:

$$
\boxed{(x,y)=(3,1)}
$$

---

**`Geometric Interpretation`**

Each equation represents a line.

The solution:

$$
(3,1)
$$

is the point where the two lines intersect.

Therefore:

$$
\boxed{
\text{Solution of system} =
\text{Intersection of the lines}
}
$$

This is one of the most important geometric interpretations of linear equations.

---

### **`3. Three Possibilities for Two Lines`**

When two linear equations are represented geometrically, there are three possible situations.

---

**`Case 1: One Solution`**

The two lines intersect at exactly one point.

For example:

$$
\begin{aligned}
x+y&=4\\
x-y&=2
\end{aligned}
$$

The lines intersect at:

$$
(3,1)
$$

Therefore:

$$
\boxed{\text{One unique solution}}
$$

---

**`Case 2: No Solution`**

Two lines can be parallel.

For example:

$$
x+y=2
$$

and:

$$
x+y=5
$$

Both lines have the same slope but different intercepts.

Therefore, they never intersect.

Hence:

$$
\boxed{\text{No solution}}
$$

Algebraically, elimination produces something like:

$$
0=3
$$

which is impossible.

---

**`Case 3: Infinitely Many Solutions`**

Two equations can represent the same line.

For example:

$$
x+y=4
$$

and:

$$
2x+2y=8
$$

The second equation is simply twice the first.

Therefore, both equations describe exactly the same line.

Every point on that line satisfies both equations.

Hence:

$$
\boxed{\text{Infinitely many solutions}}
$$

---

### **`4. Linear Equations in Three Variables`**

A linear equation in three variables has the form:

$$
ax+by+cz=d
$$

For example:

$$
x+2y+3z=6
$$

The variables are:

$$
x,\ y,\ z
$$

Unlike a linear equation in two variables, which represents a line, a linear equation in three variables represents a **plane** in $\mathbb{R}^3$.

---

**`Example`**

Consider:

$$
x+y+z=6
$$

Some points satisfying this equation are:

$$
(6,0,0)
$$

$$
(0,6,0)
$$

$$
(0,0,6)
$$

and many others.

All these points lie on the same plane.

Therefore:

$$
\boxed{
x+y+z=6
}
$$

represents a plane in $\mathbb{R}^3$.

---

### **`5. System of Equations in Three Dimensions`**

Consider:

$$
\begin{aligned}
x+y+z&=6\\
x-y+z&=2\\
2x+y-z&=3
\end{aligned}
$$

Each equation represents a plane.

The solution of the system is the set of points that belong to **all three planes simultaneously**.

Depending on the equations, the planes can produce:

- One common point
- No common point
- A common line
- The same plane

---

**`Unique Solution`**

Three planes can intersect at exactly one point.

Then:

$$
\boxed{\text{One solution}}
$$

---

**`Infinite Solutions`**

The planes may share a common line.

Then every point on that line is a solution.

Therefore:

$$
\boxed{\text{Infinitely many solutions}}
$$

---

**`No Solution`**

The planes may have no common point.

Therefore:

$$
\boxed{\text{No solution}}
$$

---

### **`6. Geometry of $A\vec{x}=\vec{b}$`**

A system of linear equations can be written compactly as:

$$
\boxed{
A\vec{x}=\vec{b}
}
$$

Suppose:

$$
A=
\begin{bmatrix}
a&b\\
c&d
\end{bmatrix}
$$

and:

$$
\vec{x} =
\begin{bmatrix}
x\\
y
\end{bmatrix}
$$

Then:

$$
A\vec{x} =
\begin{bmatrix}
a&b\\
c&d
\end{bmatrix}
\begin{bmatrix}
x\\
y
\end{bmatrix}
$$

which gives:

$$
A\vec{x} =
\begin{bmatrix}
ax+by\\
cx+dy
\end{bmatrix}
$$

Therefore:

$$
A\vec{x}=\vec{b}
$$

is simply a compact representation of a system of linear equations.

---

**`Example`**

Consider:

$$
\begin{aligned}
x+2y&=5\\
3x+4y&=11
\end{aligned}
$$

This can be written as:

$$
\begin{bmatrix}
1&2\\
3&4
\end{bmatrix}
\begin{bmatrix}
x\\
y
\end{bmatrix} =
\begin{bmatrix}
5\\
11
\end{bmatrix}
$$

Here:

$$
A=
\begin{bmatrix}
1&2\\
3&4
\end{bmatrix}
$$

$$
\vec{x}=
\begin{bmatrix}
x\\
y
\end{bmatrix}
$$

and:

$$
\vec{b}=
\begin{bmatrix}
5\\
11
\end{bmatrix}
$$

---

### **`7. Row Picture`**

The **row picture** views a system as a collection of equations.

Consider:

$$
\begin{aligned}
x+y&=4\\
2x-y&=2
\end{aligned}
$$

The first row represents:

$$
x+y=4
$$

The second row represents:

$$
2x-y=2
$$

Each equation represents a line.

The solution is the point where the two lines intersect.

Therefore:

$$
\boxed{
\text{Row Picture} =
\text{Intersection of equations}
}
$$

---

**`In Three Dimensions`**

For a system with three variables:

$$
\begin{aligned}
a_1x+b_1y+c_1z&=d_1\\
a_2x+b_2y+c_2z&=d_2\\
a_3x+b_3y+c_3z&=d_3
\end{aligned}
$$

Each equation represents a plane.

The solution is the common intersection of these planes.

---

### **`8. Column Picture`**

The same equation:

$$
A\vec{x}=\vec{b}
$$

can be interpreted using the **columns of $A$**.

Consider:

$$
A=
\begin{bmatrix}
1&2\\
3&4
\end{bmatrix}
$$

Then:

$$
A
\begin{bmatrix}
x\\
y
\end{bmatrix} =
x
\begin{bmatrix}
1\\
3
\end{bmatrix}
+
y
\begin{bmatrix}
2\\
4
\end{bmatrix}
$$

Therefore:

$$
x
\begin{bmatrix}
1\\
3
\end{bmatrix}
+
y
\begin{bmatrix}
2\\
4
\end{bmatrix} =
\vec{b}
$$

The question becomes:

> Can $\vec{b}$ be produced as a linear combination of the columns of $A$?

This is the **column picture**.

---

### **`9. Row Picture vs Column Picture`**

The row and column pictures describe the same equation:

$$
\boxed{
A\vec{x}=\vec{b}
}
$$

| Row Picture | Column Picture |
|---|---|
| Focuses on equations | Focuses on vectors |
| Rows represent equations | Columns represent vectors |
| Geometric objects intersect | Vectors are combined |
| Solution is an intersection | $\vec{b}$ is a linear combination |
| Useful for geometry of equations | Useful for span and vector spaces |

---

**`Example`**

Consider:

$$
A=
\begin{bmatrix}
1&2\\
3&4
\end{bmatrix}
$$

and:

$$
\vec{b} =
\begin{bmatrix}
5\\
11
\end{bmatrix}
$$

**`Row Picture`**

Solve:

$$
\begin{aligned}
x+2y&=5\\
3x+4y&=11
\end{aligned}
$$

The solution is the intersection of two lines.

**`Column Picture`**

Write:

$$
x
\begin{bmatrix}
1\\
3
\end{bmatrix}
+
y
\begin{bmatrix}
2\\
4
\end{bmatrix} =
\begin{bmatrix}
5\\
11
\end{bmatrix}
$$

Now we are asking whether the target vector can be constructed from the two columns.

---

### **`10. Homogeneous Linear Equations`**

A system is called **homogeneous** when the right-hand side is the zero vector.

It has the form:

$$
\boxed{
A\vec{x}=\vec{0}
}
$$

For example:

$$
\begin{aligned}
x+y&=0\\
2x-y&=0
\end{aligned}
$$

The right-hand side is:

$$
\begin{bmatrix}
0\\
0
\end{bmatrix}
$$

---

**`Important Property`**

Every homogeneous system has at least one solution:

$$
\boxed{
\vec{x}=\vec{0}
}
$$

This is because:

$$
A\vec{0}=\vec{0}
$$

for every matrix $A$.

---

### **`11. Trivial Solution`**

For a homogeneous system:

$$
A\vec{x}=\vec{0}
$$

the solution:

$$
\boxed{
\vec{x}=\vec{0}
}
$$

is called the **trivial solution**.

For example:

$$
\begin{bmatrix}
1&2\\
3&4
\end{bmatrix}
\begin{bmatrix}
x\\
y
\end{bmatrix} =
\begin{bmatrix}
0\\
0
\end{bmatrix}
$$

may have only:

$$
x=0,\qquad y=0
$$

as its solution.

---

### **`12. Non-Trivial Solutions`**

A homogeneous system can also have solutions other than the zero vector.

These are called **non-trivial solutions**.

Consider:

$$
x+2y=0
$$

Let:

$$
y=1
$$

Then:

$$
x=-2
$$

Therefore:

$$
\begin{bmatrix}
-2\\
1
\end{bmatrix}
$$

is a non-trivial solution.

We can write the complete solution as:

$$
\begin{bmatrix}
x\\
y
\end{bmatrix} =
t
\begin{bmatrix}
-2\\
1
\end{bmatrix}
$$

where:

$$
t\in\mathbb{R}
$$

This represents a line through the origin.

---

### **`13. Geometry of Homogeneous Systems`**

Consider:

$$
x+y=0
$$

This equation represents a line passing through the origin.

Why?

Because:

$$
(0,0)
$$

satisfies:

$$
0+0=0
$$

More generally:

$$
A\vec{x}=\vec{0}
$$

always contains the origin.

The set of all solutions of a homogeneous system forms a **subspace**.

---

**`Examples`**

In $\mathbb{R}^2$, the solution set can be:

- Only the origin
- A line through the origin
- The entire $\mathbb{R}^2$

In $\mathbb{R}^3$, it can be:

- Only the origin
- A line through the origin
- A plane through the origin
- All of $\mathbb{R}^3$

---

### **`14. Linear Combinations`**

A **linear combination** is an expression formed by multiplying vectors by scalars and adding them.

Suppose:

$$
\vec{v}_1=
\begin{bmatrix}
1\\
2
\end{bmatrix}
$$

and:

$$
\vec{v}_2=
\begin{bmatrix}
3\\
1
\end{bmatrix}
$$

A linear combination is:

$$
c_1\vec{v}_1+c_2\vec{v}_2
$$

where $c_1$ and $c_2$ are scalars.

---

**`Example`**

Take:

$$
c_1=2
$$

and:

$$
c_2=3
$$

Then:

$$
2\vec{v}_1+3\vec{v}_2
$$

becomes:

$$
2
\begin{bmatrix}
1\\
2
\end{bmatrix}
+
3
\begin{bmatrix}
3\\
1
\end{bmatrix}
$$

$$
= \begin{bmatrix}
2\\
4
\end{bmatrix}
+
\begin{bmatrix}
9\\
3
\end{bmatrix}
$$

Therefore:

$$
\boxed{
\begin{bmatrix}
11\\
7
\end{bmatrix}
}
$$

is a linear combination of $\vec{v}_1$ and $\vec{v}_2$.

---

### **`15. Span`**

The **span** of a collection of vectors is the set of **all possible linear combinations** of those vectors.

For vectors:

$$
\vec{v}_1,\vec{v}_2,\ldots,\vec{v}_n
$$

we write:

$$
\boxed{
\mathrm{span}
\{\vec{v}_1,\vec{v}_2,\ldots,\vec{v}_n\}
}
$$

Formally:

$$
\mathrm{span}
\{\vec{v}_1,\ldots,\vec{v}_n\} =
\left\{
c_1\vec{v}_1+\cdots+c_n\vec{v}_n
:
c_i\in\mathbb{R}
\right\}
$$

---

**`Example`**

Let:

$$
\vec{v}_1=
\begin{bmatrix}
1\\
0
\end{bmatrix}
$$

and:

$$
\vec{v}_2=
\begin{bmatrix}
0\\
1
\end{bmatrix}
$$

A general linear combination is:

$$
c_1
\begin{bmatrix}
1\\
0
\end{bmatrix}
+
c_2
\begin{bmatrix}
0\\
1
\end{bmatrix}
$$

which gives:

$$
\begin{bmatrix}
c_1\\
c_2
\end{bmatrix}
$$

Since $c_1$ and $c_2$ can be any real numbers:

$$
\boxed{
\mathrm{span}\{\vec{v}_1,\vec{v}_2\} =
\mathbb{R}^2
}
$$

---

### **`16. Geometry of Span`**

The geometry of a span depends on the number and relationship of the vectors.

**`1. One Non-Zero Vector in`** $\mathbb{R}^2$

The span is a line passing through the origin.

$$
\boxed{\text{Line}}
$$

**`2. Two Independent Vectors in`** $\mathbb{R}^2$

Their span is the entire plane.

$$
\boxed{\mathbb{R}^2}
$$

**`3. One Non-Zero Vector in`** $\mathbb{R}^3$

Its span is a line through the origin.

<br>

**`4. Two Independent Vectors in`** $\mathbb{R}^3$

Their span is a plane through the origin.

<br>

**`5. Three Independent Vectors in`** $\mathbb{R}^3$

Their span is:

$$
\boxed{\mathbb{R}^3}
$$

---

### **`17. Linear Independence and Geometry`**

Vectors are **linearly independent** if none of the vectors can be written as a linear combination of the others.

For vectors:

$$
\vec{v}_1,\vec{v}_2,\ldots,\vec{v}_n
$$

they are linearly independent if:

$$
c_1\vec{v}_1+
c_2\vec{v}_2+
\cdots+
c_n\vec{v}_n =
\vec{0}
$$

has only the solution:

$$
c_1=c_2=\cdots=c_n=0
$$

---

**`Geometric Meaning`**

Consider two vectors:

$$
\vec{v}_1=
\begin{bmatrix}
1\\
2
\end{bmatrix}
$$

and:

$$
\vec{v}_2=
\begin{bmatrix}
2\\
4
\end{bmatrix}
$$

Notice:

$$
\vec{v}_2=2\vec{v}_1
$$

Therefore, the vectors point in the same direction.

They are linearly dependent.

---

**`Independent Vectors`**

Consider:

$$
\vec{v}_1=
\begin{bmatrix}
1\\
0
\end{bmatrix}
$$

and:

$$
\vec{v}_2=
\begin{bmatrix}
0\\
1
\end{bmatrix}
$$

Neither vector can be created from the other.

Therefore:

$$
\boxed{
\vec{v}_1,\vec{v}_2
\text{ are linearly independent}
}
$$

---

### **`18. Intersection of Planes`**

In $\mathbb{R}^3$, a linear equation:

$$
ax+by+cz=d
$$

represents a plane.

Two planes can have different geometric relationships.

---

**`Case 1: Intersecting Planes`**

Two non-parallel planes generally intersect in a line.

Therefore:

$$
\boxed{\text{Intersection = line}}
$$

---

**`Case 2: Parallel Planes`**

Two distinct parallel planes never intersect.

Therefore:

$$
\boxed{\text{No intersection}}
$$

---

**`Case 3: Same Plane`**

Two equations may represent the exact same plane.

Then they have infinitely many common points.

Therefore:

$$
\boxed{\text{Intersection = entire plane}}
$$

---

### **`19. Geometric Meaning of a Unique Solution`**

A system has a **unique solution** when all the equations have exactly one common point.

In $\mathbb{R}^2$:

$$
\boxed{
\text{Two lines intersect at exactly one point}
}
$$

In $\mathbb{R}^3$:

$$
\boxed{
\text{Three planes intersect at exactly one point}
}
$$

For example:

$$
\begin{aligned}
x+y&=4\\
x-y&=2
\end{aligned}
$$

gives:

$$
(x,y)=(3,1)
$$

Therefore:

$$
\boxed{\text{Unique solution}}
$$

---

### **`20. Geometric Meaning of No Solution`**

A system has **no solution** when the equations have no common point.

For example:

$$
\begin{aligned}
x+y&=2\\
x+y&=5
\end{aligned}
$$

Subtracting the equations:

$$
0=3
$$

which is impossible.

Geometrically, the two equations represent parallel lines.

Therefore:

$$
\boxed{\text{No solution}}
$$

---

### **`21. Geometric Meaning of Infinitely Many Solutions`**

A system has infinitely many solutions when there are infinitely many points satisfying all the equations.

Consider:

$$
\begin{aligned}
x+y&=4\\
2x+2y&=8
\end{aligned}
$$

The second equation is twice the first:

$$
2(x+y)=2(4)
$$

Therefore, both equations represent the same line.

Every point on this line is a solution.

Hence:

$$
\boxed{\text{Infinitely many solutions}}
$$

---

**`Parametric Form`**

Starting with:

$$
x+y=4
$$

Let:

$$
y=t
$$

Then:

$$
x=4-t
$$

Therefore:

$$
\boxed{
x=4-t,\qquad y=t
}
$$

where:

$$
t\in\mathbb{R}
$$

This represents infinitely many points on the line.

---

### **`22. Geometry and Gaussian Elimination`**

**Gaussian Elimination** is a systematic method for simplifying a system of linear equations.

The important idea is:

> **Row operations simplify the equations without changing their solution set.**

Consider:

$$
\begin{aligned}
x+y&=4\\
2x+2y&=8
\end{aligned}
$$

The augmented matrix is:

$$
\left[
\begin{array}{cc|c}
1&1&4\\
2&2&8
\end{array}
\right]
$$

Apply:

$$
R_2\rightarrow R_2-2R_1
$$

Then:

$$
\left[
\begin{array}{cc|c}
1&1&4\\
0&0&0
\end{array}
\right]
$$

The second row represents:

$$
0=0
$$

This means the second equation did not provide any additional independent information.

Geometrically, this makes sense because both equations represented the **same line**.

---

**`Gaussian Elimination and Geometry`**

Gaussian Elimination helps reveal the geometric structure of a system.

For example:

**`One pivot for two variables`**

There is a free variable, which can produce infinitely many solutions.

<br>

**`Two pivots for two variables`**

Both variables are determined, producing a unique solution.

<br>

**`A row such as`**

$$
[0\quad0\mid c]
$$

where:

$$
c\neq0
$$

means:

$$
0=c
$$

which is impossible.

Therefore:

$$
\boxed{\text{No solution}}
$$

---

### **`Important Connections`**

The geometry of linear equations connects several major ideas in Linear Algebra:

$$
\boxed{
\text{Linear Equations}
\rightarrow
\text{Lines and Planes}
\rightarrow
\text{Systems}
\rightarrow
\text{Matrices}
}
$$

and:

$$
\boxed{
A\vec{x}=\vec{b}
\rightarrow
\text{Row Picture}
\rightarrow
\text{Column Picture}
}
$$

and:

$$
\boxed{
\text{Linear Combinations}
\rightarrow
\text{Span}
\rightarrow
\text{Linear Independence}
}
$$

---