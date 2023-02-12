---
aliases:
tags:
- Java
- Java/printf
- Java/java.util/Locale
---
**[[Javaprintf|BACK]]**

---
## `printf()`: Float & Double formatting
```java
System.out.printf(Locale.US, "%,.2f%n", 12600.364);
System.out.printf(Locale.US, "%,10.2f", 11000.364);

/*
* 12,600.36
*  11,000.36
*/
```

<br>

**`e`/`E` conversion-character**
```java
System.out.printf("%,.3f%n", 8979879875.4565);
System.out.printf("%.3E", 8979879875.4565);

/*
* 8,979,879,875.457
* 8.980E+09
*/
```