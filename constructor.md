# Constructor in Java

## Definition
A **Constructor** is a special method in Java that is automatically called when an object of a class is created. It is used to initialize the object's data members.

### Key Points
- Constructor name must be the same as the class name.
- Constructors do not have a return type (not even `void`).
- They are invoked automatically when an object is created.
- Constructors can be overloaded.

---

## Syntax

```java
class Student {
    String name;

    Student() {
        name = "Unknown";
    }
}
```

---

## Example

```java
import java.util.*;
class file{
public static void main(String[] args){  // this is main function
Student s1 = new Student("Vaishnavi", 20); // Creation of new object Student by the help of                                                     //Constructor Student store the name in a string

System.out.println("Name is:  "+s1.name);
System.out.println("Age is: "+s1.age);

  }

}

class Student{  // basically we create a class whose name is student and in which we define 

      String name;   //name 
      int age; //age

Student(String name , int age) {     // this is  a constructor which we create and there is no any return                                    type of this
this.name = name;
this.age = age;

}   // So the constructor we create i.e. Student , so we pass the argument inside this and the          //argument is name

}
```

### Output

```
Name: Vaishnavi
Age: 20
```

---

## Types of Constructors

### 1. Default Constructor

A constructor with no parameters.

```java

import java.util.*;
class file {
public static void main(String args[]){ // Main function
Student s1 = new Student(); /* here we create a object by the help of constructor student and if we can not create this so we can not give any output however code is correct but it shows blank*/
}
}
class Student{  // here we create a class whose name is Student 

Student(){ // create a constructor in which there is no any parameter

System.out.println("There is no parameter"); // print those statment which inside a print statement
}

}
```

### Output

```
Default Constructor Called
```

---

### 2. Parameterized Constructor

A constructor that accepts parameters.

```java
class Demo {
    int num;

    Demo(int num) {
        this.num = num;
    }
}
```

---

### 3. Copy Constructor (User Defined)

Creates an object by copying values from another object.

```java
class Demo {
    int num;

    Demo(int num) {
        this.num = num;
    }

    Demo(Demo obj) {
        this.num = obj.num;
    }
}
```

---

## Constructor Overloading

Multiple constructors with different parameter lists.

```java
class Demo {

    Demo() {
        System.out.println("Default Constructor");
    }

    Demo(int x) {
        System.out.println("Parameterized Constructor");
    }
}
```

---

## Advantages of Constructors

- Initializes objects automatically.
- Improves code readability.
- Ensures object data is properly set.
- Supports constructor overloading for flexibility.

---

## Time Complexity

| Operation | Time Complexity |
|-----------|----------------|
| Constructor Call | O(1) |

---

## Space Complexity

| Operation | Space Complexity |
|-----------|-----------------|
| Object Creation | O(1) |

---

## Real-World Example

```java
class Car {
    String brand;

    Car(String brand) {
        this.brand = brand;
    }

    void display() {
        System.out.println("Car Brand: " + brand);
    }
}

public class Main {
    public static void main(String[] args) {
        Car car = new Car("Toyota");
        car.display();
    }
}
```

### Output

```
Car Brand: Toyota
```

---

## Summary

A constructor is a special method used to initialize objects in Java. It is automatically executed when an object is created and helps ensure that objects start with valid data.
