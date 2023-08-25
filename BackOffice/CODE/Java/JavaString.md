---
title: JavaString
creation-date: 2023-02-05
aliases:
tags:
- Java
- Java/String/StringBuffer
- Java/String/equals
- Java/String/length
- Java/String/charAt
- Java/String/indexOf
- Java/String/isEmpty
- Java/String/trim
- Java/String/replace
- Java/toUpperCase
- Java/toLowerCase
---
**[[Java#Java Basics|HOME [Java]]]**

---
# String class
are constant; their values cannot be changed after they are created. **[[JavaStringBuffer|String buffers]]** support mutable strings. Because String objects are immutable they can be shared.
> ```java
> // String text block
> String input = """
> 			123
> 			Hello World
> 			Keane 123 Rhizome
> 			""";
> ```

<br>

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