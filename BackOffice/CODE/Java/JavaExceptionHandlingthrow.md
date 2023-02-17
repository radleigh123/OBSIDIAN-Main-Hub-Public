---
aliases:
tags:
- Java
- Java/Exceptions/throw
---
**[[JavaExceptionHandling|BACK]]**

---
## `throw` keyword
used to declare an exception. It gives an information to the programmer that there may occur an exception.

**e.g.**
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

<br>

# 
---
- https://www.javatpoint.com/throw-keyword