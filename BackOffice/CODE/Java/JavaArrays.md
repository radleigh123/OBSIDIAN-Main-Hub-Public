---
title: JavaArrays
creation-date: 2023-02-05
aliases:
tags:
- Java
- Java/Lecture
- Java/Arrays
---
**[[Java|HOME [Java]]]**

---
# Arrays
is a container object that holds a fixed number of values of a single type.

**Declaring an array:**
```java
// shorthand for "array initializer"
// reccommended when the size of the array can be determined from the elements in the initializer
dataType[] foo = {0, 0, 0, 0};

dataType[] foo = new int[]{0, 0, 0, 0};

dataType[] foo = new int[i];

dataType[] foo;
foo = new int[i];
```

**Getting array size**
```java
int arrayLength = foo.length;
```
<br>

>[!FAIL|alt-co] deprecated
> ```java
> dataType foo[];
> ```

<br>

More examples:
- [[JavaArraysarraycopy|Copying arrays]]
- [[JavaArraysmanipulation|Array manipulation]]
- **[[JavaArraysMultidimensional|Multidimensional Arrays]]**

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html