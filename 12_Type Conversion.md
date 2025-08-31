# Type Conversion in Java

## 📘 Definition
**Type Conversion** in Java refers to changing a variable of one data type into another.  
It is mainly divided into the following types:

## 📚 Types of Type Conversion in Java
1. **Implicit Type Conversion (Widening)**  
2. **Explicit Type Conversion (Narrowing)**  
3. **Boxing and Unboxing**  
4. **Type Conversion Between Primitives and Strings**  
5. **Type Conversion Between Object Types (Inheritance & Casting)**  

---

## 🔹 1. Implicit Type Conversion (Widening)

Occurs when a **smaller data type is automatically converted** into a larger data type.  
- Done **automatically** by the compiler  
- **Safe** (no data loss)

### ✅ Rules:
- `byte → short → int → long → float → double`  
- `char → int`

### 💡 Example:
```java
public class ImplicitConversion {
    public static void main(String[] args) {
        int num = 100;
        long bigNum = num;        // int → long
        float floatNum = bigNum;  // long → float

        System.out.println("Int: " + num);
        System.out.println("Long: " + bigNum);
        System.out.println("Float: " + floatNum);
    }
}
```

---

## 🔹 2. Explicit Type Conversion (Narrowing / Type Casting)

Occurs when a **larger data type is manually converted** into a smaller data type.  
- Done **manually** using **type casting** `(type)`  
- **May cause data loss** or overflow  

### 💡 Example:
```java
public class ExplicitConversion {
    public static void main(String[] args) {
        double doubleNum = 99.99;
        int intNum = (int) doubleNum;  // double → int

        int bigValue = 300;
        byte smallValue = (byte) bigValue; // int → byte (overflow may occur)

        System.out.println("Double: " + doubleNum);
        System.out.println("Int (after casting): " + intNum);
        System.out.println("Int 300 to Byte (after casting): " + smallValue);
    }
}
```

---

## 🔹 3. Boxing and Unboxing

### ✅ Boxing
Converting a **primitive type** into its corresponding **wrapper class object**.  
Example: `int → Integer`, `double → Double`

### ✅ Unboxing
Converting a **wrapper class object** back to its **primitive type**.

### 💡 Example:
```java
public class BoxingUnboxing {
    public static void main(String[] args) {
        // Boxing (primitive → object)
        int num = 10;
        Integer boxed = num;

        // Unboxing (object → primitive)
        int unboxed = boxed;

        System.out.println("Boxed: " + boxed);
        System.out.println("Unboxed: " + unboxed);
    }
}
```

---

## 🔹 4. Type Conversion Between Primitives and Strings

### ✅ Primitive → String
- Using `String.valueOf()`  
- Using `Integer.toString()`, `Double.toString()`, etc.  

### ✅ String → Primitive
- Using `Integer.parseInt()`, `Double.parseDouble()`, etc.  

### 💡 Example:
```java
public class PrimitiveStringConversion {
    public static void main(String[] args) {
        int num = 50;

        // Primitive → String
        String str1 = String.valueOf(num);
        String str2 = Integer.toString(num);

        // String → Primitive
        String s = "100";
        int parsedInt = Integer.parseInt(s);

        System.out.println("String from int: " + str1);
        System.out.println("Parsed int from String: " + parsedInt);
    }
}
```

---

## 🔹 5. Type Conversion Between Object Types (Inheritance & Casting)

Java allows **upcasting** (automatic) and **downcasting** (manual) between objects in an **inheritance hierarchy**.

### ✅ Upcasting (Implicit)
- Subclass → Superclass  
- Done automatically  
- Safe  

### ✅ Downcasting (Explicit)
- Superclass → Subclass  
- Must be done manually  
- May throw `ClassCastException`  

### 💡 Example:
```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }

    void special() {
        System.out.println("Dog has special behavior");
    }
}

public class ObjectTypeCasting {
    public static void main(String[] args) {
        // Upcasting (Dog → Animal)
        Animal a = new Dog();
        a.sound();

        // Downcasting (Animal → Dog)
        Dog d = (Dog) a;
        d.special();
    }
}
```

---

## 🔄 Comparison Table

| Feature / Type                  | Automatic? | Manual? | Risk of Data Loss? | Example                    |
|---------------------------------|------------|---------|--------------------|----------------------------|
| **Implicit (Widening)**         | ✅ Yes      | ❌ No   | ❌ No              | `int → long`               |
| **Explicit (Narrowing)**        | ❌ No       | ✅ Yes  | ✅ Yes             | `double → int`             |
| **Boxing / Unboxing**           | ✅ Auto     | ❌ No   | ❌ No              | `int ↔ Integer`            |
| **Primitives ↔ Strings**        | ❌ No       | ✅ Yes  | ❌ No              | `int ↔ String`             |
| **Object Casting**              | ✅ (Upcast) | ✅ (Downcast) | ⚠️ Exception risk | `Dog ↔ Animal`             |

---

## 📌 Quick Summary
- **Widening (Implicit)**: Safe, automatic, no data loss.  
- **Narrowing (Explicit)**: Manual, may cause **data loss** or **overflow**.  
- **Boxing/Unboxing**: Conversion between primitives and wrapper classes.  
- **Primitives ↔ Strings**: Using `valueOf()`, `toString()`, `parseInt()`, etc.  
- **Object Casting**: Upcasting (safe), Downcasting (manual, may cause exceptions).  
