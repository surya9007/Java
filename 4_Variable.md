
## 🔧 **Variables in Java**

A **variable** in Java is a **named container** used to **store data** that can be changed during the execution of a program.

---

### 🧠 **Key Features of Java Variables**

* Java is a **statically typed** language – every variable must be **declared with a type** before use.
* Variables store **primitive values** (like `int`, `float`) or **references to objects** (like `String`, `Scanner`).

---

## 🔠 **Types of Variables in Java**

### 1. 🧱 **Local Variables**

* Declared inside methods, constructors, or blocks
* Only accessible within that block
* Not automatically initialized

```java
void greet() {
    String message = "Hello!";
    System.out.println(message);  // Local variable
}
```

---

### 2. 🏠 **Instance Variables (Non-static fields)**

* Declared inside a class but **outside methods**
* Each object gets its own copy
* Initialized to default values if not manually set

```java
class Car {
    int speed;           // Instance variable
    String model;
}
```

---

### 3. 🏢 **Static Variables (Class-level variables)**

* Declared with the `static` keyword
* Shared across **all objects** of the class

```java
class Student {
    static String college = "ABC College";  // Static variable
}
```

---

## 🧪 **Variable Declaration and Initialization**

```java
datatype variableName = value;
```

✅ **Examples:**

```java
int age = 25;
float price = 99.99f;
char grade = 'A';
boolean isJavaFun = true;
String name = "Raja";
```

---

## 🛑 **Java Naming Rules**

* Must begin with a **letter**, `_`, or `$`
* **No spaces or special symbols** (except `_` and `$`)
* Cannot be a **Java keyword** (like `int`, `class`, etc.)
* **Camel case** is preferred: `userName`, `totalMarks`

---

## 🔒 Constant Variables

If a variable should **never change**, use the `final` keyword:

```java
final double PI = 3.14159;
```

---
