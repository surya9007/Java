
## 🧩 Data Types in Java

**Data types** in Java define the **type and size of data** a variable can hold. Java is a **statically typed language**, so **every variable must have a declared type** before use.

---

## 📚 Categories of Data Types

Java data types are divided into **two main categories**:

### 1. 🎯 **Primitive Data Types**

> Built-in types that store **single values**
> Total: **8 types**

| Data Type | Size    | Example Value         | Description                  |
| --------- | ------- | --------------------- | ---------------------------- |
| `byte`    | 1 byte  | `byte a = 100;`       | Small integer (-128 to 127)  |
| `short`   | 2 bytes | `short s = 10000;`    | Medium integer               |
| `int`     | 4 bytes | `int x = 12345;`      | Default integer type         |
| `long`    | 8 bytes | `long l = 9999999L;`  | Large integers               |
| `float`   | 4 bytes | `float f = 3.14f;`    | Decimal with lower precision |
| `double`  | 8 bytes | `double d = 2.71828;` | High-precision decimal       |
| `char`    | 2 bytes | `char c = 'A';`       | Single Unicode character     |
| `boolean` | 1 bit   | `boolean b = true;`   | Only `true` or `false`       |


---

### 2. 🧱 **Non-Primitive (Reference) Data Types**

> Store **references to objects**, not the actual value

| Type                | Example                      | Description                |
| ------------------- | ---------------------------- | -------------------------- |
| `String`            | `String name = "John";`      | Sequence of characters     |
| `Arrays`            | `int[] arr = {1,2,3};`       | Collection of similar data |
| `Class`             | `Student s = new Student();` | Custom object              |
| `Interface`, `Enum` | Advanced object types        | Used for OOP design        |

---



## ✅ Java Program: Example of All Data Types

```java
public class DataTypesExample {
    public static void main(String[] args) {
        
        // 🔹 Primitive Data Types
        
        // 1. byte (1 byte, -128 to 127)
        byte b = 100;
        System.out.println("byte: " + b);

        // 2. short (2 bytes, -32,768 to 32,767)
        short s = 20000;
        System.out.println("short: " + s);

        // 3. int (4 bytes, default for integers)
        int age = 25;
        System.out.println("int: " + age);

        // 4. long (8 bytes, add L at the end)
        long population = 7800000000L;
        System.out.println("long: " + population);

        // 5. float (4 bytes, add f at the end)
        float price = 99.99f;
        System.out.println("float: " + price);

        // 6. double (8 bytes, default for decimal values)
        double pi = 3.1415926535;
        System.out.println("double: " + pi);

        // 7. char (2 bytes, Unicode characters)
        char grade = 'A';
        System.out.println("char: " + grade);

        // 8. boolean (1 bit, only true or false)
        boolean isJavaFun = true;
        System.out.println("boolean: " + isJavaFun);

        // 🔹 Non-Primitive Data Types

        // 1. String (class)
        String name = "Raja";
        System.out.println("String: " + name);

        // 2. Array (non-primitive)
        int[] marks = {85, 90, 95};
        System.out.println("Array: " + marks[0] + ", " + marks[1] + ", " + marks[2]);

        // 3. Object of a class (reference type)
        DataTypesExample obj = new DataTypesExample();
        System.out.println("Object: " + obj);

    }
}
```

## 🧾 Output (sample)

```
byte: 100
short: 20000
int: 25
long: 7800000000
float: 99.99
double: 3.1415926535
char: A
boolean: true
String: Raja
Array: 85, 90, 95
Object: DataTypesExample@6bc7c054
```

> ⚠️ The last line is the object's memory reference (you can override `toString()` to customize it).

---


## 🛑 Default Values of Primitive Data Types

| Data Type | Default Value |
| --------- | ------------- |
| `int`     | `0`           |
| `float`   | `0.0f`        |
| `char`    | `\u0000`      |
| `boolean` | `false`       |
| `String`  | `null`        |

---

## 🔍 Type Conversion in Java

### 🔸 Implicit (Widening)

Automatically done by Java

```java
int a = 10;
double d = a;  // OK
```

### 🔸 Explicit (Narrowing)

Manual cast required

```java
double d = 9.78;
int a = (int) d;  // Possible data loss
```

---
