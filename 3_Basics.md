
## 📝 Comments in Java

**Comments** are **non-executable lines** in Java code meant for **documentation, explanation, or disabling code** during testing. The compiler **ignores** them.

---

### 1. **Single-Line Comment (`//`)**

* Starts with `//`
* Used for short explanations or quick notes

✅ **Example:**

```java
int age = 20; // This stores the user's age
```

---

### 2. **Multi-Line Comment (`/* ... */`)**

* Starts with `/*` and ends with `*/`
* Used for block comments, usually over multiple lines

✅ **Example:**

```java
/* This is a multi-line comment
   explaining the purpose of the following code block */
int sum = a + b;
```

---

## ✅ Best Practices for Using Comments

* Use comments to **explain why**, not what
  *(The code tells what it does, comments explain why it does that)*
* Keep them **short and meaningful**
* Avoid **over-commenting** obvious code
* Use Javadoc for **API-level documentation**

---


---

## 🔁 Output Operations in Java

Java provides powerful and flexible methods for handling **input** (reading data) and **output** (displaying data). I/O operations are done using:

* **Standard I/O (console-based)**
* **File I/O (file-based)** – optional for advanced learners

---

## ✅ **1. Output in Java** – `System.out`

### 🖨️ Using `System.out.println()` and `System.out.print()`

| Method      | Description                 |
| ----------- | --------------------------- |
| `println()` | Prints data with a newline  |
| `print()`   | Prints data without newline |

✅ **Example:**

```java
System.out.println("Welcome to Java!");  // With newline
System.out.print("Hello");               // Without newline
System.out.print(" World");              // Continues on same line
```


---
