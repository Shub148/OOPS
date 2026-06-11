# Super Keyword in Java

## Definition

The **super** keyword in Java is a reference variable used to refer to the immediate parent class object.

It is primarily used to:

1. Access parent class variables.
2. Invoke parent class methods.
3. Call parent class constructors.

---

## 1. Access Parent Class Variable

When a child class and parent class have variables with the same name, `super` is used to access the parent class variable.

### Example

```java
class Animal {
    String color = "White";
}

class Dog extends Animal {
    String color = "Black";

    void display() {
        System.out.println("Child Color: " + color);
        System.out.println("Parent Color: " + super.color);
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.display();
    }
}
```

### Output

```text
Child Color: Black
Parent Color: White
```

---

## 2. Invoke Parent Class Method

`super` can be used to call a method of the parent class when it is overridden in the child class.

### Example

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }

    void display() {
        sound();
        super.sound();
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.display();
    }
}
```

### Output

```text
Dog barks
Animal makes sound
```

---

## 3. Call Parent Class Constructor

`super()` is used to invoke the constructor of the parent class.

### Example

```java
class Animal {
    Animal() {
        System.out.println("Animal Constructor");
    }
}

class Dog extends Animal {
    Dog() {
        super();
        System.out.println("Dog Constructor");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
    }
}
```

### Output

```text
Animal Constructor
Dog Constructor
```

---

## Parameterized Constructor Using super()

### Example

```java
class Animal {
    Animal(String type) {
        System.out.println("Animal Type: " + type);
    }
}

class Dog extends Animal {
    Dog() {
        super("Mammal");
        System.out.println("Dog Constructor");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
    }
}
```

### Output

```text
Animal Type: Mammal
Dog Constructor
```

---

## Important Rules

* `super()` must be the first statement in a constructor.
* `super` refers only to the immediate parent class.
* It cannot be used in a static context.
* If `super()` is not written explicitly, Java automatically calls the default parent constructor.

---

## Difference Between this and super

| Feature          | this                 | super               |
| ---------------- | -------------------- | ------------------- |
| Refers To        | Current Class Object | Parent Class Object |
| Access Variables | Current Class        | Parent Class        |
| Access Methods   | Current Class        | Parent Class        |
| Call Constructor | this()               | super()             |

---

## Real-World Example

```java
import java.util.*;
class file {

public static void main(String args[]){
Horse h1 = new Horse();
System.out.println(h1.color);

}

}

class Animal{
String color;

Animal(){
System.out.println("Animal is Animal");
}

}

class Horse extends Animal{

String color;
super.color = "Black";  // here super automatically inherit the properties of Animal we have to not define them
Run(){
System.out.println("Horse run fast");

}

}
```

### Output

```text
Current Company: Microsoft
Parent Company: Google
```

---

## Advantages of super Keyword

* Accesses parent class members easily.
* Resolves variable hiding problems.
* Enables constructor chaining.
* Supports method overriding implementation.

---

## Time Complexity

```text
Access Parent Variable : O(1)
Call Parent Method     : O(1)
Invoke Constructor     : O(1)
Space Complexity       : O(1)
```

---

## Conclusion

The `super` keyword is used to access members of the parent class and establish communication between parent and child classes. It plays a crucial role in inheritance, method overriding, and constructor chaining in Java.
