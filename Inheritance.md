# Inheritance in Java

## Definition

**Inheritance** is an Object-Oriented Programming (OOP) concept that allows one class to acquire the properties and behaviors (fields and methods) of another class.

The class that inherits is called the **Child Class (Subclass)**, and the class whose properties are inherited is called the **Parent Class (Superclass)**.

---

## Why Use Inheritance?

- Promotes code reusability.
- Reduces code duplication.
- Improves maintainability.
- Supports method overriding and polymorphism.

---

## Syntax

```java
class Parent {
    // fields and methods
}

class Child extends Parent {
    // additional fields and methods
}
```

---

## Example

```java
import java.util.*;
class file {
 public static void main(String args[]){
     Fish Dolphine = new Fish();
     Dolphine.eat();
     Dolphine.swim();
     Dolphine.dubaki();
     Dolphine.marat();
     Dolphine.dance();
     
 }   
    
    
}

// Base Class
class Animal{
    String color;
    int number;
    void eat(){
        System.out.println("Animal Khana kha raha hai");
    }
    
    void swim(){
        System.out.println("animal tairat hai");
    }
    
}


// Derived class
class Fish extends Animal{
 int fins;
 
 void dubaki(){
     System.out.println("animal dubaki marat hai");
 }
 void marat(){
     System.out.println("Fish marat hai");
 }
   void dance(){
       
       System.out.println("Fish dance karat hai");
   } 
}

// Base Class

class Animal{
String color;  // Properties of Animal

void eat(){  // funstion of animal

System.out.println("eats");
}

void breathe(){  // Another function of animals

System.out.println("breathe");
}
}

// Derived class

class fish extends Animal{ // when we used extend Animal so it include all the property of animal

int fins;  //  another proerty of fish

void swim(){
   System.out.println("swims in water");

}
}

```

### Output

```
Animal is breathing
fish is swim
```

---

## Types of Inheritance in Java

### 1. Single Inheritance

One child class inherits from one parent class.

```java
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking...");
    }
}
```

---

### 2. Multilevel Inheritance

A class inherits from a class that already inherits another class.

```java
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking...");
    }
}

class Puppy extends Dog {
    void weep() {
        System.out.println("Weeping...");
    }
}
```

---

### 3. Hierarchical Inheritance

Multiple child classes inherit from the same parent class.

```java
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking...");
    }
}

class Cat extends Animal {
    void meow() {
        System.out.println("Meowing...");
    }
}
```

---

### 4. Multiple Inheritance (Through Interfaces)

Java does not support multiple inheritance with classes to avoid ambiguity, but it supports multiple inheritance using interfaces.

```java
interface A {
    void show();
}

interface B {
    void display();
}

class Demo implements A, B {

    public void show() {
        System.out.println("Show Method");
    }

    public void display() {
        System.out.println("Display Method");
    }
}
```

---

## The `super` Keyword

The `super` keyword is used to refer to the immediate parent class object.

### Example

```java
class Animal {
    String color = "White";
}

class Dog extends Animal {
    String color = "Black";

    void printColor() {
        System.out.println(super.color);
    }
}
```

### Output

```
White
```

---

## Method Overriding with Inheritance

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}
```

### Output

```
Dog barks
```

---

## Advantages of Inheritance

- Code reusability.
- Easy maintenance.
- Faster development.
- Supports runtime polymorphism.
- Establishes parent-child relationships.

---

## Disadvantages of Inheritance

- Tight coupling between classes.
- Changes in parent class may affect child classes.
- Can make code complex if overused.

---

## Real-World Example

```java
class Vehicle {
    void start() {
        System.out.println("Vehicle Started");
    }
}

class Car extends Vehicle {
    void drive() {
        System.out.println("Car is Driving");
    }
}

public class Main {
    public static void main(String[] args) {
        Car car = new Car();

        car.start();
        car.drive();
    }
}
```

### Output

```
Vehicle Started
Car is Driving
```

---

## Time Complexity

| Operation | Time Complexity |
|-----------|----------------|
| Method Call | O(1) |
| Inherited Method Access | O(1) |

---

## Space Complexity

| Operation | Space Complexity |
|-----------|-----------------|
| Object Creation | O(1) |

---

## Key Points

- Inheritance is achieved using the `extends` keyword.
- Java supports Single, Multilevel, and Hierarchical inheritance through classes.
- Multiple inheritance is supported through interfaces.
- The `super` keyword accesses parent class members.
- Inheritance promotes code reusability and maintainability.

---

## Summary

Inheritance is a fundamental OOP concept that enables one class to inherit the properties and methods of another class. It helps create reusable, organized, and maintainable code while supporting advanced concepts like polymorphism and method overriding.
