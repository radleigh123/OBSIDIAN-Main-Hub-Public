---
aliases:
tags:
- Java
- Java/printf
- Java/java.util/Date
---
**[[Javaprintf|BACK]]**

---
<center>package: <strong>java.util.Date</strong></center>

## `printf()`: Date & Time formatting
**Time formatting**
suffix characters for time formatting:
>[!column|flex collapse no-t]
>>[!INFO|clean no-t collapse]
>> **H** - hours
>> **M** - minutes
>> **S** - seconds
>> **L** - milliseconds
>> **N** - nanoseconds
>
>>[!INFO|clean no-t collapse]
>> **p** - a.m./p.m. formatting
>> **z** - time-zone offset

```java
System.out.printf("hours %tH : minutes %tM : seconds %tS", date, date, date);

System.out.printf("%1$tH:%1$tM:%1$tS %1$tp %1$tL %1$tN %1$tz %n", date); // `1$` one argument

/*
* hours 15 : minutes 15 : seconds 00
* 15:15:00 pm 183 183000000 +0800
*/
```

<br>

**Date formatting**
special formatting characters for date formatting:
>[!column|flex collapse no-t]
>>[!INFO|clean no-t collapse]
>> **A** - full day of the week
>> **d** - two-digit day of the month
>> **B** - full month name
>> **m** - two-digit month
>
>>[!INFO|clean no-t collapse]
>> **Y** - year in four digits
>> **y** - last two digits of the year

```java
System.out.printf("%1$tA, %1$tB %1$tY %n", date);

System.out.printf("%1$td.%1$tm.%1$ty %n", date);

/*
* Thursday, November 2018
* 22.11.18
*/
```