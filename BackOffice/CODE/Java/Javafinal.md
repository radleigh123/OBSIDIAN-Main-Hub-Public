---
title: JavaConstants
creation-date: 2023-02-10
aliases:
tags:
- Java
- Java/final
- Java/static
---
**[[Java#Packages, Interfaces, and Encapsulation|HOME [Java]]]**

---
# `final` Keyword
A **constant** is a value that is <mark class="hltr-lightred">fixed and cannot be changed at runtime</mark>. In Java, **constants** are typically defined using the `final` keyword.  ^c164c7

The value of a constant can be assigned only once. Java developers usually render the names of constants in upper cases.

```java
final double PI = 3.1459;

final String MANUFACTURER = "Yamaha Corp.";
```

<br>

**final Variables**
$\quad$becomes a constant that can be initialized only once and can’t change its value during the runtime. It’s more common to declare them on the class level so they can be reused by several methods of the same class. You can also declare a variable with the keyword [[Javastatic|static]] and with a proper [[JavaAccessModifiers|access]] [[JavaMethod|method]] so they can be used, e.g.,
```java
static final int TEMPERATURE = 215;
```
**final Methods**
$\quad$declaring a class method as `final` means this method can’t be overridden if someone decides to [[JavaInheritance|extend]] the [[JavaClass&Object|class]]. e.g.,
```java
static final double convertToCelsius(double far) {
	return ((far - 32) + 5 / 9);
}
```
**final Classes**
$\quad$If you declare a class as `final`, all its methods become implicitly `final`.and no one will be able to subclass it. e.g.,
>[!aside|show-title right collapse]+ RESULT
> 5

```java
public final class MathUtils {
    public static int add(int a, int b) {
        return a + b;
    }
    
    public static int multiply(int a, int b) {
        return a * b;
    }
}

public class MyApp {
    public static void main(String[] args) {
        int result = MathUtils.add(2, 3); // `static` was declared
        
        System.out.println(result);
    }
}
```

<br>

# 
---
- https://www.baeldung.com/java-final