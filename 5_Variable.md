## 🌟 **Java Variables**

### ✅ **1. What is a Variable?**

A **variable** is a name given to a memory location that stores data.
It allows programs to store and manipulate values.

---

### ✅ **2. Rules for Naming Variables**

* Must begin with a letter (A-Z or a-z), `$`, or `_`
* Cannot start with a number
* Cannot use Java reserved keywords (`int`, `class`, `public`, etc.)
* Should follow **camelCase** (e.g., `studentName`, `totalMarks`)

---

### ✅ **3. Types of Variables**

Java has three main types of variables:

| Type         | Description                                           |
| ------------ | ----------------------------------------------------- |
| **Local**    | Declared inside methods/blocks/constructors           |
| **Instance** | Declared inside class, outside methods                |
| **Static**   | Declared with `static` keyword, shared by all objects |

---

### ✅ **4. Data Types in Java**

#### 🔹 Primitive Types (8 types)

| Type      | Size    | Example                  |
| --------- | ------- | ------------------------ |
| `int`     | 4 bytes | `int age = 25;`          |
| `float`   | 4 bytes | `float pi = 3.14f;`      |
| `double`  | 8 bytes | `double d = 22.56;`      |
| `char`    | 2 bytes | `char grade = 'A';`      |
| `boolean` | 1 bit   | `boolean isPass = true;` |
| `byte`    | 1 byte  | `byte b = 100;`          |
| `short`   | 2 bytes | `short s = 32000;`       |
| `long`    | 8 bytes | `long l = 123456789L;`   |

#### 🔹 Non-Primitive Types

* String, Array, Class, Interface, etc.

---

### ✅ **5. Declaring and Initializing Variables**

```java
int number = 10;
float pi = 3.14f;
char grade = 'A';
boolean isJavaFun = true;
String name = "Surya";
```

---

### ✅ **6. Multiple Declarations**

```java
int a = 10, b = 20, c = 30;
```

---

### ✅ **7. Constants**

Use `final` keyword to declare constants.

```java
final int MAX = 100;
```

---

### ✅ **8. Variable Scope Example**

```java
public class Example {
  int a = 5; // Instance variable

  public void method() {
    int b = 10; // Local variable
    System.out.println(a + b);
  }

  public static void main(String[] args) {
    Example obj = new Example();
    obj.method();
  }
}
```

---

### ✅ **9. Practice Programs**

#### 🔸 Program 1: Add Two Numbers

```java
public class AddNumbers {
  public static void main(String[] args) {
    int a = 5;
    int b = 10;
    int sum = a + b;
    System.out.println("Sum = " + sum);
  }
}
```

#### 🔸 Program 2: Display Student Info

```java
public class Student {
  public static void main(String[] args) {
    String name = "Surya";
    int age = 20;
    char grade = 'A';
    System.out.println("Name: " + name);
    System.out.println("Age: " + age);
    System.out.println("Grade: " + grade);
  }
}
```

---
