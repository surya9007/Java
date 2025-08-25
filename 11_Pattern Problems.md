# ⭐ Java Pattern Printing Problems (Basic to Advanced) with Solutions

This file contains **20 pattern problems** in Java — starting from **basic** to **advanced**, 
with code solutions and tricks explained.

---

## 1. Solid Square Pattern 
**Problem:** Print a solid N x N square.

**Input:** `N = 4`  
**Output:**
```
****
****
****
****
```

**Java Solution:**
```java
for(int i=0; i<4; i++) {
    for(int j=0; j<4; j++) {
        System.out.print("*");
    }
    System.out.println();
}
```
**Trick:** Two nested loops → rows & columns.

---

## 2. Right Triangle Pattern
```
*
**
***
****
```
```java
for(int i=1; i<=4; i++) {
    for(int j=1; j<=i; j++) {
        System.out.print("*");
    }
    System.out.println();
}
```
**Trick:** Outer loop = rows, inner loop = stars equal to row number.

---

## 3. Inverted Right Triangle
```
****
***
**
*
```
```java
for(int i=4; i>=1; i--) {
    for(int j=1; j<=i; j++) {
        System.out.print("*");
    }
    System.out.println();
}
```
**Trick:** Just reverse loop direction.

---

## 4. Number Triangle
```
1
12
123
1234
```
```java
for(int i=1; i<=4; i++) {
    for(int j=1; j<=i; j++) {
        System.out.print(j);
    }
    System.out.println();
}
```
**Trick:** Print column index instead of `*`.

---

## 5. Floyd’s Triangle
```
1
2 3
4 5 6
7 8 9 10
```
```java
int num=1;
for(int i=1; i<=4; i++) {
    for(int j=1; j<=i; j++) {
        System.out.print(num++ + " ");
    }
    System.out.println();
}
```
**Trick:** Use a counter that increments each time.

---

## 6. Inverted Number Triangle
```
1234
123
12
1
```
```java
for(int i=4; i>=1; i--) {
    for(int j=1; j<=i; j++) {
        System.out.print(j);
    }
    System.out.println();
}
```
**Trick:** Just reverse outer loop.

---

## 7. 0-1 Triangle
```
1
01
101
0101
```
```java
for(int i=1; i<=4; i++) {
    for(int j=1; j<=i; j++) {
        if((i+j)%2==0) System.out.print("1");
        else System.out.print("0");
    }
    System.out.println();
}
```
**Trick:** Use `(i+j)%2` to decide 1 or 0.

---

## 8. Pyramid Pattern
```
   *   
  ***  
 ***** 
*******
```
```java
int n=4;
for(int i=1; i<=n; i++) {
    for(int j=1; j<=n-i; j++) System.out.print(" ");
    for(int j=1; j<=2*i-1; j++) System.out.print("*");
    System.out.println();
}
```
**Trick:** Spaces before stars = `n-i`, stars = `2*i-1`.

---

## 9. Inverted Pyramid
```
*******
 ***** 
  ***  
   *   
```
```java
int n=4;
for(int i=n; i>=1; i--) {
    for(int j=1; j<=n-i; j++) System.out.print(" ");
    for(int j=1; j<=2*i-1; j++) System.out.print("*");
    System.out.println();
}
```
**Trick:** Reverse outer loop.

---

## 10. Diamond Pattern
```
   *   
  ***  
 ***** 
******* 
 ***** 
  ***  
   *   
```
```java
int n=4;
for(int i=1; i<=n; i++) {
    for(int j=1; j<=n-i; j++) System.out.print(" ");
    for(int j=1; j<=2*i-1; j++) System.out.print("*");
    System.out.println();
}
for(int i=n-1; i>=1; i--) {
    for(int j=1; j<=n-i; j++) System.out.print(" ");
    for(int j=1; j<=2*i-1; j++) System.out.print("*");
    System.out.println();
}
```
**Trick:** Upper pyramid + lower inverted pyramid.

---

## 11. Hollow Square
```
*****
*   *
*   *
*****
```
```java
int n=5;
for(int i=1; i<=n; i++) {
    for(int j=1; j<=n; j++) {
        if(i==1 || i==n || j==1 || j==n) System.out.print("*");
        else System.out.print(" ");
    }
    System.out.println();
}
```
**Trick:** Border = stars, inside = spaces.

---

## 12. Hollow Diamond
```
   *   
  * *  
 *   * 
*     *
 *   * 
  * *  
   *   
```
```java
int n=4;
for(int i=1; i<=n; i++) {
    for(int j=1; j<=n-i; j++) System.out.print(" ");
    for(int j=1; j<=2*i-1; j++) {
        if(j==1 || j==2*i-1) System.out.print("*");
        else System.out.print(" ");
    }
    System.out.println();
}
for(int i=n-1; i>=1; i--) {
    for(int j=1; j<=n-i; j++) System.out.print(" ");
    for(int j=1; j<=2*i-1; j++) {
        if(j==1 || j==2*i-1) System.out.print("*");
        else System.out.print(" ");
    }
    System.out.println();
}
```
**Trick:** Print star only at first & last column.

---

## 13. Hourglass Pattern
```
******* 
 ***** 
  ***  
   *   
  ***  
 ***** 
******* 
```
```java
int n=4;
for(int i=n; i>=1; i--) {
    for(int j=1; j<=n-i; j++) System.out.print(" ");
    for(int j=1; j<=2*i-1; j++) System.out.print("*");
    System.out.println();
}
for(int i=2; i<=n; i++) {
    for(int j=1; j<=n-i; j++) System.out.print(" ");
    for(int j=1; j<=2*i-1; j++) System.out.print("*");
    System.out.println();
}
```
**Trick:** Inverted + normal pyramid.

---

## 14. Pascal’s Triangle
```
      1
     1 1
    1 2 1
   1 3 3 1
  1 4 6 4 1
```
```java
int n=5;
for(int i=0; i<n; i++) {
    int num=1;
    for(int j=0; j<n-i; j++) System.out.print(" ");
    for(int j=0; j<=i; j++) {
        System.out.print(num + " ");
        num = num*(i-j)/(j+1);
    }
    System.out.println();
}
```
**Trick:** Use binomial coefficient formula.

---

## 15. Butterfly Pattern
```
*      *
**    **
***  ***
********
***  ***
**    **
*      *
```
```java
int n=4;
for(int i=1; i<=n; i++) {
    for(int j=1; j<=i; j++) System.out.print("*");
    for(int j=1; j<=2*(n-i); j++) System.out.print(" ");
    for(int j=1; j<=i; j++) System.out.print("*");
    System.out.println();
}
for(int i=n; i>=1; i--) {
    for(int j=1; j<=i; j++) System.out.print("*");
    for(int j=1; j<=2*(n-i); j++) System.out.print(" ");
    for(int j=1; j<=i; j++) System.out.print("*");
    System.out.println();
}
```
**Trick:** Symmetry + spaces in middle.

---

## 16. Hollow Pyramid
```
   *   
  * *  
 *   * 
*******
```
```java
int n=4;
for(int i=1; i<=n; i++) {
    for(int j=1; j<=n-i; j++) System.out.print(" ");
    for(int j=1; j<=2*i-1; j++) {
        if(j==1 || j==2*i-1 || i==n) System.out.print("*");
        else System.out.print(" ");
    }
    System.out.println();
}
```
**Trick:** Star at edges & bottom row.

---

## 17. Zig-Zag Pattern
```
   *       *   
 *   *   *   * 
*       *       *
```
```java
int n=9;
for(int i=1; i<=3; i++) {
    for(int j=1; j<=n; j++) {
        if((i+j)%4==0 || (i==2 && j%4==0)) System.out.print("*");
        else System.out.print(" ");
    }
    System.out.println();
}
```
**Trick:** Use modulo math `(i+j)%4==0`.

---

## 18. Hollow Right Triangle
```
*
**
* *
*  *
*****
```
```java
int n=5;
for(int i=1; i<=n; i++) {
    for(int j=1; j<=i; j++) {
        if(j==1 || j==i || i==n) System.out.print("*");
        else System.out.print(" ");
    }
    System.out.println();
}
```
**Trick:** Print star at edges only.

---

## 19. Cross (X) Pattern
```
*   *
 * * 
  *  
 * * 
*   *
```
```java
int n=5;
for(int i=1; i<=n; i++) {
    for(int j=1; j<=n; j++) {
        if(j==i || j==n-i+1) System.out.print("*");
        else System.out.print(" ");
    }
    System.out.println();
}
```
**Trick:** Star at diagonal positions.

---

## 20. Palindromic Number Pyramid
```
   1
  121
 12321
1234321
```
```java
int n=4;
for(int i=1; i<=n; i++) {
    for(int j=1; j<=n-i; j++) System.out.print(" ");
    for(int j=i; j>=1; j--) System.out.print(j);
    for(int j=2; j<=i; j++) System.out.print(j);
    System.out.println();
}
```
**Trick:** First half descending, second half ascending numbers.

---

# 🔤 Character Patterns

---

## 21. Right Triangle Alphabet Pattern
```
A
A B
A B C
A B C D
A B C D E
```

**Trick:** Print `(char)('A' + j)`.

```java
public class CharTriangle {
    public static void main(String[] args) {
        int n = 5;
        for(int i=0; i<n; i++) {
            for(int j=0; j<=i; j++) {
                System.out.print((char)('A' + j) + " ");
            }
            System.out.println();
        }
    }
}
```

---

## 22. Inverted Character Triangle
```
A B C D E
A B C D
A B C
A B
A
```

**Trick:** Inner loop decreases.

```java
public class InvertedCharTriangle {
    public static void main(String[] args) {
        int n = 5;
        for(int i=n; i>=1; i--) {
            for(int j=0; j<i; j++) {
                System.out.print((char)('A' + j) + " ");
            }
            System.out.println();
        }
    }
}
```

---

## 23. Character Pyramid
```
    A
   A B
  A B C
 A B C D
A B C D E
```

**Trick:** Spaces + alphabets.

```java
public class CharPyramid {
    public static void main(String[] args) {
        int n = 5;
        for(int i=0; i<n; i++) {
            for(int j=i; j<n; j++) System.out.print(" ");
            for(int j=0; j<=i; j++) System.out.print((char)('A' + j) + " ");
            System.out.println();
        }
    }
}
```

---

## 24. Character Diamond
```
    A
   A B
  A B C
   A B
    A
```

**Trick:** Pyramid + Inverted.

```java
public class CharDiamond {
    public static void main(String[] args) {
        int n = 3;
        for(int i=0; i<n; i++) {
            for(int j=i; j<n; j++) System.out.print(" ");
            for(int j=0; j<=i; j++) System.out.print((char)('A' + j) + " ");
            System.out.println();
        }
        for(int i=n-2; i>=0; i--) {
            for(int j=i; j<n; j++) System.out.print(" ");
            for(int j=0; j<=i; j++) System.out.print((char)('A' + j) + " ");
            System.out.println();
        }
    }
}
```

---

## 25. Floyd’s Character Triangle
```
A
B C
D E F
G H I J
```

**Trick:** Use one variable `ch` and increment.

```java
public class FloydChar {
    public static void main(String[] args) {
        int n = 4;
        char ch = 'A';
        for(int i=1; i<=n; i++) {
            for(int j=1; j<=i; j++) {
                System.out.print(ch + " ");
                ch++;
            }
            System.out.println();
        }
    }
}
```

# Java Pattern Problem (Odd Number Based)

## Question 26: Special Pattern (Only if input is an odd number)

Write a program in Java to print the following pattern when the input is an **odd number**.
input :- n = 5.

```
 *                       * 
 *                       *  * 
 *  *  *  *  *  *  *  *  *  *  * 
 *                       *  *
 *                       *
```


## Java Solution:

```java

import java.util.Scanner;

public class Tgh{
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an odd number: ");
        int n = scanner.nextInt();
        scanner.close();

        // Upper half
        for (int j = 0; j < n / 2; ++j) {
            System.out.print(" * ");
            for (int k = 0; k < n + 2; ++k) {
                System.out.print("   ");
            }
            for (int m = 1; m <= j + 1; ++m) {
                System.out.print(" * ");
            }
            System.out.println();
        }

        // // Middle line
        for (int i = 0; i < 1 + n + 2; ++i) {
            System.out.print(" * ");
        }
        for (int i = 0; i < n / 2 + 1; ++i) {
            System.out.print(" * ");
        }
        System.out.println();

        // // Lower half
        for (int j = n / 2; j > 0; --j) {
            System.out.print(" * ");
            for (int k = 0; k < n + 2; ++k) {
                System.out.print("   ");
            }
            for (int m = 1; m < j + 1; ++m) {
                System.out.print(" * ");
            }
            System.out.println();
        }
    }
}
---



