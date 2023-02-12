---
title: JavatoString
creation-date: 2023-02-10
aliases:
tags:
- Java
- Java/Lecture
- Java/toString
- Java/toHexString
- Java/Class
- Java/toUpperCase
---
**[[Java|HOME [Java]]]**

---
# `toString()` method
> any object that this method is applied on, will then be returned as a `string` object.

a built-in method in Java that returns the value given to it in _string_ format.

**e.g.**
```java
public class Proto1 {
    public static void main(String[] args) {
        int num1 = 450;

        System.out.println(Integer.toString(num1));

        System.out.println(Integer.toHexString(45).toUpperCase());
    }
}
```

<br>

**Override `toString()`**
```java
class Proto2 {
    String var1 = "Mars";
    String var2 = "Hello";
    String var3 = "Venus";

    public String toString() {
        return var1 + "\n" + var2 + "\n" + var3;
    }
}

public class Proto1 {
    public static void main(String[] args) {
        Proto2 proto2 = new Proto2();

        System.out.println(proto2.toString());
    }
}
```

**Using `toString()` to get address**
```java
myClass myclass = new myClass();

System.out.print(myclass.toString()); // prints address
```

<br>

# 
---
- https://www.educative.io/answers/how-to-use-the-tostring-in-java