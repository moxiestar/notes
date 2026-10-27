# MATH 210 | Module 2

## **Chapter 2.3**

**Linear Transformation**

- **Eigenvector:** a non-zero vector that, when multiplied by a matrix, is scaled linearly (as if being multiplied by a scalar)

  - If *Av* = *kv* (for a scalar *k*) then *v* is the eigenvector of *A*
  - Eigenvectors do not change direction after transformation

- **Eigenvalue:** the quantity of the scalar that transforms the eigenvector

- **Example problems**

  - **Graphing a matrix with no eigenvectors**

    [[Screenshot 2026-10-26 at 9.00.46 PM.png]]

  - **Graphing a matrix with one eigenvector**

    [[Screenshot 2026-10-26 at 9.01.22 PM.png]]

## **Chapter 3.1**

**Transpose**

- **The transpose of a matrix $A$, denoted $A^T$,** is the matrix found by switching the rows and columns (the first row becomes the first column)

  [[Screenshot 2026-10-26 at 9.43.57 PM.png]]

- **Transpose rules**

  - $(A + B)^T = A^T + B^T$
  - $(AB)^T ≠ A^T(B^T)$
    - But $(AB)^T = B^T(A^T)$
  - $(kA)^T = kA^T$
  - $(A^{-1})^T = (A^T)^{-1}$
  - $(A^T)^T = A$

- **Symmetry and skew-symmetry**

  - A square matrix A is **symmetric** if $A = A^T$
    - Note that $A + A^T$ is **always symmetric**
    - Note that $AA^T$ is **always symmetric**
  - A square matrix B is **skew-symmetric** if $-B = B^T$
    - Note that $B - B^T$ is **always skew-symmetric**
  - **For any square matrix A, it can be written as the sum of a symmetric matrix and a skew symmetric matrix**
    - **Equation:** $A = \frac{1}{2}(A + A^T) + \frac{1}{2}(A - A^T)$

- **Example problems**

  - **Writing a matrix as the sum of a symmetric and skew-symmetric matrix**

    [[Screenshot 2026-10-26 at 9.52.50 PM.png]]

## **Chapter 3.2**

**Trace**

- **The trace of a square matrix A** is the sum of its diagonal entries
- **Trace rules,** for square matrices A and B and scalar K
  - $tr(A + B) = trA + trB$
  - $tr(A - B) = trA - trB$
  - $tr(kA) = k(tr(A))$
  - $tr(AB) = tr(BA)$
  - $tr(A^T) = tr(A)$ ← **the trace of the transpose is just the trace**
  - $tr(A^{-1})$ is the sum of the reciprocals of the eigenvalues of A

## **Chapter 3.3**

**Determinants**

- **The determinant of a 1×1 matrix** $[a]$ is $a$

- **The determinant of a 2×2 matrix** $ [[a,b],[c,d]] $ is $ad-bc$

- **The determinant of a 3×3 matrix** is a little more complicated

  [[Screenshot 2026-10-26 at 10.00.49 PM.png]]

- **Determinant rules**

  - **For a square matrix A, the determinant indicates if the matrix is invertible**

    - **If the determinant ≠ 0,** the matrix is invertible
    - **If the determinant = 0,** the matrix is not invertible

  - When finding the determinant of a matrix, use the row with the most 0s if possible

  - Remember negative and positive rules of different entries in the matrix

    [[Screenshot 2026-10-26 at 10.10.45 PM.png]]

- **Example problems**

  - **Finding the determinant of a 3×3 matrix**

    [[Screenshot 2026-10-26 at 10.09.25 PM.png]]

## **Chapter 3.4**

**Properties of Determinants**

- For any square matrix A, if two rows or columns are identical, then the determinant is 0

- **Row operation rules**

  - Switching any two rows of a matrix will make the determinant negative

  - Multiplying a row by a scalar will multiply the determinant by that scalar

  - Multiplying a row of A by a scalar, then adding the resulting row to another row, does not change the determinant

    [[Screenshot 2026-10-26 at 10.13.02 PM.png]]

- **Interactions between determinants and other matrix operations**

  - $det(kA) = k^ndet(A)$
  - $det(A^T) = det(A)$
  - $det(AB) = det(A)det(B)$
  - If A is invertible, then $det(A^{-1}) = \frac{1}{det(A)}$

- **Interactions between determinants and row reductions**

  - If a square matrix A reduces to a matrix with a row of 0s, its determinant equals 0
  - If a square matrix A reduces to the identity matrix, its determinant cannot equal 0
  - If a square matrix A is invertible, its determinant cannot equal 0
  - If a square matrix A is not invertible, its determinant equals 0

- **Example problems**

  - **Finding the determinant based on elementary row operations**

    [[Screenshot 2026-10-26 at 10.40.32 PM.png]]

  - **Determining which matrices are invertible**

    [[Screenshot 2026-10-26 at 10.43.34 PM.png]]

**Triangular matrices**

- **An upper triangular matrix** is a matrix with all entries equaling 0 below the diagonal
- **A lower triangular matrix** is a matrix with all entries equaling 0 above the diagonal
- **A triangular matrix** can refer to either one
- **The determinant of a triangular matrix** is the product of its entries along the diagonal

## **Chapter 4.1**

**Eigenvalues & Eigenvectors**

- **For a square matrix A, if there is a scalar λ and a non-zero vector x such that Ax = λx…**

  - Then λ is an eigenvalue of A
  - Then x is an eigenvector of A
  - **Note that** not every matrix has eigenvalues and eigenvectors

- **Process of finding eigenvalues and eigenvectors from the Ax = λx equation**

  [[Screenshot 2026-10-26 at 11.02.24 PM.png]]

  [[Screenshot 2026-10-26 at 11.10.04 PM.png]]

- **Example problems**

  - **Defining basic eigenvalues and eigenvectors**

    [[Screenshot 2026-10-26 at 10.52.33 PM.png]]

  - **Finding eigenvalues and eigenvectors for 2×2 matrices**

    [[Screenshot 2026-10-26 at 11.03.29 PM.png]]

  - **Finding eigenvalues and eigenvectors for a 2×2 matrix**

    [[Screenshot 2026-10-26 at 11.11.31 PM.png]]

## **Chapter 4.2**

**Properties of Eigenvalues**

- **Eigenvalues rules**

  - **The eigenvalues for triangular matrices are the diagonal entries of the matrix**

  - **The trace of of a matrix** is the sum of the eigenvalues

  - **The determinant of a matrix** is the product of the eigenvalues of a matrix

  - **If a is an eigenvalue for A,** then a² is an eigenvalue for A²

  - **If a is an eigenvalue for A,** then 4a is an eigenvalue for 4A

  - **If A is invertible, and a is an eigenvalue for A,** then $\frac{1}{a}$ is an eigenvalue for $A^{-1}$

  - **The eigenvalues of $A$** are the **same** as the eigenvalues of $A^T$

  - **The eigenvalues of $A^{-1}$** are reciprocals of the eigenvalues of $A$

    [[Screenshot 2026-10-26 at 11.43.48 PM.png]]

  - **It is only possible to have an eigenvalue of 0** if the original matrix includes 0s and is not invertible (and therefore its determinant is 0)

    [[Screenshot 2026-10-26 at 11.47.11 PM.png]]

- **Example problems**

  - **Finding the eigenvalues for an upper triangular matrix**

    [[Screenshot 2026-10-26 at 11.39.30 PM.png]]

## **Chapter 6.2**

**Diagonal Matrices**

- **A diagonal matrix is a square matrix** with its only non-zero entries on the diagonal

- **A square matrix A is diagonalizable** if $A = PDP^{-1}$ for a diagonal matrix D and an invertible matrix P

  - We can take advantage of this equation to cancel things out

    [[Screenshot 2026-10-27 at 12.29.21 AM.png]]

- **A square matrix A can be diagonalized by…**

  1. **Finding the eigenvalues** ($λ_1$ through $λ_n$) and populate D with them
  2. Find the eigenvector for each eigenvalue ($v_1$ through $v_n$) and populate P with them (in the same order as D)

- **Diagonal matrix rules**

  - Multiplying a square matrix A by a diagonal matrix D (to find DA) involves multiplying each row of A by a corresponding entry of D
  - Multiplying a diagonal matrix D by a square matrix A (to find AD) involves multiplying each column of A by a corresponding entry of D

- **Example problems**

  - **Diagonalizing a matrix**

    [[Screenshot 2026-10-27 at 12.20.13 AM.png]]

  - **Finding matrices P and D to diagonalize matrix A**

    [[Screenshot 2026-10-27 at 12.20.40 AM.png]]

    [[Screenshot 2026-10-27 at 12.21.01 AM.png]]

  - **Diagonalizing a 3×3 matrix**

    [[Screenshot 2026-10-27 at 12.28.15 AM.png]]

    [[Screenshot 2026-10-27 at 12.28.23 AM.png]]

  - **Finding the determinant of a square matrix via diagonalization**

  [[Screenshot 2026-10-27 at 12.29.50 AM.png]]

## **Chapter 8.1**

**Dot Products and Orthogonal Vectors**

- **A dot product is found by multiplying two column vectors straight across**

  [[Screenshot 2026-10-27 at 12.42.18 AM.png]]
- **Dot products** are commutative, distributive, movable, and have positive sums (greater than or equal to 0)

**Unit vectors**

- **A unit vector** is a vector of length 1
  - **To rescale a vector to a unit vector, we divide it by its current length**

    [[Screenshot 2026-10-27 at 12.44.23 AM.png]]

 **Orthogonal vectors**

- **Two vectors, v and w, are said to be orthogonal** if their dot product equals 0
- **Two vectors, v and w, are said to be normal** if their dot product equals 0 and they are both unit vectors
- **A set of vectors is said to be orthonormal** if their inner vectors all have dot products of 0
- **A set of vectors is said to be orthonormal** if their inner vectors are all orthogonal unit vectors

  [[Screenshot 2026-10-27 at 12.47.14 AM.png]]

**Parallel and perpendicular vectors**

- **Two vectors, v and w, are said to be perpendicular** if their dot product equals 0
- **Two vectors, v and w, are said to be parallel** if $v = kw$ for some constant $k$
- **Example problems**
  - **Graphing vectors to find the angle between them**

    [[Screenshot 2026-10-27 at 12.48.14 AM.png]]

     