---
cssclass:
aliases:
tags:
- Java
- Java/Operators/Shift 
---
**[[JavaOperatorsShift|BACK]]**

---
## Unsigned Right Shift Operator `>>>`
Unsigned Right Shift Operator moves the bits of the integer a given number of places to the right.
[java - Difference between >>> and >> - Stack Overflow](https://stackoverflow.com/questions/2811319/difference-between-and)
```java
// unsigned right shift of 8
8 = 1000
8 >>> 2 = 0010

// unsigned right shift of -8
 0111
  + 1
______
 1000
-8 = 1000
-8 >>> 2 = 0010

byte num1 = 8;
byte num2 = -8;

System.out.println(num1 >>> 2); // 2
System.out.println(num2 >>> 2); // 1073741822
```
>[!NOTE|collapse ttl-c txt-c alt-co]
> *Unsigned Right Shift Operator moves the bits of the integer a given number of places to the right.*

<br>

**Unsigned Left Shift Operator**
Unlike unsigned Right Shift, there is no `<<<` operator in Java because the <u>logical (`<<`) and arithmetic left-shift (`<<<`) operations are identical</u>.