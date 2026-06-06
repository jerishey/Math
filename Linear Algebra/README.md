# Linear Algebra
Linear Algebra is the branch of mathematics that focuses on the study of vectors, vector spaces, matrices, and linear transformations. It deals with linear equations, linear functions, and their representations through matrices and determinants.

`Uses of Linear Algebra`
```bash
1. Machine Learning: Used to represent and process data using vectors and matrices in algorithms.

2. Artificial Intelligence: Helps in building and optimizing neural networks using matrix operations.

3. Data Science: Used to organize, analyze, and reduce large datasets efficiently.

4. Computer Graphics: Used to perform transformations like rotation, scaling, and translation of objects.

5. Image Processing: Represents images as matrices to apply filters and enhancements.

6. Search Engines: Used to measure similarity between data using vector representations.
```
## Introduction
Linear Algebra is the branch of mathematics that studies vectors, matrices, and linear equations and how they interact.

### `Types of Linear Algebra`
Linear Algebra is divided into different branches based on the difficulty level of topics, which are

`1. Foundations of Linear Algebra :` The foundations of Linear Algebra consist of the basic concepts that are required before studying advanced topics such as vector spaces, eigenvalues, and matrix decompositions.
```bash
1. Scalars : Quantities with magnitude only (e.g., speed, mass, volume, etc.).

2. Vectors : Quantities with both direction and magnitude, elements of a vector space (e.g., velocity, weight, friction, etc).

3. Vector Space : A collection of vectors that can be added and scaled by scalars.

4. Matrix : A rectangular array of numbers arranged in rows and columns.

5. Matrix Operations : Arithmetic operations like addition, multiplication, and transposition.
```

`2. Abstract Linear Algebra :` Abstract Linear Algebra studies the theoretical structures behind vectors, matrices, and linear transformations. Instead of focusing mainly on calculations, it focuses on understanding the underlying mathematical concepts and proving their properties.
```bash
1. Linear Transformations : A linear transformation is a special kind of function between vector spaces that preserves the operations of
- Vector addition and Subtraction
- Scalar multiplication

2. Eigenvalues and Eigenvectors : Eigenvalues and eigenvectors are fundamental concepts in linear algebra.
- An eigenvector is a vector whose direction doesn’t change when a matrix is applied.
- The eigenvalue is the factor by which that vector is scaled.

Mathematically:

Av = λv

Where:
 A = Square matrix
 v = Eigenvector (non-zero vector)
 λ = Eigenvalue (scalar value)

3. Singular Value Decomposition : Singular Value Decomposition (SVD) is a powerful mathematical technique used in signal processing, statistics, and machine learning.

- It decomposes a matrix into three other matrices, where one represents the rotation, another the scaling, and the third the final rotation.
- It's essential for identifying the intrinsic geometric structure of data.
```

`3. Applied Linear Algebra :` Applied Linear Algebra focuses on using linear algebra concepts to solve real-world problems in science, engineering, computer science, data science, machine learning, economics, and many other fields.
<br>
Unlike Abstract Linear Algebra, which emphasizes theory and proofs, Applied Linear Algebra emphasizes computation, algorithms, and practical applications.
```bash
1. Linear Programming : Linear programming is a method to achieve the best outcome in a mathematical model whose requirements are represented by linear relationships.

- It is widely used in business and economics to maximize profit or minimize cost while considering constraints.
- This is a technique for optimizing (maximizing or minimizing) a linear objective function, subject to linear equality and inequality constraints.

2. Linear Equation Systems : Systems of linear equations involve multiple linear equations that share the same set of variables.

- The solution to these systems is the set of values that satisfy all equations simultaneously, which can be found using various methods, including substitution, elimination, and matrix operations.

3. Gaussian Elimination : Gaussian elimination is a systematic method for solving systems of linear equations.

- It involves applying a series of operations to transform the system's matrix into its row echelon form or reduced row echelon form, making it easier to solve for the variables.
- It is a step-by-step procedure to simplify a system of linear equations into a form that's easier to solve.
```

## Foundations of Linear Algebra
Linear algebra builds on a small set of core ideas; scalars, vectors, matrices, and the equations that connect them.

### `1. Scalar`
Scalar is a single numerical value that conveys magnitude but no direction or dimension. It is a zero-dimensional entity, meaning it cannot be decomposed into smaller parts or represented along any axis. 
<br>
Scalars serve as the fundamental units of computation in mathematics, physics and computer science.

```bash
1. Represents a single quantity such as temperature, accuracy or cost.

2. Serves as the building block for forming higher-dimensional data structures like vectors and matrices.

3. Use Case: Used in machine learning to represent loss functions, accuracy values or statistical measures such as mean and variance.

4. Advantage: Simple to store and compute; forms the foundation for complex mathematical models.

5. Disadvantage: Cannot represent any direction, relationship or multidimensional structure.
```

`Scalar Quantities :` A scalar quantity is a physical quantity that has only magnitude and no direction.

- It is described by a single numerical value, typically with units.
- Scalars represent quantities where direction is not relevant, such as temperature, mass, time, and energy.
- They can be added, subtracted, multiplied, and divided using standard arithmetic operations.
- Scalars are easier to work with compared to vector quantities since they don’t require considering directions or components.

<b>Example: </b>
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

### `2. Vector`
In mathematics, vectors are fundamental objects that represent quantities with both magnitude and direction. They are widely used in various branches of mathematics, physics, engineering, computer science, and other disciplines.
<hr>

### `Key Features of Vectors:`

`1. Magnitude :` A vector has a size or length called its magnitude.
- The size or length of the vector.
- Denoted by $|\vec{v}|$ or $\|\vec{v}\|$

`2. Direction :` A vector always points in a specific direction.
- The direction of the vector in space.
- Represented by the arrowhead that indicates where the vector points.
<hr>

### `Real-life analogy of Vectors`
To better understand vectors, consider a situation where a football coach is training a goalkeeper to pass the ball. The coach needs to instruct the goalkeeper:
- `Direction:` Where to send the ball (toward another player or a specific region).
- `Magnitude:` How hard to kick the ball (the strength of the pass).
<hr>

### `Representation of Vector`
Vectors are represented by taking an arrow above the quantity to indicate that it has both magnitude and direction.
- The Force vector is represented $\vec{F}$ where the arrow above F represents that it is a vector quantity. 
<br>
<hr>

Vectors can also be represented by taking their respective magnitude in x, y, and z-directions.
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
<hr>

`2. Magnitude of Vectors :` The magnitude of a vector represents the strength of the vector. We can calculate the magnitude of the vector by taking the square root of the sum of the squares of each component in the x, y, and z directions. 
<br>
<hr>

For any vector: $\vec{A} = a\hat{i} + b\hat{j} + c\hat{k}$, The magnitude of the vector is denoted by $|\vec{A}|$ or $\|\vec{A}\|$ and is given by :

$$
|\vec{A}| = \sqrt{a^2 + b^2 + c^2}
$$

- The magnitude of a vector is a scalar value.
<hr>

`3. Components of Vectors :` A vector can be easily broken into its two components which represent the value of the vector in perpendicular dimensions.
<br>
In a 2-D coordinate system, we can easily break the vector into two components namely the x-component and y-component.
<hr>

For any vector $\vec{A}$ making an angle $\theta$ with the positive x-axis:

- X-component is $A_x$ and its value is 

$$
A_x = A \cos\theta
$$

- Y-component is $A_y$ and its value is

$$
A_y = A \sin\theta
$$

where θ is the angle formed by the vector with the positive x-axis. Also, the magnitude of the vector A is calculated using the formula,

$$
|\vec{A}| = \sqrt{A_x^2 + A_y^2}
$$
<hr>

`4. Angle Between Two Vectors :` If two vectors in the 2-D plane intersect each other then the angle between them can easily be calculated using the dot product of the vector formula. 
<br>
We know that for two vectors vector a, and vector b their dot product is given by :

$$
\vec{a} \cdot \vec{b} = |\vec{a}| \, |\vec{b}| \cos\theta
$$

Explanation:
- $| \vec{a}|$ = magnitude of vector $\vec{a}$
- $| \vec{b}|$ = magnitude of vector $\vec{b}$
- θ = angle between the vectors
<hr>
We can easily calculate the dot product of the two vectors using the dot product rule and then taking the inverse trigonometric cos function on both sides we can easily calculate the angle between two vectors as :

$$
\theta = \cos^{-1}\left(\frac{\vec{a}\cdot\vec{b}}{|\vec{a}|\,|\vec{b}|}\right)
$$
<hr>

### `Types of Vectors`
Vectors can be classified into different categories on the basis of their magnitude and direction.

<i> `The various types of vectors are :` 

`1. Zero Vector :` A zero vector is the vector that has no magnitude and no direction. A zero vector is written as $\vec{0}$ or 0 and looks like:
- In 2D: (0, 0)
- In 3D: (0, 0, 0)

<b>Feature :</b>
```bash
1. Its magnitude is 0.
2. It does not point in any direction.
3. It acts like the additive identity for vectors. (Adding it to any vector leaves the vector unchanged.)
```
`2. Unit Vector :` Unit vectors are the vectors that have a magnitude (length) of exactly 1.

- It shows direction only, not size.
- Any vector can be converted into a unit vector by dividing it by its magnitude.
- Represented by the symbol '^' such as $\hat{a}$.
<hr>

We define a unit vector in each 3-D axis as,
- Unit vector in the x-direction is i
- Unit vector in the y-direction is j
- Unit vector in the z-direction is k

Also, the magnitude of this vector is,

|i| = 1, |j| = 1, |k| = 1
<hr>

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
<hr>

`3. Equal Vectors :` Equal vectors are vectors that have the same magnitude and direction. In simple words, two vectors are said to be equal if they have the same length and direction; otherwise, they are unequal vectors.

<b>`Equal Vector Formula :`</b>
For Two Vectors A and B to be equal, the following two conditions must be met:

- Same Magnitude: Length of A must be equal to the length of B.
- Same Direction: Direction of A must be the same as the direction of B.

`Properties of Equal Vector`
```bash
1. If Two vectors A and B have same length and point in the same direction they are said to be equal else they would be unequal.

2. Equal Vectors are vectors with equal coordinates and same signs so equal vectors can be called as parallel vectors but the reverse may or may not be true.

3. Equal vectors have same components.

4. Position of the vectors does not affect the equality of vectors, Vectors are considered equal as long as their magnitude and direction matches, irrespective of where they are located in the coordinate system.

5. Equal Vector will still be equal if we add / subtract / divide / multiply both the vectors with the same quantity (can be scalar or vector ). For example say A = B and C is another vector then A - C = B - C.
```