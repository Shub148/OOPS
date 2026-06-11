# Static Keyword in Java

## Definition

The **static** keyword in Java is used to create variables, methods, blocks, and nested classes that belong to the class rather than an object.

A static member is shared among all instances of the class.

---

## Static Variable

A static variable is common to all objects of a class.

### Example

```java
class Student {
    static String college = "ABC University";
    String name;

    Student(String name) {
        this.name = name;
    }

    void display() {
        System.out.println(name + " studies at " + college);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student("Shubham");
        Student s2 = new Student("Rahul");

        s1.display();
        s2.display();
    }
}
```

### Output

```text
Shubham studies at ABC University
Rahul studies at ABC University
```

---

## Static Method

A static method belongs to the class and can be called without creating an object.

### Example

```java
class MathUtil {
    static int square(int x) {
        return x * x;
    }
}

public class Main {
    public static void main(String[] args) {
        System.out.println(MathUtil.square(5));
    }
}
```

### Output

```text
25
```

---

## Static Block

A static block is executed only once when the class is loaded into memory.

### Example

```java
class Demo {
    static {
        System.out.println("Static Block Executed");
    }

    public static void main(String[] args) {
        System.out.println("Main Method Executed");
    }
}
```

### Output

```text
Static Block Executed
Main Method Executed
```

---

## Static Nested Class

A nested class declared with the static keyword is called a static nested class.

### Example

```java
class Outer {
    static class Inner {
        void show() {
            System.out.println("Inside Static Nested Class");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Outer.Inner obj = new Outer.Inner();
        obj.show();
    }
}
```

### Output

```text
Inside Static Nested Class
```

---

## Important Points

* Static members belong to the class, not objects.
* Memory is allocated only once for static variables.
* Static methods can access only static members directly.
* Static methods cannot use `this` or `super`.
* Static blocks execute before the main method.

---

## Real-World Example

```java
import java.util.*;
class file {
public static void main(String args[]){

Student s1 = new Student();
s1.schoolName = "JNU";

Student s2 = new Student(); /*for this also school name is printed same as s1 school name  because it declared  for every variable or object and stored same value */
System.out.println(s2.schoolName);

Student s3 = new Student();

s3.schoolName = "CHS"; /* So school name is changed for every variable we declare their school name is updated with this name of school because  a static keyword is created only one times */


}

}

class Student{
 String name;
int roll;
static String schoolName;

// Make a setter

void setName(String Name) {
   this.name = name;

}

// Make a getter

String getName(){
  return this.name;

}

}
```

### Output

```text
Total Objects: 3
```

---

## Advantages of Static Keyword

* Saves memory by sharing data among objects.
* Provides utility methods without object creation.
* Useful for constants and common configurations.
* Helps maintain class-level information.

---

## Time Complexity

Static access operations are direct.

```text
Access Static Variable : O(1)
Call Static Method     : O(1)
Space Complexity       : O(1)
```

---

## Conclusion

The `static` keyword is used to create class-level variables and methods that are shared among all objects. It improves memory efficiency and allows utility functionality without creating objects, making it one of the most commonly used keywords in Java.
