---
title: Javaexpressions
creation-date: 2023-02-03
aliases:
tags:
- Java
- Java/Expressions
- Java/Conversion
---
**[[Java|HOME [Java]]]**

---
# Expressions
is a construct made up of variables, operators, and method invocations, which are constructed according to the syntax of the language, that evaluates to a single value.

>[!INFO|clean alt-co txt-c no-t]
> **expression** = operands  operators
> **operands** = values variables numbers quantity
> **operators** = + - * / %

```java
public class Main {
    public static void main(String[] args) {
        int num1 = 10 + 1;
        
        // for compiler to compute floating-point values
        num1 = (int) (num1 * 4.564);

        System.out.print(num1);
    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/nutsandbolts/expressions.html