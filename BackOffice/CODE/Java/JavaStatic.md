---
title: JavaStatic
creation-date: 2023-02-12
aliases:
tags:
- Java
- Java/static
---
**[[Java#Class Methods|HOME [Java]]]**

---
# `static` keyword
is used to declare class-level members.

it means that the member(variable or method) belongs to the class, rather than to a specific instance of the class. This means that the method can be called without creating an [[JavaClass&Object|object]] of the class.
>[!aside|right show-title]+ RESULT:
> 3 of total

```java
public class Proto1 {
    public static void main(String[] args) {
        Proto2 person1 = new Proto2("Keane");
        Proto2 person2 = new Proto2("Radleigh");
        Proto2 person3 = new Proto2("World");

        Proto2.displayCount(); // because method is STATIC
    }
}

public class Proto2 {
    String name;
    static int count; // STATIC, shares its increment

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

More example:
- [[JavastaticSample0|Converting Farenheit to Celsius]]

<br>

# 
---
- [A Guide to the Static Keyword](https://www.baeldung.com/java-static#:~:text=In%20the%20Java%20programming%20language,all%20instances%20of%20the%20class.)