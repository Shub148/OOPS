# Access Modifiers in Java

## Introduction

Access Modifiers in Java control the visibility and accessibility of classes, variables, methods, and constructors.

They help implement **Encapsulation** by restricting access to data and methods.

---

# Types of Access Modifiers

Java provides four access modifiers:

1. Public
2. Protected
3. Default (Package-Private)
4. Private

---

``` Java
import java.util.*;
class BankAccount{
public String username;
private String password;
public void setPassword(String pwd){

password = pwd;
}
public static void main(String args[]){
BankAccount myAcc = new BankAccount();
myAcc.username = "onerupeespepsi";
myAcc.setPassword("abcdefgh");
}
}
```

# 1. Public Access Modifier

A member declared as `public` can be accessed from anywhere in the program.

## Example

```java
public class Student {

    public String name = "Shubham";
}
```

### Access

```java
Student s = new Student();
System.out.println(s.name);
```

### Features

* Accessible from any package.
* Highest visibility.

---

# 2. Private Access Modifier

A member declared as `private` can only be accessed within the same class.

## Example

```java
class Student {

    private String name = "Shubham";
}
```

### Access Using Getter Method

```java
class Student {

    private String name = "Shubham";

    public String getName() {
        return name;
    }
}
```

### Features

* Most restricted access.
* Used for data hiding.
* Supports encapsulation.

---

# 3. Default Access Modifier

When no access modifier is specified, Java uses the default access modifier.

## Example

```java
class Student {

    String name = "Shubham";
}
```

### Features

* Accessible only within the same package.
* Cannot be accessed outside the package.

---

# 4. Protected Access Modifier

A member declared as `protected` can be accessed:

* Within the same package.
* By subclasses in different packages.

## Example

```java
class Animal {

    protected void sound() {
        System.out.println("Animal Sound");
    }
}
```

```java
class Dog extends Animal {

    void display() {
        sound();
    }
}
```

### Features

* Supports inheritance.
* More accessible than private.
* Less accessible than public.

---

# Accessibility Table

| Modifier  | Same Class | Same Package | Subclass | Other Package |
| --------- | ---------- | ------------ | -------- | ------------- |
| Private   | ✅          | ❌            | ❌        | ❌             |
| Default   | ✅          | ✅            | ❌        | ❌             |
| Protected | ✅          | ✅            | ✅        | ❌             |
| Public    | ✅          | ✅            | ✅        | ✅             |

---

# Access Modifiers for Classes

## Public Class

```java
public class Student {

}
```

Can be accessed from any package.

---

## Default Class

```java
class Student {

}
```

Accessible only within the same package.

---

# Why Use Access Modifiers?

* Data Security
* Encapsulation
* Controlled Access
* Better Code Maintenance
* Prevent Unauthorized Modifications

---

# Real-World Example

## Bank Account

```java
class BankAccount {

    private double balance;

    public void deposit(double amount) {
        balance += amount;
    }

    public double getBalance() {
        return balance;
    }
}
```

### Explanation

* `balance` is private and cannot be modified directly.
* Users interact through public methods.
* Ensures data security.

---

# Difference Between Public and Private

| Public                | Private                      |
| --------------------- | ---------------------------- |
| Accessible Everywhere | Accessible Only Inside Class |
| High Visibility       | Low Visibility               |
| Less Secure           | More Secure                  |
| Used for APIs         | Used for Data Hiding         |

---

# Interview Questions

### 1. What are Access Modifiers?

Access Modifiers control the visibility and accessibility of class members.

### 2. How many Access Modifiers are available in Java?

Four:

* Public
* Protected
* Default
* Private

### 3. Which Access Modifier is the most restrictive?

`private`

### 4. Which Access Modifier is used in inheritance?

`protected`

### 5. Can a top-level class be private?

No.

Top-level classes can only be:

* public
* default

---

# Conclusion

Access Modifiers are an essential feature of Java that help control access to classes, methods, and variables. They improve security, support encapsulation, and make applications more maintainable and robust.
