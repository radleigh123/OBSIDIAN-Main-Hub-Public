---
title: JavaAbstraction
creation-date: 2023-02-12
aliases:
tags:
- Java
- Java/Class/Constructor
- Java/Class/Inheritance
- Java/Class/Abstract
---
**[[Java#Packages, Interfaces, and Encapsulation|HOME [Java]]]**

---
## `abstract` Keyword
is a process of hiding the implementation details and showing only the essential features of an object, class, or method.

**[[JavaAbstractClass|abstract class]]** - is a class that is declared `abstract`—it may or may not include abstract methods. Abstract classes cannot be instantiated, but they can be subclassed.

**abstract method** - is a method that is declared without an implementation (without braces, and followed by a semicolon), e.g.:
```java
abstract void moveTo(double deltaX, double deltaY);
```

**e.g.**
```java
abstract class Proto2 {
    abstract void go(); // now meant to be overriden
}

class Proto3 extends Proto2 {
    int m_num1 = 150; // inaccessible

    @Override
    void go() {
        System.out.println("Proto3::go()....");
    }
}

class Proto4 extends Proto2 {
    @Override
    void go() {
        System.out.println("Proto4::go()....");
    }
}

public class Proto1 {
    public static void main(String[] args) {
        Proto2 proto3 = new Proto3();

        proto3.go();
        proto3 = new Proto4();
        proto3.go();
    }
}
```

<br>

See more:
▪$\ \,$**[[JavaInterface|Interface]]**

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/IandI/abstract.html