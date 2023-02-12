---
title: JavaConstructors
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
# Constructors
> special type of method which is used to initialize the object

It is called when an object is instantiated. At the time of calling constructor, memory for the object is allocated in the memory.
**e.g.**
```java
class Proto2 {
    Proto2(int m_num1) {
        System.out.println("Constructor called\n");

        this.m_num1 = m_num1;
    }

    int m_num1;
}

public class Proto1 {
    public static void main(String[] args) {
        Proto2 proto21 = new Proto2(15 + 5);

        System.out.println(proto21.m_num1);
    }
}
```

<br>

---
- [[JavaConstructorsOverloaded|Overloading constructors]]

<br>

# 
---
- https://www.javatpoint.com/java-constructor