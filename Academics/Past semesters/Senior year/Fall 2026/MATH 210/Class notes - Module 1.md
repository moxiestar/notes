# MATH 210 | Module 1

## **Chapter 1.1**

**Linear Equations**

- **A linear equation** is an equation that can be written as the sum of the coefficients times variables equaling another number
  - **Example:** 4x - 5y + 7.3z = 27
- **A system of linear equations** is a set of linear equations involving the same variables
  - **Example:** 4r + 3s = 2 | r + s - t = -5 | s = 2t | r - 3s + t = 0
- **A solution to a system of linear equations** is a set of values that satisfies each equation

**Matrices**

- **A matrix** is an array of numbers
- Linear equations can be rewritten as “augmented” matrices, where both the coefficients and the sum (number on the other side of the equals sign) are written as entries in the matrix

## **Chapter 1.2**

**Systems of Linear Equations**

- **A linear equation** is an equation that can be written as the sum of the coefficients times variables equaling another number

## **Chapter 1.3**

**Reduced Row Echelon Form (RREF)**

- **A matrix can be written in RREF,** a form that isolates the solutions to the underlying system of equations

  [[Screenshot 2026-10-24 at 2.03.20 PM.png]]

- **Rules of RREF**

  - First non-zero entry on each row must be 1
  - The leading 1s fall in a staircase pattern
  - Each leading 1 has a 0 above it
  - Only the last row can contain all 0s

- **To convert a matrix to RREF**, we can perform any of the following **elementary row operations**

  - Switching two rows
  - Adding or subtracting one row from another
  - Multiplying a row by a constant
  - Multiplying a row by a constant and adding it to another row

## **Chapter 1.4**

**Matrix Solutions**

- **A matrix or system of linear equations can have…**
  - **No** solutions (inconsistent)
  - **One** unique solution (consistent)
  - **Infinite** solutions (consistent)
- **Determining matrix solutions**
  - If there’s an inconsistent row (0 0 0 1), the matrix has no solutions
  - If there are no inconsistencies, and at least one row with all 0s and free variables (variables with no noted solution), the matrix has infinite solutions 
  - If there are no inconsistencies and leading 1s in every row, the matrix has one unique solution
- **Example problems**
  - **Finding k for various solutions**

    [[Screenshot 2026-10-24 at 2.08.43 PM.png]]

## **Chapter 2.1**

**Matrix Addition and Basic Multiplication**

- **Matrix review**
  - **A matrix** is an array of numbers
  - **The dimensions of a matrix** are the number of rows and columns
    - Rows always come first 
  - **The elements of a matrix** are the individual numbers
- **Example problems**
  - **Finding the matrix X for a simple matrix equation**

    [[Screenshot 2026-10-24 at 2.14.35 PM.png]]
  - **Finding scalars *a* and *b* for a simple vector equation**

    [[Screenshot 2026-10-24 at 2.15.26 PM.png]]

## **Chapter 2.2**

**Matrix Multiplication**

- **Matrices and column vectors**
  - **Column vector:** a matrix that has only one column (n x 1)
  - **Row vector:** a matrix that has only one row (1 x n)
- **Multiplying larger matrices**
  - For A, an m x r matrix, and B, an r x n matrix, their product AB is the m x n matrix
  - **Steps**
    1. **Multiply the first row of A by the first column of B** and add the resulting product to find the first entry of the first row of AB
    2. **Multiply the first row of A by the second column of B** and add the resulting product to find the second entry of the first row of AB
    3. **Multiply the first row of A by the nth column of B** and add the resulting product to find the nth entry of the first row of AB
    4. **Multiply the second row of A by the first column of B** and add the resulting product to find the first entry of the second row of AB
    5. **Multiply the second row of A by the second column of B** and add the resulting product to find the second entry of the second row of AB
    6. **Multiply the second row of A by the nth column of B** and add the resulting product to find the nth entry of the second row of AB
- **Example problems**
  - **Multiplying matrices Y and Z**

    [[Screenshot 2026-10-24 at 2.21.19 PM.png]]

## **Chapter 2.3**

**Vectors**

- **A vector** can be defined as the line that connects **an initial point** and **a terminal point**
  - Vectors are drawn as the line that connects these two points on the Cartesian plane
  - The components of a vector are the coordinates of the terminal piont
- **Finding the length of a vector**

  [[Screenshot 2026-10-24 at 2.32.49 PM.png]]
- **Example problems**
  - Adding and graphing multiple vectors

    [[Screenshot 2026-10-24 at 2.31.24 PM.png]]

## **Chapter 2.4**

**Vector Equations**

- **Finding solutions to vector equations of the form Ax = b**
  - **If the equation Ax = b has infinitely many solutions**, then the equation Ax = 0 will also have **infinitely many solutions**
  - **If the equation Ax = b has one unique solution**, then the equation Ax = 0 will also have **one unique solution**
  - **If the equation Ax = b has no solutions**, then the equation Ax = 0 could have either **infinitely many solutions** or **one unique solution**

    [[Screenshot 2026-10-24 at 2.43.18 PM.png]]

    [[Screenshot 2026-10-24 at 2.43.44 PM.png]]
- **Example problems**
  - **Solving for Ax = b**

    [[Screenshot 2026-10-24 at 2.40.04 PM.png]]
  - **Solving Ax = 0** 

    [[Screenshot 2026-10-24 at 2.45.59 PM.png]]
  - Finding solutions to Ax = b based on solutions ot Ax = 0 

    [[Screenshot 2026-10-24 at 2.46.24 PM.png]]

     