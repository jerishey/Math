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

### `Features of Scalar`
```bash
1. Represents a single quantity such as temperature, accuracy or cost.

2. Serves as the building block for forming higher-dimensional data structures like vectors and matrices.

3. Use Case: Used in machine learning to represent loss functions, accuracy values or statistical measures such as mean and variance.

4. Advantage: Simple to store and compute; forms the foundation for complex mathematical models.

5. Disadvantage: Cannot represent any direction, relationship or multidimensional structure.
```

### `Scalar Quantities :` 
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
<hr>

## `2. Vector`
In mathematics, vectors are fundamental objects that represent quantities with both magnitude and direction. They are widely used in various branches of mathematics, physics, engineering, computer science, and other disciplines.

### `Key Features of Vectors:`

`1. Magnitude :` A vector has a size or length called its magnitude.
- The size or length of the vector.
- Denoted by $|\vec{v}|$ or $\|\vec{v}\|$

`2. Direction :` A vector always points in a specific direction.
- The direction of the vector in space.
- Represented by the arrowhead that indicates where the vector points.


### `Real-life analogy of Vectors`
To better understand vectors, consider a situation where a football coach is training a goalkeeper to pass the ball. The coach needs to instruct the goalkeeper:
- `Direction:` Where to send the ball (toward another player or a specific region).
- `Magnitude:` How hard to kick the ball (the strength of the pass).
<hr>

### `Representation of Vector`
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

## `Types of Vectors`
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


## `3. Introduction to Matrices`
Matrices are rectangular arrays of numbers, symbols, or characters where all of these elements are arranged in each row and column.

- A matrix is identified by its order, which is given in the form of rows ⨯ columns, and the location of each element is given by the row and column it belongs to.
- A matrix is represented as ([P]m⨯n), where P is the matrix, m is the number of rows, and n is the number of columns.

### <b> `Example` </b>

`1. Matrix A (2×2) :`

A=
$\begin{bmatrix}
1 & 2\\
3 & 4
\end{bmatrix}_{2\times2}$

`2. Matrix B (3×3) :`

B=
$\begin{bmatrix}
1 & -1 & 2\\
3 & 2 & 6\\
4 & -2 & 5
\end{bmatrix}_{3\times3}$

Here, A is a 2×2 matrix (2 rows and 2 columns) and B is a 3×3 matrix (3 rows and 3 columns).
<hr>

### `Order of Matrix :` 
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

#### `Type of Matrices Based on Order of Matrix` 
The order of a matrix indicates its dimension and also defines the various types of matrices. The following are some different matrices that are classified based on the order of a matrix.

`1. Singleton Matrix :` A singleton matrix is defined as a matrix that has only one element, i.e., it has only one row and one column. So, the order of a singleton matrix is "1 × 1"
- Matrix given below is a singleton matrix.

        A = [ 23 ]

`2. Row Matrix :` A row matrix is defined as a matrix that has only one row. A matrix "A = [aij]" is said to be a row matrix if the order of the matrix is "1 × n"
- Matrix given below is a row matrix of order "1 × 3"

        B = [ -1 0 1 ]

`3. Column Matrix :` A column matrix is defined as a matrix that has only one column. The matrix "A = [aij]" is said to be a column matrix if the order of the matrix is "m × 1"
- Matrix given below is a row matrix of order "4 × 1"

            | p |
            | q |
      C =   | r |
            | s |

`4. Rectangular Matrix :` A rectangular matrix is defined as a matrix that does not have an equal number of rows and columns. The order of a rectangular matrix that has "m" rows and "n" columns is "m × n" 
- Matrix given below is a row matrix of order "2 × 3"

        D = | 12 14 16 |
            | 6   7  8 |

`5. Square Matrix :` A square matrix is defined as a matrix that has an equal number of rows and columns. The order of a square matrix that has "n" rows and "n" columns is "n × n" 
- Matrix given below is a row matrix of order "2 × 2"

        E = | 3  6 |
            | 9 15 |

#### <b>`Important Points on Order of Matrix` </b>
```bash
1. The first number in the order of a matrix will always represent the number of rows in the matrix, while the second number represents the number of columns in the matrix.
2. The addition or subtraction of any two matrices is possible if the order of the two matrices is the same.
3. Multiplication of any two matrices is possible only when the number of columns in the first matrix is equal to the number of rows in the second matrix.
4. If the order of a matrix is "m × n," then the order of its transpose matrix will be "n × m," where a transpose matrix is formed by changing the rows of a matrix into columns and its columns into rows.
```