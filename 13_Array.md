# 📚 Arrays in Java

---

## 1. Array Declaration

An **array** in Java is a data structure that can hold multiple values of the same type in a single variable.

### Syntax:
```java
datatype[] arrayName;
```

or

```java
datatype arrayName[];
```

### Example:
```java
int[] numbers;        // preferred
String names[];
```

---

## 2. Array Initialization

Arrays can be initialized in two ways:

### a) Static Initialization
Values are directly assigned at the time of declaration.
```java
int[] numbers = {1, 2, 3, 4, 5};
```

### b) Dynamic Initialization
Values are assigned later using the `new` keyword.
```java
int[] numbers = new int[5];
numbers[0] = 10;
numbers[1] = 20;
```

---

## 3. `java.util.Arrays` Class

The `Arrays` class provides utility methods to manipulate arrays.

### Common Methods:
- **`Arrays.toString(array)`** → Converts array to a string.
- **`Arrays.sort(array)`** → Sorts the array in ascending order.
- **`Arrays.fill(array, value)`** → Fills the array with the given value.
- **`Arrays.copyOf(array, newLength)`** → Copies the array into a new array.
- **`Arrays.equals(arr1, arr2)`** → Compares two arrays.

### Example:
```java
import java.util.Arrays;

public class ArraysExample {
    public static void main(String[] args) {
        int[] arr = {5, 3, 1, 4, 2};

        System.out.println("Original: " + Arrays.toString(arr));
        Arrays.sort(arr);
        System.out.println("Sorted: " + Arrays.toString(arr));

        int[] copy = Arrays.copyOf(arr, 7);
        System.out.println("Copy: " + Arrays.toString(copy));

        Arrays.fill(copy, 6);
        System.out.println("Filled: " + Arrays.toString(copy));
    }
}
```

---

## 4. One-dimensional Arrays

A **one-dimensional array** stores a list of elements in a single row.

### Example:
```java
public class OneDArray {
    public static void main(String[] args) {
        int[] marks = {85, 90, 78, 92, 88};

        for (int i = 0; i < marks.length; i++) {
            System.out.println("Element at index " + i + ": " + marks[i]);
        }
    }
}
```

---

## 5. Array Operations & Methods (Coding)

### a) Traversing an Array
```java
for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
```

### b) Finding Maximum Element
```java
int max = arr[0];
for (int i = 1; i < arr.length; i++) {
    if (arr[i] > max) {
        max = arr[i];
    }
}
System.out.println("Maximum = " + max);
```

### c) Searching an Element (Linear Search)
```java
int key = 30;
boolean found = false;
for (int num : arr) {
    if (num == key) {
        found = true;
        break;
    }
}
System.out.println("Found? " + found);
```

---

## 6. Practice: Array Manipulation Exercises

### Exercise 1: Reverse an Array
```java
public class ReverseArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        
        for (int i = arr.length - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
    }
}
```

### Exercise 2: Sum of Array Elements
```java
int sum = 0;
for (int num : arr) {
    sum += num;
}
System.out.println("Sum = " + sum);
```

### Exercise 3: Check if Array is Sorted
```java
boolean sorted = true;
for (int i = 0; i < arr.length - 1; i++) {
    if (arr[i] > arr[i+1]) {
        sorted = false;
        break;
    }
}
System.out.println("Sorted? " + sorted);
```

---

## 1. What is the difference between `array.length` and `string.length()`?

- **`array.length`**
  - A **property** (not a method).
  - Returns the **size of the array** (number of elements it can hold).
  - Example:
    ```java
    int[] arr = {1, 2, 3};
    System.out.println(arr.length);  // Output: 3
    ```

- **`string.length()`**
  - A **method** of the `String` class.
  - Returns the **number of characters** in the string.
  - Example:
    ```java
    String str = "Hello";
    System.out.println(str.length());  // Output: 5
    ```

✅ **Key Difference:**  
`array.length` is a **field/property** (no parentheses).  
`string.length()` is a **method** (with parentheses).

---

## 2. Explain array bounds and `ArrayIndexOutOfBoundsException`

- **Array Bounds:**
  - In Java, arrays are **zero-indexed**, meaning the first element is at index `0` and the last element is at index `array.length - 1`.
  - Accessing any index outside this range is invalid.

- **`ArrayIndexOutOfBoundsException`:**
  - A **runtime exception** thrown when you try to access an invalid index in an array.
  - Example:
    ```java
    public class Example {
        public static void main(String[] args) {
            int[] arr = {10, 20, 30};
            System.out.println(arr[3]); // ❌ Error: index 3 is out of bounds
        }
    }
    ```
  - Valid indices for this array are `0`, `1`, and `2`. Accessing `arr[3]` causes the exception.

---

✅ This covers **Array declaration, initialization, `java.util.Arrays`, one-dimensional arrays, operations, and practice exercises**.
