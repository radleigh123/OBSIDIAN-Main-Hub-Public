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
**[[UpdateJava|HOME [Java]]]**

---
# Constructors
> special type of method which is used to initialize the object

It is called only once when an object is instantiated. At the time of calling constructor, memory for the object is allocated in the memory. The *constructors* have the following characteristics:
- They are called when the class is being instantiated.
- They must have the same name as the class they’re in.
- They can’t return a value and you don’t specify the keyword `void` as a return type.

**e.g.**
```java
class myClass {
    myClass(int m_num1) {
        System.out.print("Constructor called... ");

        this.m_num1 = m_num1;
    }

    int m_num1;
}

public class Proto {
    public static void main(String[] args) {
        myClass myclass = new myClass(15 + 5);

        System.out.println(myclass.m_num1);
    }
}
```

<br>

More Example:
- [[JavaConstructorsOverloaded|Overloading constructors]]

<br>

# 
---
- https://www.javatpoint.com/java-constructor