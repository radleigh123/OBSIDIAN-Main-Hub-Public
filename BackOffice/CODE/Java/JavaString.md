---
title: JavaString
creation-date: 2023-02-05
aliases:
tags:
- Java
- Java/Lecture
- Java/String/StringBuffer
- Java/String/equals
- Java/String/length
- Java/String/charAt
- Java/String/indexOf
- Java/String/isEmpty
- Java/String/toUpperCase
- Java/String/toLowerCase
- Java/String/trim
- Java/String/replace
---
**[[Java|HOME [Java]]]**

---
# String class
are constant; their values cannot be changed after they are created.
**[[JavaStringBuffers|String buffers]]** support mutable strings. Because String objects are immutable they can be shared.
**Comparing strings**
```java
String name = "Keane";

// case sensitive
boolean result = name.equals("Keane");

// ignore cases
boolean result = name.equalsIgnoreCase("keane");
```
<br>

**Getting String size**
```java
String greet = "Hello";

System.out.print(greet.length());
```
<br>

**Select specific element**
```java
String greet = "Hello";

System.out.print(greet.charAt(2)); // e
```

**Determine element position**
```java
String greet = "Hello";

System.out.print(greet.indexOf('l')); // 2
```
<br>

**Determine if String is null**
```java
String greet = "";

System.out.print(greet.isEmpty()); // true
```
<br>

**Uppercase & Lowercase**
```java
System.out.print(greet.toUpperCase()); // HELLO
System.out.print(greet.toLowerCase()); // hello
```
<br>

**Trim string**
```java
String greet = "   Hello   ";

System.out.print(greet.trim()); // Hello
```
<br>

**Replace character**
```java
String greet = "Hello";

System.out.print(greet.replace('l', 't')); // Hetto
```

<br>

# 
---
- **[Class String](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html)**