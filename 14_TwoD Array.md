# 📚 Two-Dimensional Arrays in Java

---

## 1. Theory: 2D Array Declaration

A **two-dimensional (2D) array** in Java is essentially an **array of arrays**.  
It is used to represent **matrices, tables, or grids** of elements arranged in rows and columns.

### 🔹 Declaration
```java
datatype[][] arrayName;
```
or
```java
datatype arrayName[][];
```
or
```java
datatype[] arrayName[];
```

### 🔹 Initialization

#### a) Static Initialization
Assign values directly at the time of declaration:
```java
int[][] matrix = { 
    {1, 2, 3}, 
    {4, 5, 6}, 
    {7, 8, 9} 
};
```
This creates a **3x3 matrix**.

#### b) Dynamic Initialization
Create an empty matrix with predefined size:
```java
int[][] matrix = new int[3][3]; // 3 rows, 3 columns
matrix[0][0] = 1;
matrix[0][1] = 2;
```
Here, all elements are initialized to **0** by default.

---

## 2. Matrix Operations

A 2D array is commonly used for **matrix operations** such as:

1. **Matrix Addition** → Add corresponding elements of two matrices.
2. **Matrix Subtraction** → Subtract elements of one matrix from another.
3. **Matrix Multiplication** → Multiply rows of one matrix with columns of another.
4. **Transpose** → Convert rows into columns and vice versa.

---

## 3. Coding: Matrix Programs

### a) Matrix Addition
```java
public class MatrixAddition {
    public static void main(String[] args) {
        int[][] A = {{1, 2, 3}, {4, 5, 6}};
        int[][] B = {{7, 8, 9}, {10, 11, 12}};
        int[][] C = new int[2][3];

        for (int i = 0; i < A.length; i++) {
            for (int j = 0; j < A[0].length; j++) {
                C[i][j] = A[i][j] + B[i][j];
            }
        }

        System.out.println("Matrix Addition:");
        for (int[] row : C) {
            for (int val : row) {
                System.out.print(val + " ");
            }
            System.out.println();
        }
    }
}
```

### b) Matrix Multiplication
```java
public class MatrixMultiplication {
    public static void main(String[] args) {
        int[][] A = {{1, 2, 3}, {4, 5, 6}};
        int[][] B = {{7, 8}, {9, 10}, {11, 12}};
        int[][] C = new int[2][2];

        for (int i = 0; i < A.length; i++) {
            for (int j = 0; j < B[0].length; j++) {
                for (int k = 0; k < B.length; k++) {
                    C[i][j] += A[i][k] * B[k][j];
                }
            }
        }

        System.out.println("Matrix Multiplication:");
        for (int[] row : C) {
            for (int val : row) {
                System.out.print(val + " ");
            }
            System.out.println();
        }
    }
}
```

### c) Matrix Transpose
```java
public class MatrixTranspose {
    public static void main(String[] args) {
        int[][] A = {{1, 2, 3}, {4, 5, 6}};
        int[][] T = new int[3][2];

        for (int i = 0; i < A.length; i++) {
            for (int j = 0; j < A[0].length; j++) {
                T[j][i] = A[i][j];
            }
        }

        System.out.println("Transpose:");
        for (int[] row : T) {
            for (int val : row) {
                System.out.print(val + " ");
            }
            System.out.println();
        }
    }
}
```

---

## 4. Practice: 2D Array Exercises

### Q1: How do you traverse a 2D array?
You use **nested loops** → one for rows and one for columns.

```java
for (int i = 0; i < arr.length; i++) {
    for (int j = 0; j < arr[i].length; j++) {
        System.out.print(arr[i][j] + " ");
    }
    System.out.println();
}
```

---

### Q2: What is a Jagged Array?
A **jagged array** is a 2D array where rows may have different lengths.  
Unlike a matrix, not all rows need the same number of columns.

```java
int[][] jagged = new int[3][];
jagged[0] = new int[2];  // row 1 has 2 columns
jagged[1] = new int[4];  // row 2 has 4 columns
jagged[2] = new int[3];  // row 3 has 3 columns
```

---

### Q3: How do you pass 2D arrays to methods?
You can pass a 2D array just like a 1D array.

```java
public class Pass2DArray {
    static void printArray(int[][] arr) {
        for (int[] row : arr) {
            for (int val : row) {
                System.out.print(val + " ");
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        int[][] matrix = {{1,2,3}, {4,5,6}};
        printArray(matrix);
    }
}
```

---

## ✅ Summary
- **2D arrays** represent matrices or tables.  
- They can be declared, initialized, and traversed using nested loops.  
- **Matrix operations** such as addition, multiplication, and transpose are implemented using 2D arrays.  
- **Jagged arrays** allow irregular row sizes.  
- **Passing 2D arrays to methods** works the same as with 1D arrays.  

---
