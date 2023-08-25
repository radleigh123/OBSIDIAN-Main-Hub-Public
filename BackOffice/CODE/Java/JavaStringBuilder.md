---
cssclass:
aliases:
tags:
- Java
- Java/String 
---
**[[Java#Java Basics|HOME [Java]]]**

---
## StringBuilder Class
Since the `String` class in Java creates an immutable sequence of characters, the `StringBuilder` class provides an alternative to `String` class, as it creates a mutable sequence of characters.

Constructors:
```java
// Constructs a string builder with no characters in it and an initial capacity of 16 characters.
StringBuilder()

// Constructs a string builder with no characters in it and an initial capacity specified by the capacity argument.
StringBuilder(int capacity)

// Constructs a string builder that contains the same characters as the specified CharSequence.
StringBuilder(CharSequence seq)

// Constructs a string builder initialized to the contents of the specified string.
StringBuilder(String str)
```

<br>

# 
---
- [StringBuilder (Java Platform SE 8 ) (oracle.com)](https://docs.oracle.com/javase/8/docs/api/java/lang/StringBuilder.html)
- [StringBuilder Class in Java with Examples - GeeksforGeeks](https://www.geeksforgeeks.org/stringbuilder-class-in-java-with-examples/)
- See also:
	- [[JavaStringBuffer|StringBuffer class]]