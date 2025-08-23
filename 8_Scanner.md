In Java, **`Scanner`** is a class in the `java.util` package used to take **input** from various sources, most commonly from the **keyboard**.

**Key points:**

* You need to **import** it:

  ```java
  import java.util.Scanner;
  ```
* It can read different data types: `int`, `double`, `String`, `boolean`, etc.
* It reads input **token by token** (split by whitespace) unless you use special methods like `nextLine()`.

**Example:**

```java
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);  // Create Scanner object
        
        System.out.print("Enter your name: ");
        String name = sc.nextLine();  // Read a line of text
        
        System.out.print("Enter your age: ");
        int age = sc.nextInt();       // Read an integer
        
        System.out.println("Hello " + name + ", you are " + age + " years old.");
        
        sc.close();  // Close scanner to prevent resource leaks
    }
}
```

In Java, `Scanner` can read **all primitive data types** and also **Strings**.

| **Java Data Type** | **Scanner Method**                            | **Example**                        |
| ------------------ | --------------------------------------------- | ---------------------------------- |
| `byte`             | `nextByte()`                                  | `byte b = sc.nextByte();`          |
| `short`            | `nextShort()`                                 | `short s = sc.nextShort();`        |
| `int`              | `nextInt()`                                   | `int i = sc.nextInt();`            |
| `long`             | `nextLong()`                                  | `long l = sc.nextLong();`          |
| `float`            | `nextFloat()`                                 | `float f = sc.nextFloat();`        |
| `double`           | `nextDouble()`                                | `double d = sc.nextDouble();`      |
| `boolean`          | `nextBoolean()`                               | `boolean flag = sc.nextBoolean();` |
| `char`             | **No direct method** — use `next().charAt(0)` | `char c = sc.next().charAt(0);`    |
| `String`           | `next()` or `nextLine()`                      | `String s = sc.nextLine();`        |

---

**Example reading all types:**

```java
import java.util.Scanner;

class AllTypesExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter byte: ");
        byte b = sc.nextByte();

        System.out.print("Enter short: ");
        short s = sc.nextShort();

        System.out.print("Enter int: ");
        int i = sc.nextInt();

        System.out.print("Enter long: ");
        long l = sc.nextLong();

        System.out.print("Enter float: ");
        float f = sc.nextFloat();

        System.out.print("Enter double: ");
        double d = sc.nextDouble();

        System.out.print("Enter boolean (true/false): ");
        boolean bool = sc.nextBoolean();

        System.out.print("Enter a character: ");
        char c = sc.next().charAt(0);

        sc.nextLine(); // clear buffer before nextLine()

        System.out.print("Enter a string: ");
        String str = sc.nextLine();

        System.out.println("\n--- Output ---");
        System.out.println("byte: " + b);
        System.out.println("short: " + s);
        System.out.println("int: " + i);
        System.out.println("long: " + l);
        System.out.println("float: " + f);
        System.out.println("double: " + d);
        System.out.println("boolean: " + bool);
        System.out.println("char: " + c);
        System.out.println("string: " + str);

        sc.close();
    }
}
```

## What is the difference between `next()` and `nextLine()` in Java?

In Java, both `next()` and `nextLine()` are methods of the `Scanner` class used for reading input, but they behave differently:

---

### 🔹 `next()`

- **Reads:** A **single word** (token), stopping at whitespace.
- **Delimiters:** Uses space, tab, or newline as default delimiters.
- **Skips:** Leading whitespace (spaces, tabs, newlines).
- **Example Input:**
  ```
  Hello world
  ```
  - `scanner.next()` → `"Hello"`  
  - `scanner.next()` again → `"world"`

---

### 🔹 `nextLine()`

- **Reads:** The **entire line** of input, including spaces, until a newline `\n`.
- **Stops:** When it encounters the **end of the line**.
- **Returns:** Everything typed before Enter was pressed.
- **Example Input:**
  ```
  Hello world
  ```
  - `scanner.nextLine()` → `"Hello world"`

---

### ⚠ Common Issue

If you use `next()`, `nextInt()`, etc., **before** `nextLine()`, the newline character (`\n`) is **not consumed**, so the next `nextLine()` may appear to "skip" input.

#### Example:
```java
Scanner scanner = new Scanner(System.in);
int age = scanner.nextInt();      // suppose input: 25
String name = scanner.nextLine(); // seems skipped
```

**Why?**  
Because `nextInt()` only reads `25`, **not** the newline after it, so `nextLine()` reads the leftover newline.

#### ✅ Fix:
```java
scanner.nextLine();              // consume the leftover newline
String name = scanner.nextLine(); // now works as expected
```

---

### ✅ Summary

| Method       | Reads           | Stops at      | Useful for                   |
|--------------|------------------|---------------|------------------------------|
| `next()`     | Next word/token  | Whitespace    | Reading individual words     |
| `nextLine()` | Whole line       | Newline (`\n`) | Reading full lines of input |

