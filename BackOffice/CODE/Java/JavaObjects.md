---
title: JavaObjects
creation-date: 2023-02-10
aliases:
tags:
- Java
- Java/Lecture
- Java/Class/Constructor
- Java/this
---
**[[Java|HOME [Java]]]**

---
# Objects
> **An object is an instance of a class.** A class is a template or blueprint from which objects are created. So, an object is the instance(result) of a class.

An entity that has state and behavior is known as an object e.g., chair, bike, marker, pen, table, car, etc.
![[JavaObjectsimage0.png|center ws-med]]

**e.g.**
```java
class Proto2 {
    Proto2(int m_num1) {
        System.out.println("Constructor called\n");

        this.m_num1 = m_num1;
    }

    void addNumbers() {
        System.out.println("Proto2::addNumbers() called... " + m_num1);
    }

    int m_num1;
}

public class Proto1 {
    public static void main(String[] args) {
        Proto2 proto21 = new Proto2(15);
        Proto2 proto22 = new Proto2(21);

        proto21.addNumbers(); // 15
        proto22.addNumbers(); // 21
    }
}
```

<br>

---
**Learn more**
- [[JavaObjectsarrays|Array of Objects]]
- [[JavaObjectsCopy|Copy objects]] ^1a283e

<br>

# 
---
- https://docs.oracle.com/javase/7/docs/api/java/lang/Object.html
- https://www.javatpoint.com/object-and-class-in-java