---
aliases:
tags:
- Java
- Java/printf
- Java/java.util/Locale
---
**[[JavaprintfInteger|BACK]]**

---
<center>package: <strong>java.util.Locale</strong></center>

## `printf()`: Integer formatting
```java
System.out.printf(Locale.US, "%,d%n", 1000000);
System.out.printf(Locale.ITALY, "%,d", 1000000);

/*
* 1,000,000
* 1.000.000
*/
```