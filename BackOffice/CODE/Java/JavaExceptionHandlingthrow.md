---
aliases:
tags:
- Java
- Java/Exceptions/throw
---
**[[JavaExceptionHandling|BACK]]**

---
## `throw` keyword -- statement
> If an [[JavaExceptionHandling|exception]] has occurred in a method, you may want to [[JavaExceptionHandlingtrycatch|catch]] the exception, do partial error processing such as **error logging**, or *throw* it to the calling [[JavaMethod|method]] again for further processing or just to make the user aware of the problem. In some cases you may want to catch an exception and handle it but *throw* another exception (with modified error information) to the calling method.

The *throw* statement is used to throw Java exception objects. The object that a program throws must be Throwable (*you can throw a ball, but you can’t throw a grand piano*). This means that you can throw only subclasses of the **[[JavaExceptionHandlingHierarchy|Throwable]]** class and that all Java exceptions are its subclasses.

ArithmeticException sample program:
```java
public class Proto {
    static void validate(int age) {
        if (age < 18) {
            throw new ArithmeticException("Too young");
        } else {
            System.out.println("Eligible to vote");
        }
    }

    public static void main(String[] args) {
        validate(17);
    }
}
```
Result:
>[!INFO|collapse alt-co clean no-t]
> Exception in thread "main" java.lang.ArithmeticException: **Too young**
> $\quad$at Main.validate(Main.java:4)
> $\quad$at Main.main(Main.java:11)

<br>

# 
---
- https://www.javatpoint.com/throw-keyword