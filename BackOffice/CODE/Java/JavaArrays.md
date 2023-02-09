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
>[!recite|alt-co clean no-i collapse] **[[JavaArraysMultidimensional|Multidimensional Arrays]]**

**Declaring an array:**
```java
// shorthand for "array initializer"
// reccommended when the size of the array can be determined from the elements in the initializer
dataType[] foo = {0, 0, 0, 0};
```
<br>

```java
dataType[] foo = new int[i];
```
```java
dataType[] foo;
foo = new int[i];
```
```java
dataType[] foo = new int[]{0, 0, 0, 0};
```

**Getting array size**
```java
System.out.print(foo.length);
```
<br>

>[!FAIL|alt-co txt-c ttl-c] deprecated
> **dataType foo[];**

---
- [[JavaArraysarraycopy|Copying arrays]]
- [[JavaArraysmanipulation|Array manipulation]]

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html