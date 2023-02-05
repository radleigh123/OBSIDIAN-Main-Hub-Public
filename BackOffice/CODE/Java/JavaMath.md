---
title: JavaMath
creation-date: 2023-02-05
aliases:
tags:
- Java
- Java/Lecture
- Java/Math/max
- Java/Math/round
- Java/Math/ceil
- Java/Math/floor
---
**[[Java|HOME [Java]]]**

---
# Math class
contains methods for performing basic numeric operations such as the elementary exponential, logarithm, square root, and trigonometric functions.
**e.g.**
```java
public class Main {
    public static void main(String[] args) {
        double num1 = 3.49, num2 = -10;

        System.out.println(Math.max(num1, num2)); // alternative `min`
        System.out.println(Math.round(num1));
        System.out.println(Math.ceil(num1)); // always round up
        System.out.println(Math.floor(num1)); // always round down
    }
}
```

**Sample**
- [[JavaMathsample0|Finding the hypotenuse of triangle]]

<br>

# 
---
- **More methods** - https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html