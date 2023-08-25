---
aliases:
tags:
- Java
- Java/printf
---
**[[Javaprintf|BACK]]**

---
## `printf()`: Boolean formatting
According to the docs, it works the following way: if the second argument is **null**, then the result is “false”. If the argument is a `boolean` or `Boolean`, then the result is the string returned by `String.valueOf(arg)`. Otherwise, the result is “true”.
```java
System.out.printf("%b%n", null);
System.out.printf("%B%n", false); // uppercase formatting
System.out.printf("%B%n", 5.3);
System.out.printf("%b%n", "random text");

/*
* false
* FALSE
* TRUE
* true
*/
```