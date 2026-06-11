# Interfaces in Java

## Definition

An **interface** in Java is a blueprint of a class that contains abstract methods and constants. It is used to achieve **abstraction** and **multiple inheritance** in Java.

An interface defines **what a class should do**, but not **how it should do it**.

---

## Syntax

```java
interface Animal {
    void sound();
}
```

Implementing an Interface:

```java
class Dog implements Animal {
    public void sound() {
        System.out.println("Bark");
    }
}
```

---

## Example Program

```java
import java.util.*;
class file {
public static void main(String args[]){
 Queen q = new Queen();
     q.moves();

Rook r = new Rook();
  r.moves();

King k = new King();
  k.moves();

  }
}
interface ChessPlayer {
  void moves();

}

class Queen implements ChessPlayer {
public void moves() {
System.out.println("up, right, left, down, diagonal (in all 4 directions)");
}
  }

class Rook implements ChessPlayer {
public void moves() {
  System.out.println("up, down, left, right");
  }
}

class King implements ChessPlayer {
  public void moves(){
System.out.println("up, down, bottom, left, right,diagonal( by 1 step)");
    }

}
```

### Output

```text
Car is starting...
```

---

## Features of Interfaces

* Supports abstraction.
* Supports multiple inheritance.
* Methods are public and abstract by default.
* Variables are public, static, and final by default.
* Cannot be instantiated.
* A class can implement multiple interfaces.

---

## Multiple Inheritance Using Interfaces

```java
interface A {
    void show();
}

interface B {
    void display();
}

class Demo implements A, B {
    public void show() {
        System.out.println("Method of Interface A");
    }

    public void display() {
        System.out.println("Method of Interface B");
    }
}

public class Main {
    public static void main(String[] args) {
        Demo d = new Demo();
        d.show();
        d.display();
    }
}
```

### Output

```text
Method of Interface A
Method of Interface B
```

---

## Default Methods (Java 8+)

```java
interface Test {
    default void message() {
        System.out.println("Default Method");
    }
}

class Demo implements Test {}

public class Main {
    public static void main(String[] args) {
        Demo d = new Demo();
        d.message();
    }
}
```

### Output

```text
Default Method
```

---

## Static Methods in Interface

```java
interface MathUtil {
    static void display() {
        System.out.println("Static Method in Interface");
    }
}

public class Main {
    public static void main(String[] args) {
        MathUtil.display();
    }
}
```

### Output

```text
Static Method in Interface
```

---

## Advantages

* Provides complete abstraction.
* Supports multiple inheritance.
* Improves code flexibility and maintainability.
* Promotes loose coupling between classes.
* Useful for defining contracts between classes.

---

## Difference Between Abstract Class and Interface

| Feature              | Abstract Class      | Interface                 |
| -------------------- | ------------------- | ------------------------- |
| Methods              | Abstract + Concrete | Abstract, Default, Static |
| Multiple Inheritance | Not Supported       | Supported                 |
| Constructors         | Yes                 | No                        |
| Variables            | Any Type            | public static final       |
| Access Modifiers     | Any                 | Public by Default         |

---

## Time Complexity

Interface declaration itself does not have any time complexity.

Method calls through interfaces have:

```text
Time Complexity: O(1)
Space Complexity: O(1)
```

---

## Conclusion

Interfaces are one of the most important concepts in Java. They help achieve abstraction, support multiple inheritance, and make applications more modular, scalable, and maintainable.
