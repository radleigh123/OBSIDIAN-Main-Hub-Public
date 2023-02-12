---
title: JavaMethods
creation-date: 2023-02-09
aliases:
tags:
- Java
- Java/Lecture
- Java/Methods
---
**[[Java|HOME [Java]]]**

---
# Methods
a block of code that is executed when it is called upon.
```java
class Proto2 {
    public int addNumber(int a, int b) {
        return a + b;
    }
}

public class Proto1 {
    public static void main(String[] args) {
        Proto2 proto21 = new Proto2(); // creating an instance of Proto2 class
        Proto2 proto22 = new Proto2();

        System.out.println(proto21.addNumber(1, 2));
        System.out.println(proto22.addNumber(10, 2));
    }

}
```

**or**
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
---
- **[[JavaMethodsOverloading|Overloading methods]]**
- **[[JavaMethodsOverriding|Overriding methods]]**

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/javaOO/methods.html