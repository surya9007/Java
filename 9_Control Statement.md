

## 🕹️ Control Statements in Java

**Control statements** determine the **flow of execution** in a Java program. They allow you to make **decisions**, **repeat code**, and **jump** between parts of the program.

Java provides **three main categories** of control statements:

---

## ✅ 1. **Conditional (Decision-Making) Statements**

### 🔸 a) `if` Statement

Executes code **only if** a condition is true.

```java
int age = 18;
if (age >= 18) {
    System.out.println("You are eligible to vote.");
}
```

---

### 🔸 b) `if-else` Statement

Executes one block if the condition is true, otherwise another.

```java
if (age >= 18) {
    System.out.println("Adult");
} else {
    System.out.println("Minor");
}
```

---

### 🔸 c) `if-else-if` Ladder

Multiple conditions checked one after another.

```java
int marks = 85;
if (marks >= 90) {
    System.out.println("Grade A");
} else if (marks >= 75) {
    System.out.println("Grade B");
} else {
    System.out.println("Grade C");
}
```

---

### 🔸 d) `switch` Statement

Simplifies checking against multiple values of the same variable.

```java
int day = 3;
switch (day) {
    case 1: System.out.println("Monday"); break;
    case 2: System.out.println("Tuesday"); break;
    case 3: System.out.println("Wednesday"); break;
    default: System.out.println("Invalid day");
}
```

---

## 🔁 2. **Looping (Iteration) Statements**

Used to **repeat** a block of code.

### 🔸 a) `for` Loop

```java
for (int i = 1; i <= 5; i++) {
    System.out.println("Count: " + i);
}
```

---

### 🔸 b) `while` Loop

```java
int i = 1;
while (i <= 5) {
    System.out.println("Count: " + i);
    i++;
}
```

---

### 🔸 c) `do-while` Loop

Executes at least once, even if the condition is false.

```java
int i = 1;
do {
    System.out.println("Count: " + i);
    i++;
} while (i <= 5);
```

---

## 🔁 3. **Jump (Branching) Statements**

Used to **control the flow** of execution explicitly.

### 🔸 a) `break`

* Exits from a loop or switch.

```java
for (int i = 1; i <= 10; i++) {
    if (i == 5) break;
    System.out.println(i);
}
```

---

### 🔸 b) `continue`

* Skips the current iteration and continues with the next.

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) continue;
    System.out.println(i);
}
```

---

### 🔸 c) `return`

* Exits from a method and optionally returns a value.

```java
public static int add(int a, int b) {
    return a + b;
}
```

---
