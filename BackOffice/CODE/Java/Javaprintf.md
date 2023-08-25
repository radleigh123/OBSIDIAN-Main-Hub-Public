---
aliases:
tags:
- Java
- Java/printf
---
**[[Java|HOME [Java]]]**

---
## `printf()`
an optional method to control, format, and display text to the console window two arguments.
**Syntax:**
```java
System.out.printf(locale, format, arguments);
```
**Conversion-characters:**
>[!column|flex no-t collapse]
>>[!INFO|clean no-t collapse]
>> ◾ **[[JavaprintfInteger|%d]]** - int
>> ◾ **[[JavaprintfFloatDouble|%f]]** - double
>> ◾ **[[JavaprintfCharacter|%c]]** - char
>
>>[!INFO|clean no-t collapse]
>> ◾ **[[JavaprintfString|%s]]** - String
>> ◾ **[[JavaprintfBoolean|%b]]** - boolean
>> ◾ **[[JavaprintfTime|%t]]** - date/time values

```java
public class Proto1 {
    public static void main(String[] args) {
        String var1 = "Hello %s %s %s";
        System.out.printf(var1, "!", " + ", null); // Hello! + null
    }
}
```

<br>

### Format specifier rules
```java
%[flags][width][.precision]conversion-character
```
**[width]**
minimum number of characters to be written as output
```java
System.out.printf("Hello%10s", "World");

// Output: Hello          World
```

**[.precision]**
sets number of digits of precision (*floating-point values*)
```java
System.out.printf("Hello%.3f", 3.13254);

// Hello3.132
```

**[flags]**
adds an effect to output based on the flag added to format specifier
>[!column|collapse no-t flex]
>>[!INFO|clean no-t]
>> **-** - left justify
>> **+** - output a plus or minus sign for numeric value
>>> ```java
>>> System.out.printf("%,+d", -1500);
>>> ```
>>
>> &nbsp;
>> **0** - numeric values are zero-padded
>> **,** - comma grouping separator, $\text{numbers}\ \ge\ 1000$


- **%n** - newline

<br>

# 
---
- [Formatting Output with printf() in Java](https://www.baeldung.com/java-printstream-printf)
- https://docs.oracle.com/en/java/javase/12/docs/api/java.base/java/util/Formatter.html#syntax