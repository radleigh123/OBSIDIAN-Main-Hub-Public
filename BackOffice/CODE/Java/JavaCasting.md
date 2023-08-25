---
cssclass:
title: JavaCasting
creation-date: 2023-03-14
aliases:
tags:
- Java
- Java/Object
- Java/typecasting
---
**[[Java|HOME [Java]]]**

---
# Casting
> All Java classes form an [[JavaInheritance|inheritance]] tree with the class [[JavaObject|Object]] on top of the hierarchy — all Java classes are direct or indirect descendants of **Object**.

Java is smart enough to automatically cast an instance of the class to its ancestor. When the <mark class="hltr-lightgreen">variable has more generic type than an instance of the object</mark> this is called **upcasting**.
```java
public class Main {
    public static void main(String[] args) {
        myClass2 myclass1 = new myClass2();
        baseClass myclass2 = new myClass2(); //upcasting
        Object myclass3 = new myClass2(); //upcasting
    }
}
```

More examples:
- [[JavaCastingSample|Testing data types using instanceof]]

<br>

# 
---
- https://www.w3schools.com/java/java_type_casting.asp
- https://www.baeldung.com/java-type-casting