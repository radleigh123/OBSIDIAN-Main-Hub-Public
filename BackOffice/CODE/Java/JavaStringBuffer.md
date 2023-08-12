---
aliases:
tags:
- Java
- Java/Lecture
- Java/String/StringBuffer
---
**[[JavaString|BACK]]**

---
## String Buffers
a peer class of **[[JavaString|String]]** that provides much of the functionality of strings.
**e.g.**
```java
StringBuffer sb = new StringBuffer();

sb.append("Hello");
sb.append(" ");
sb.append("World");
// Now the string buffer contains "Hello World"

sb.insert(5, "there");
// Now the string buffer contains "Hello there World"

String finalString = sb.toString();
// The finalString variable now contains "Hello there World"
```

<br>

# 
---
- https://docs.oracle.com/javase/7/docs/api/java/lang/StringBuffer.html
- https://www.geeksforgeeks.org/stringbuffer-class-in-java/