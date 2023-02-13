---
title: JavaInheritance
creation-date: 2023-02-12
aliases:
tags:
- Java
- Java/Lecture
- Java/Class/Inheritance
- Java/private
- Java/Methods
---
**[[Java|HOME [Java]]]**

---
# Inheritance
is a mechanism in which one object acquires all the properties and behaviors of a parent object.
>[!NOTE]- In Java, multiple and hybrid inheritance is supported through interface only
> ![[JavaInheritanceimage0.png|center wm-sm]] ![[JavaInheritanceimage1.png|center wm-sm]]

**e.g.**
```java
public class Proto1 {
    public static void main(String[] args) {
        Proto3 proto3 = new Proto3();

        System.out.println(proto3.getNumber() + proto3.m_num2);
    }
}

public class Proto2 {
    private int m_num1 = 150;

    int getNumber() {
        return m_num1;
    }
}

class Proto3 extends Proto2 {
    int m_num2 = 50;
}
```

<br>

# 
---
- https://www.javatpoint.com/inheritance-in-java