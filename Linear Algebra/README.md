# Linear Algebra
Linear Algebra is the branch of mathematics that focuses on the study of vectors, vector spaces, matrices, and linear transformations. It deals with linear equations, linear functions, and their representations through matrices and determinants.

```bash
1. Vector : A vector is an ordered list of numbers that represents a quantity with magnitude and direction.

Example:
v = [2, 4, 6]

2. Matrix : A matrix is a rectangular arrangement of numbers in rows and columns.

Example:
[1  2]
[3  4]

3. Linear Equation : A linear equation is an equation in which each variable has a power of 1.

Example:
ax+by=c

4. Scalar : A scalar is a single number used to multiply or scale a vector.

Example:
3 × [1, 2] = [3, 6]

5. Dot Product : The dot product is the multiplication of two vectors that results in a single number.

Example:
[1,2] • [3,4] = (1×3 + 2×4) = 11

6. Eigenvalues & Eigenvectors : 
- Eigenvector: A vector whose direction does not change after a transformation
- Eigenvalue: A scalar that shows how much the vector is scaled
```

## Uses of Linear Algebra
```bash
1. Machine Learning: Used to represent and process data using vectors and matrices in algorithms.

2. Artificial Intelligence: Helps in building and optimizing neural networks using matrix operations.

3. Data Science: Used to organize, analyze, and reduce large datasets efficiently.

4. Computer Graphics: Used to perform transformations like rotation, scaling, and translation of objects.

5. Image Processing: Represents images as matrices to apply filters and enhancements.

6. Search Engines: Used to measure similarity between data using vector representations.
```

## Types of Linear Algebra

`1. Foundations of Linear Algebra :` Elementary linear algebra introduces the foundational concepts that form the building blocks of the subject. It covers basic operations on matrices, solving systems of equations, and understanding vectors.
```bash
1. Scalars : Quantities with magnitude only (e.g., speed, mass, volume, etc.).
2. Vectors : Quantities with both direction and magnitude, elements of a vector space (e.g., velocity, weight, friction, etc).
3. Vector Space : A collection of vectors that can be added and scaled by scalars.
4. Matrix : A rectangular array of numbers arranged in rows and columns.
5. Matrix Operations : Arithmetic operations like addition, multiplication, and transposition.
```

`2. Abstract Linear Algebra :` Advanced/Abstract linear algebra mostly covers all the advanced topics related to linear algebra, such as Linear function, Linear transformation, Eigenvectors, and Eigenvalues.
<br>

<i> <b>1. Linear Transformations : </b> A linear transformation is a special kind of function between vector spaces that preserves the operations of
1. Vector addition and Subtraction
2. Scalar multiplication

```bash 
In other words, if T is a linear transformation, then for any vectors u and v and scalar c:

T(u + v) = T(u) + T(v)
T(cu) = cT(u)
```
<b> 2. Eigenvalues and Eigenvectors : </b> Eigenvalues and eigenvectors are fundamental concepts in linear algebra.

- An eigenvector is a vector whose direction doesn’t change when a matrix is applied.
- The eigenvalue is the factor by which that vector is scaled.


Mathematically:

Av = λv

Where:
- **A** = Square matrix
- **v** = Eigenvector (non-zero vector)
- **λ** = Eigenvalue (scalar value)

<b> Singular Value Decomposition : </b> Singular Value Decomposition (SVD) is a powerful mathematical technique used in signal processing, statistics, and machine learning.

- It decomposes a matrix into three other matrices, where one represents the rotation, another the scaling, and the third the final rotation.
- It's essential for identifying the intrinsic geometric structure of data.
</i>