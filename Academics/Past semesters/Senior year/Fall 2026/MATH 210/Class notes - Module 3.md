# MATH 210 | Module 3

## **Chapter 8.1.5**

**Linear Dependence & Independence ([video](https://www.youtube.com/watch?v=9kDpbZCK62Y))**

- **Definition**
  - If we have three vectors, and **one can be written as the combination of the others**, then all three are **linearly dependent**
  - If we have three vectors, and **none of them can be written as the combination of the others**, then all three are **linearly independent**
- **Determining linear (in)dependence with RREF**
  - For **linear independence**, the **coefficients** of the vectors in a sum equation **must be 0**
  - For **linear dependence**, the **coefficients** of the vectors in a sum equation **must be nonzero**
  - If **non-zero coefficients do not exist**, the vectors are **linearly independent**
  - If **non-zero coefficients exist**, the vectors are **linearly dependent**
  - If the coefficients include a **free variable**, the vectors are **linearly dependent**
- **Determining linear (in)dependence with determinants**
  - For square matrices, if the **determinant is 0**, the vectors are **linearly dependent**
  - If the **determinant is nonzero**, the vectors are **linearly independent**
- **Linear (in)dependence and orthogonality**
  - If the vectors in a set are orthogonal, they are not necessarily linearly independent
  - If the vectors in a set are orthogonal and nonzero, they are necessarily linearly independent
- The same rules apply to matrices

## Chapter 8.2

**Gram-Schmidt Orthonormalization**

- **The Gram-Schmidt algorithm can be used to turn a set of linearly independent vectors into a set of orthogonal vectors**

  - Note that the new vectors are still linearly independent
  - Once we have the new set of orthogonal vectors, we can create a set of orthonormal vectors by dividing each vector by its length

- **Process**

  [[Screenshot 2026-11-17 at 9.14.14 PM.png]]

## Chapter 8.3

**Orthogonal and Symmetric Matrices**

- **An orthogonal matrix is a square matrix with orthonormal column vectors**

- **Properties of orthogonal matrices**

  - $Q^TQ = I$
  - $Q^{-1}$
  - $QQ^T = QQ^{-1} = I$

- Symmetric matrices will only ever have real number solutions and orthogonal eigenvectors

- These matrices can be diagonalized ($A = PDP^{-1}$), but P is an orthogonal matrix, composed of the normalized column vectors

- **Diagonalizing orthogonal matrices**

  [[Screenshot 2026-11-19 at 1.07.37 AM.png]]

## Chapter 8.4.1 - 8.4.2

**Singular Value Decomposition**

- Note that diagonal matrices don’t have to be square

- The singular value decomposition (SVD) is a way of writing a matrix as

  [[Screenshot 2026-11-19 at 1.10.12 AM.png]]

  [[Screenshot 2026-11-18 at 11.54.23 PM.png]]

- **Steps of SVD**

  - Compute $A^TA$, which is a symmetric matrix
  - Find the eigenvalues of $A^TA$, which are positive numbers
  - Find the eigenvectors of $A^TA$, which are orthogonal vectors
  - Build the diagonal matrix $Σ$ out of singular values (the square roots of the eigenvalues)
  - Rescale the vectors to have length 1
  - Build the matrix $V$ from these vectors
  - Multiply $A$ by the rescaled vectors of $A^TA$, then divide the product by the singular values, to find orthogonal vectors
  - Find additional vectors that are linearly independent to thes ones
  - Apply the Gram-Schmidt process to orthogonalize the vectors and rescale
  - Build the matrix $U$ from these vectors

## Chapter 8.5

**Image Compression**

[[Screenshot 2026-11-19 at 1.18.43 AM.png]]

- To find the ratio, divide the new dimensions by the original dimensions

## Chapter 9.1

**Introduction to Derivatives**

- Derivatives are related to slope and tangent

## Chapter 9.2

**Calculating Derivatives**

- **Derivative rules**

  - Derivative of a constant = 0

  - Derivative of x = 1

  - Power rule: $x^n = nx^{n-1}$

  - Other rules

    [[Screenshot 2026-11-19 at 1.21.13 AM.png]]

**Notes from practice exam**

- If A is symmetric, A inverse is also symmetric, and A is orthogonally diagonalizable
- If M is orthogonally diagonalizable, then so is $M²$
- If U and V are orthogonal matrices, then UV is orthogonal too
- If U is orthogonal, then its columns are linearly independent
- If U is orthogonal, the length of Uv equals the length of v (for any vector v)
- If C is a 7 x 3 matrix, then $C^TC$ has at most 3 non-zero eigenvalues
- If S is a symmetric matrix with non-negative eigenvalues, then the diagonalization of S is the same as the SVD of S
- The tangent line is horizontal where the derivative = 0