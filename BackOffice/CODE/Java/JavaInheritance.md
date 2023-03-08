---
title: JavaInheritance
creation-date: 2023-02-12
aliases:
tags:
- Java
- Java/Lecture
- Java/Class/Inheritance
- Java/Methods
---
**[[Java|HOME [Java]]]**

---
# Inheritance
is a mechanism in which one object acquires all the properties and behaviors of a parent object. In OO languages the term *inheritance* means an <mark class="hltr-lightgreen">ability to define a new class based on an existing one</mark> (not from scratch).

>[!WARNING|ttl-c alt-co]- In Java, multiple and hybrid inheritance is supported through interface only
> ![[JavaInheritanceimage0.png|center wm-sm]] ![[JavaInheritanceimage1.png|center wm-sm]]

**e.g.**
```java
public class Proto1 {

    public static void main(String[] args) {
        DerivedClass derived = new DerivedClass();

        System.out.println(derived.getNumber() + derived.m_num2);
    }

}

public class BaseClass {
    private int m_num1 = 150;

    int getNumber() {
        return m_num1;
    }
}

class DerivedClass extends BaseClass {
    int m_num2 = 50;
}

/* The class DerivedClass will have all the features the class BaseClass has. In such a setup, the BaseClass is called a superclass, and DerivedClass is called a subclass (can also use the terms `ancestor` and `descendent`).
*/
```

More examples:
- [[Javasuper|super keyword]]

<br>

# 
---
- https://www.javatpoint.com/inheritance-in-java