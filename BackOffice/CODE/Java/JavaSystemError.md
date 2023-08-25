---
aliases:
tags:
- Java
- Java/System.err
---
**[[Java#Introduction|HOME [Java]]]**

---
## System Error
is a standard error output stream that is used to write error messages. It is a PrintStream object that is automatically created by the Java runtime system, and it is connected to the standard error device (usually the console).
```java
public static void main(String[] args) {
  System.err.println("An error occurred.");
}
```

<br>

# 
---
- [Java System.in, System.out, and System.error](https://jenkov.com/tutorials/java-io/system-in-out-error.html)
- [Difference between System.out.println() and System.err.println()](https://stackoverflow.com/questions/3163399/difference-between-system-out-println-and-system-err-println)