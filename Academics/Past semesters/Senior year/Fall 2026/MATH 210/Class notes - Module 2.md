# MATH 210 | Module 2

## **Chapter 2.3**

**Linear Transformation**

- **Eigenvector:** a non-zero vector that, when multiplied by a matrix, is scaled linearly (as if being multiplied by a scalar)

  - If *Av* = *kv* (for a scalar *k*) then *v* is the eigenvector of *A*
  - Eigenvectors do not change direction after transformation

- **Eigenvalue:** the quantity of the scalar that transforms the eigenvector

- 

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

**Determinant**

- The determinant of a 1×1 matrix $[a]$ is a
- The determinant of a 2×2 matrix 