# Object-Oriented Programming System (OOPS)

## Introduction

Object-Oriented Programming System (OOPS) is a programming paradigm that organizes software design around objects rather than functions and logic.

An object represents a real-world entity and contains:

* **State** → Data (Attributes)
* **Behavior** → Methods (Functions)

OOPS helps in writing modular, reusable, scalable, and maintainable code.

---

# Why OOPS?

* Code Reusability
* Better Maintainability
* Improved Security
* Easy Troubleshooting
* Faster Development
* Real-world Modeling

---

# Class

A class is a blueprint or template for creating objects.

## Syntax (Java)

```java
class Student {
    String name;
    int age;
}
```

### Example

```java
class Student {
    String name;
    int age;
}
```

---

# Object

An object is an instance of a class.

## Example

```java
Student s1 = new Student();

s1.name = "Shubham";
s1.age = 20;
```

---

# Four Pillars of OOPS

1. Encapsulation
2. Abstraction
3. Inheritance
4. Polymorphism

---

# 1. Encapsulation

Encapsulation is the process of wrapping data and methods into a single unit.

It protects data from unauthorized access.

## Example

```java
class Student {
    private String name;

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}
```

## Advantages

* Data Security
* Better Control
* Easy Maintenance

---

# 2. Abstraction

Abstraction means hiding implementation details and showing only essential information.

## Abstract Class Example

```java
abstract class Animal {
    abstract void sound();
}
```

```java
class Dog extends Animal {
    void sound() {
        System.out.println("Bark");
    }
}
```

## Advantages

* Reduces Complexity
* Improves Security
* Focuses on Important Features

---

# 3. Inheritance

Inheritance allows one class to acquire properties and methods of another class.

## Syntax

```java
class Parent {
    
}

class Child extends Parent {
    
}
```

## Example

```java
class Animal {
    void eat() {
        System.out.println("Eating");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking");
    }
}
```

## Types of Inheritance

### Single Inheritance

```text
A → B
```

### Multilevel Inheritance

```text
A → B → C
```

### Hierarchical Inheritance

```text
      A
     / \
    B   C
```

### Multiple Inheritance

Not supported directly through classes in Java.

Implemented using Interfaces.

---

# 4. Polymorphism

Polymorphism means "Many Forms".

A single method can perform different tasks.

## Types

### Compile-Time Polymorphism

Method Overloading

```java
class Math {

    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}
```

### Run-Time Polymorphism

Method Overriding

```java
class Animal {
    void sound() {
        System.out.println("Animal Sound");
    }
}

class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Bark");
    }
}
```

---

# Constructor

A constructor is a special method used to initialize objects.

## Example

```java
class Student {

    String name;

    Student(String name) {
        this.name = name;
    }
}
```

---

# Types of Constructors

## Default Constructor

```java
Student() {

}
```

## Parameterized Constructor

```java
Student(String name) {
    this.name = name;
}
```

---

# this Keyword

Refers to the current object.

## Example

```java
class Student {

    String name;

    Student(String name) {
        this.name = name;
    }
}
```

---

# super Keyword

Refers to the parent class object.

## Example

```java
class Animal {
    String color = "White";
}

class Dog extends Animal {

    void display() {
        System.out.println(super.color);
    }
}
```

---

# Interface

An interface contains abstract methods.

## Example

```java
interface Animal {

    void sound();
}
```

```java
class Dog implements Animal {

    public void sound() {
        System.out.println("Bark");
    }
}
```

---

# Difference Between Class and Object

| Class                  | Object             |
| ---------------------- | ------------------ |
| Blueprint              | Instance           |
| Logical Entity         | Physical Entity    |
| No Memory Allocated    | Memory Allocated   |
| Used to Create Objects | Created from Class |

---

# Difference Between Abstract Class and Interface

| Abstract Class                         | Interface                 |
| -------------------------------------- | ------------------------- |
| Can have abstract and concrete methods | Contains abstract methods |
| Supports constructors                  | No constructors           |
| Uses extends                           | Uses implements           |
| Partial abstraction                    | Complete abstraction      |

---

# Advantages of OOPS

* Reusable Code
* Data Security
* Easy Maintenance
* Scalability
* Modularity
* Better Code Organization

---

# Disadvantages of OOPS

* More Memory Usage
* Larger Program Size
* Complex Design for Small Applications

---

# Real-World Example

### Class

```java
Car
```

### Object

```java
BMW
Audi
Tesla
```

### Attributes

```java
Color
Speed
Model
```

### Methods

```java
Start()
Stop()
Accelerate()
```

---

# Conclusion

Object-Oriented Programming System (OOPS) is a powerful programming paradigm that helps developers create modular, reusable, secure, and scalable applications. Understanding the four pillars—Encapsulation, Abstraction, Inheritance, and Polymorphism—is essential for mastering Java and software development.
