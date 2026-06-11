# Polymorphism in Java

## Definition

**Polymorphism** is one of the four pillars of Object-Oriented Programming (OOP). The word *Polymorphism* means **"many forms"**. It allows the same method or object to behave differently based on the context.

In Java, polymorphism enables a single interface to represent different underlying forms (data types).

---

## Why Use Polymorphism?

- Improves code flexibility.
- Enhances code reusability.
- Supports method overriding and overloading.
- Reduces complexity in large applications.

---

## Types of Polymorphism in Java

### 1. Compile-Time Polymorphism (Method Overloading)

Achieved when multiple methods have the same name but different parameter lists.

### Example

```java
class Calculator { 

    int add(int a, int b) {  // here function name is add but parameter is a  and b
        return a + b;
    }

    int add(int a, int b, int c) { // here is also function is add but parameter is a , b and c
        return a + b + c;
    }
}
// so basically one function have different parameter name
public class Main {
    public static void main(String[] args) {
        Calculator obj = new Calculator();

        System.out.println(obj.add(10, 20));
        System.out.println(obj.add(10, 20, 30));
    }
}
```

### Output

```
30
60
```

---

## Method Overloading Rules

- Method name must be the same.
- Parameter list must be different.
- Return type may or may not be different.
- Achieved at compile time.

---

### 2. Runtime Polymorphism (Method Overriding)

Achieved when a child class provides a specific implementation of a method already defined in the parent class.

### Example - So basically here Parent and Child both contain the same function but with different definition

```java
class Animal {

    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {

        Animal obj = new Dog();
        obj.sound();
    }
}
```

### Output

```
Dog barks
```

---

## Dynamic Method Dispatch

Runtime polymorphism is achieved through **Dynamic Method Dispatch**, where the method to be executed is determined at runtime.

### Example

```java
class Animal {
    void sound() {
        System.out.println("Animal Sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog Bark");
    }
}

class Cat extends Animal {
    void sound() {
        System.out.println("Cat Meow");
    }
}

public class Main {
    public static void main(String[] args) {

        Animal a;

        a = new Dog();
        a.sound();

        a = new Cat();
        a.sound();
    }
}
```

### Output

```
Dog Bark
Cat Meow
```

---

## Real-World Example

```java
class Payment {

    void pay() {
        System.out.println("Processing Payment");
    }
}

class CreditCard extends Payment {

    @Override
    void pay() {
        System.out.println("Payment via Credit Card");
    }
}

class UPI extends Payment {

    @Override
    void pay() {
        System.out.println("Payment via UPI");
    }
}

public class Main {
    public static void main(String[] args) {

        Payment p;

        p = new CreditCard();
        p.pay();

        p = new UPI();
        p.pay();
    }
}
```

### Output

```
Payment via Credit Card
Payment via UPI
```

---

## Advantages of Polymorphism

- Improves code readability.
- Enhances maintainability.
- Increases flexibility.
- Supports dynamic behavior.
- Promotes code reusability.

---

## Disadvantages of Polymorphism

- Slight runtime overhead in dynamic binding.
- Can make debugging more complex.
- Overuse may reduce code clarity.

---

## Compile-Time vs Runtime Polymorphism

| Feature | Compile-Time | Runtime |
|----------|-------------|----------|
| Achieved By | Method Overloading | Method Overriding |
| Binding | Early Binding | Late Binding |
| Performance | Faster | Slightly Slower |
| Decision Time | Compile Time | Runtime |

---

## Time Complexity

| Operation | Time Complexity |
|-----------|----------------|
| Method Call | O(1) |
| Overloaded Method Resolution | O(1) |
| Overridden Method Call | O(1) |

---

## Space Complexity

| Operation | Space Complexity |
|-----------|-----------------|
| Method Invocation | O(1) |

---

## Key Points

- Polymorphism means **one interface, multiple implementations**.
- Java supports:
  - Compile-Time Polymorphism (Method Overloading)
  - Runtime Polymorphism (Method Overriding)
- Runtime polymorphism is achieved through inheritance.
- Dynamic Method Dispatch decides which overridden method to call at runtime.
- Polymorphism makes applications scalable and maintainable.

---

## Summary

Polymorphism is an OOP concept that allows the same method or object reference to perform different tasks based on the actual object. Java implements polymorphism through **method overloading** (compile-time) and **method overriding** (runtime), making programs more flexible, reusable, and easier to maintain.
