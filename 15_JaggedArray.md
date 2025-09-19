# 📘 Jagged Array in Java

## ✅ Definition
A **jagged array** is an **array of arrays where each row can have a different number of columns**.  
Unlike a **2D array** (matrix) where every row must have the same number of elements, in a **jagged array** the length of each row can be different.

---

## ✅ Representation

### Normal 2D Array (Matrix)
```
Row 1 → [1, 2, 3]
Row 2 → [4, 5, 6]
Row 3 → [7, 8, 9]
```

Every row has equal columns.

### Jagged Array
```
Row 1 → [1, 2, 3]
Row 2 → [4, 5]
Row 3 → [6, 7, 8, 9]
```

Each row has **different length**.

---

## ✅ Example Code

```java
public class JaggedArrayExample {
    public static void main(String[] args) {
        // Declare jagged array with 3 rows
        int[][] jagged = new int[3][];

        // Initialize rows with different column sizes
        jagged[0] = new int[3]; // row 1 has 3 elements
        jagged[1] = new int[2]; // row 2 has 2 elements
        jagged[2] = new int[4]; // row 3 has 4 elements

        // Assign values
        jagged[0][0] = 1; jagged[0][1] = 2; jagged[0][2] = 3;
        jagged[1][0] = 4; jagged[1][1] = 5;
        jagged[2][0] = 6; jagged[2][1] = 7; jagged[2][2] = 8; jagged[2][3] = 9;

        // Print jagged array
        for (int i = 0; i < jagged.length; i++) {
            for (int j = 0; j < jagged[i].length; j++) {
                System.out.print(jagged[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

### ✅ Output
```
1 2 3
4 5
6 7 8 9
```

---

# 📌 Problems on Jagged Array

## 1. Store Marks of Students (Unequal Subjects per Student)
- Student 1 → 3 subjects  
- Student 2 → 2 subjects  
- Student 3 → 4 subjects  

Represent using a jagged array and print.

---

## 2. Create a Triangle Pattern using Jagged Array
```
Row 1 → 1
Row 2 → 1 2
Row 3 → 1 2 3
Row 4 → 1 2 3 4
```

---

## 3. Sum of Each Row in Jagged Array

### Example Input
```
1 2 3
4 5
6 7 8 9
```

### Output
```
Row 1 sum = 6
Row 2 sum = 9
Row 3 sum = 30
```

---

## 4. Find Largest Element in Each Row

### Example Input
```
10 20 5
4 50
6 7 100 9
```

### Output
```
Row 1 max = 20
Row 2 max = 50
Row 3 max = 100
```

---

## 5. Print Jagged Array in Reverse Row Order

### Example Input
```
1 2 3
4 5
6 7 8 9
```

### Output
```
6 7 8 9
4 5
1 2 3
```


## 1. Store Marks of Students (Unequal Subjects per Student)

```java
public class StudentMarks {
    public static void main(String[] args) {
        int[][] marks = new int[3][];
        marks[0] = new int[]{85, 90, 78};     // Student 1 → 3 subjects
        marks[1] = new int[]{88, 76};         // Student 2 → 2 subjects
        marks[2] = new int[]{92, 81, 74, 69}; // Student 3 → 4 subjects

        for (int i = 0; i < marks.length; i++) {
            System.out.print("Student " + (i + 1) + ": ");
            for (int j = 0; j < marks[i].length; j++) {
                System.out.print(marks[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

### ✅ Output
```
Student 1: 85 90 78
Student 2: 88 76
Student 3: 92 81 74 69
```

---

## 2. Create a Triangle Pattern using Jagged Array

```java
public class TrianglePattern {
    public static void main(String[] args) {
        int[][] triangle = new int[4][];

        for (int i = 0; i < 4; i++) {
            triangle[i] = new int[i + 1];
            for (int j = 0; j <= i; j++) {
                triangle[i][j] = j + 1;
            }
        }

        for (int i = 0; i < triangle.length; i++) {
            for (int j = 0; j < triangle[i].length; j++) {
                System.out.print(triangle[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

### ✅ Output
```
1
1 2
1 2 3
1 2 3 4
```

---

## 3. Sum of Each Row in Jagged Array

```java
public class RowSum {
    public static void main(String[] args) {
        int[][] arr = {
            {1, 2, 3},
            {4, 5},
            {6, 7, 8, 9}
        };

        for (int i = 0; i < arr.length; i++) {
            int sum = 0;
            for (int j = 0; j < arr[i].length; j++) {
                sum += arr[i][j];
            }
            System.out.println("Row " + (i + 1) + " sum = " + sum);
        }
    }
}
```

### ✅ Output
```
Row 1 sum = 6
Row 2 sum = 9
Row 3 sum = 30
```

---

## 4. Find Largest Element in Each Row

```java
public class RowMax {
    public static void main(String[] args) {
        int[][] arr = {
            {10, 20, 5},
            {4, 50},
            {6, 7, 100, 9}
        };

        for (int i = 0; i < arr.length; i++) {
            int max = arr[i][0];
            for (int j = 1; j < arr[i].length; j++) {
                if (arr[i][j] > max) {
                    max = arr[i][j];
                }
            }
            System.out.println("Row " + (i + 1) + " max = " + max);
        }
    }
}
```

### ✅ Output
```
Row 1 max = 20
Row 2 max = 50
Row 3 max = 100
```

---

## 5. Print Jagged Array in Reverse Row Order

```java
public class ReverseRows {
    public static void main(String[] args) {
        int[][] arr = {
            {1, 2, 3},
            {4, 5},
            {6, 7, 8, 9}
        };

        for (int i = arr.length - 1; i >= 0; i--) {
            for (int j = 0; j < arr[i].length; j++) {
                System.out.print(arr[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

### ✅ Output
```
6 7 8 9
4 5
1 2 3
```

---
