---
title: JavaStatic
creation-date: 2023-02-12
aliases:
tags:
- Java
- Java/Lecture
- Java/static
---
**[[Java|HOME [Java]]]**

---
# `static` keyword
> it means that the [[JavaMethods|method]] belongs to the class, rather than to a specific instance of the class. This means that the method can be called without creating an [[JavaObjects|object]] of the class.

means that the particular member belongs to a type itself, rather than to an instance of that type.
**e.g.**
```java
public class Proto1 {
    public static void main(String[] args) {
        Proto2 person1 = new Proto2("Keane");
        Proto2 person2 = new Proto2("Radleigh");
        Proto2 person3 = new Proto2("World");

        Proto2.displayCount();
    }
}

public class Proto2 {
    String name;
    static int count;

    Proto2(String name) {
        this.name = name;
        count++;
    }

    static void displayCount() {
        System.out.printf("%d of total%n", count);
        return;
    }
}
```

<br>

# 
---
- [A Guide to the Static Keyword](https://www.baeldung.com/java-static#:~:text=In%20the%20Java%20programming%20language,all%20instances%20of%20the%20class.)