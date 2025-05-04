# Matrix Template Library in C++

A templated C++ library for handling matrix operations efficiently, supporting various functionalities like addition, multiplication, submatrix extraction, transpose, and row/column traversal. Designed to optimize computational efficiency, especially in matrix multiplication order.

## Features

- **Matrix Operations**:
  - Transpose of a matrix
  - Extract a submatrix with specified dimensions
  - Addition of two matrices
  - Efficient multiplication of three matrices (optimal order selection)
- **Traversal Methods**:
  - Row-major traversal
  - Column-major traversal
- **Template Support**: Works with any data type (e.g., `int`, `float`, `double`).
- **Memory Efficiency**: Submatrix and transpose operations share data with the original matrix (no deep copy). Direct assignments create deep copies.

## Installation

1. **Prerequisites**: A C++ compiler (e.g., `g++`).
2. **Compilation**:
   ```bash
   g++ main.cpp -o matrix_app

## Run

   ```bash
   ./matrix_app
   ```
## Usage

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
Choose from one of the following matrix operations:
1. Transpose of a matrix
2. Finding a sub-matrix
3. Addition of two matrices
4. Effective Multiplication of 3 matrices
Press Any Key For Exit...
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

# Example Workflow

## Transpose:
1. Select option 1.  
2. Enter matrix dimensions and elements.  
3. View the transposed matrix.  

## Submatrix Extraction:
1. Select option 2.  
2. Enter the original matrix, then specify submatrix dimensions.  
3. The submatrix is displayed.  

## Matrix Addition:
1. Select option 3.  
2. Input two matrices of the same dimensions.  
3. The result is shown.  

## Efficient Multiplication:
1. Select option 4.  
2. Input three matrices (A, B, C).  
3. The library automatically computes `A*(B*C)` or `(A*B)*C` based on dimension optimization.

---

# Implementation Details

## Class `MatOp<T>`

### Constructors:
- `MatOp(int m, int n)`: Initializes an `m x n` matrix with zeros.
- `MatOp(int m, int n, T ***result)`: Shares data with an existing matrix (used for submatrix).

### Key Methods:
- `MatrixTranspose()`: Returns a transposed matrix (shared data).
- `SubMatrixOperation()`: Extracts a submatrix.
- `MatrixAddition()` and `MatrixMultiplication()`: Static methods for operations.
- `RowTraversal()` and `ColTraversal()`: Print matrix in row/column order.

### Efficient Multiplication:
- For three matrices, the library checks dimensions to minimize computational complexity  
  (e.g., computes `A*(B*C)` if B has larger dimensions).
