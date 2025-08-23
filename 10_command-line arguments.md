## 📘 Command-Line Arguments in Java

### 🧾 Definition

**Command-line arguments** in Java are values passed to the `main()` method when running a program from the command line.  
They are received as an array of `String` values:

```java
public static void main(String[] args)
```

Each argument is a string entered after the class name during execution.

---

### 🧪 Basic Example

```java
public class CommandLineExample {
    public static void main(String[] args) {
        System.out.println("Number of arguments: " + args.length);

        for (int i = 0; i < args.length; i++) {
            System.out.println("Argument " + i + ": " + args[i]);
        }
    }
}
```

---

### ▶️ How to Run

**Compile:**
```bash
javac CommandLineExample.java
```

**Run with arguments:**
```bash
java CommandLineExample Hello 123 World
```

---

### 🧾 Output:
```
Number of arguments: 3
Argument 0: Hello
Argument 1: 123
Argument 2: World
```

---

## 🔢 Parsing Command-Line Arguments

Since all arguments come as **strings**, you must **convert them** to other data types if needed:

### ✅ Example 1: Convert String to Integer

```java
public class SumTwoNumbers {
    public static void main(String[] args) {
        int num1 = Integer.parseInt(args[0]);
        int num2 = Integer.parseInt(args[1]);

        int sum = num1 + num2;

        System.out.println("Sum = " + sum);
    }
}
```

**Run:**
```bash
java SumTwoNumbers 10 20
```

**Output:**
```
Sum = 30
```

---

### ✅ Example 2: Convert String to Double

```java
public class AreaOfCircle {
    public static void main(String[] args) {
        double radius = Double.parseDouble(args[0]);
        double area = Math.PI * radius * radius;

        System.out.println("Area = " + area);
    }
}
```

**Run:**
```bash
java AreaOfCircle 7.5
```

**Output:**
```
Area = 176.71458676442586
```

---

### ✅ Example 3: Using String Arguments

```java
public class Greeting {
    public static void main(String[] args) {
        String name = args[0];
        System.out.println("Hello, " + name + "!");
    }
}
```

**Run:**
```bash
java Greeting Alice
```

**Output:**
```
Hello, Alice!
```

---

### ⚠️ Notes:
- All command-line arguments are strings by default.
- Use parsing methods like:
  - `Integer.parseInt()`
  - `Double.parseDouble()`
  - `Boolean.parseBoolean()`
- Make sure to check `args.length` to avoid `ArrayIndexOutOfBoundsException`.

---

### 📌 Common Use Cases:
- Reading numbers or text without user prompts
- Batch processing with file names or data
- Configuring behavior of programs via input
