---
title: JavaMethods
creation-date: 2023-02-09
aliases:
tags:
- Java
- Java/Lecture
- Java/Methods
---
**[[UpdateJava|HOME [Java]]]**

---
# Methods
a block of code that is executed when it is called upon.

![[JavaMethod.excalidraw.svg|center]]

**e.g.**
```java
public class Proto1 {
    public static void main(String[] args) {
        System.out.println(addNumber(1, 2));
        System.out.println(addNumber(10, 2));
    }

	static int addNumber(int a, int b) {
        return a + b;
    }
}
```

<br>

More example:
- **[[JavaMethodsOverloading|Method Overloading]]**
- **[[JavaMethodsOverriding|Method Overriding]]**

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/javaOO/methods.html