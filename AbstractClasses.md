# Abstract Classes in Java

## Definition

An **Abstract Class** in Java is a class that cannot be instantiated (objects cannot be created directly). It is declared using the `abstract` keyword and is primarily used to achieve **abstraction**.

An abstract class can contain:
- Abstract methods (methods without a body)
- Concrete methods (methods with a body)
- Constructors
- Variables

---

## Why Use Abstract Classes?

- To provide a common base for related classes.
- To enforce certain methods to be implemented by subclasses.
- To achieve partial abstraction.
- To promote code reusability.

---

## Syntax

```java
abstract class Animal {

    abstract void sound();

    void eat() {
        System.out.println("Animal is eating");
    }
}
```

---

## Example

```java
abstract class Animal {

    abstract void sound();

    void eat() {
        System.out.println("Animal is eating");
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

        Dog d = new Dog();

        d.sound();
        d.eat();
    }
}
```

### Output

```
Dog barks
Animal is eating
```

---

## Abstract Method

An abstract method is a method declared without a body.

### Syntax

```java
abstract void display();
```

### Example

```java
abstract class Shape {

    abstract void draw();
}

class Circle extends Shape {

    @Override
    void draw() {
        System.out.println("Drawing Circle");
    }
}
```

---

## Rules of Abstract Classes

### 1. Cannot Create Objects

```java
abstract class Animal {
}

public class Main {
    public static void main(String[] args) {

        // Error
        // Animal a = new Animal();
    }
}
```

---

### 2. Can Have Constructors

```java
abstract class Animal {

    Animal() {
        System.out.println("Abstract Class Constructor");
    }
}

class Dog extends Animal {
}
```

### Output

```
Abstract Class Constructor
```

---

### 3. Can Have Concrete Methods

```java
abstract class Animal {

    void eat() {
        System.out.println("Eating...");
    }
}
```

---

### 4. Subclass Must Implement Abstract Methods

```java
abstract class Animal {
    abstract void sound();
}

class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Dog Barks");
    }
}
```

---

## Real-World Example

```java
import java.util.*;
class file {
public static void main(String args[]){

Horse h = new Horse();
h.eat();
h.walk();

Chicken c = new Chicken();
c.eat();
c.walk();


  }
}
abstract class Animal {

void eat(){   // this is same for every animal not defined again for other classes
System.out.println("The Animal is Eat");
}

abstract void walk(); // for every animal it is different and we have to define for other animal 

}

class Horse extends Animal {

void walk(){ // here again we have to define walk but not have to define eat beacuse it is same

System.out.println("Walikng on 4 legs");
}

}
class Chicken extends Animal {

void walk(){

System.out.println("Wlak on 2 legs"); // So here again we have to define walk

}

}




```

### Output

```
50000.0
70000.0
```

---

## Abstract Class vs Interface

| Feature | Abstract Class | Interface |
|----------|---------------|------------|
| Keyword | `abstract` | `interface` |
| Constructors | Allowed | Not Allowed |
| Variables | Instance & Static | Public Static Final |
| Methods | Abstract + Concrete | Abstract, Default, Static |
| Multiple Inheritance | No | Yes |
| Object Creation | Not Allowed | Not Allowed |

---

## Advantages of Abstract Classes

- Provides abstraction.
- Encourages code reuse.
- Supports inheritance.
- Allows partial implementation.
- Improves maintainability.

---

## Disadvantages of Abstract Classes

- Cannot support multiple inheritance.
- Increases complexity if overused.
- Less flexible than interfaces in some cases.

---

## Time Complexity

| Operation | Time Complexity |
|-----------|----------------|
| Method Call | O(1) |
| Abstract Method Override Call | O(1) |

---

## Space Complexity

| Operation | Space Complexity |
|-----------|-----------------|
| Object Creation | O(1) |

---

## Key Points

- Abstract classes are declared using the `abstract` keyword.
- Objects of abstract classes cannot be created.
- Abstract classes can contain both abstract and concrete methods.
- Subclasses must implement all abstract methods.
- Abstract classes support constructors and instance variables.
- Used to achieve partial abstraction.

---

## Summary

An Abstract Class in Java serves as a blueprint for other classes. It allows developers to define common functionality while enforcing subclasses to provide specific implementations. Abstract classes are widely used in real-world applications to achieve abstraction, code reuse, and maintainability.
