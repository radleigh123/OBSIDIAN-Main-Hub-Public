---
aliases:
tags:
- Java
- Java/Exceptions/try
- Java/Exceptions/catch
---
**[[JavaExceptionHandling|BACK]]**

---
## `try` keyword
used to specify a block where we should place an exception code. It means we can't use try block alone. The try block must be followed by either catch or finally.

**e.g. (ArithmeticException)**
```java
import java.util.Scanner;

public class Proto {
    public static void main(String[] args) {
        try {
            Scanner sc = new Scanner(System.in);
            System.out.print("Input two numbers: ");
            int z = sc.nextInt() / sc.nextInt();
            sc.close();

            System.out.println("result: " + z);
        } catch (ArithmeticException e) {
            System.out.println("Value can't divide zero");
        } catch (Exception e) {
            // It's generally useful to use specific exception to let the user know
            System.out.println("Something went very wrong");
        }
    }
}
```

<br>

---
## `catch` block
block is used to handle the exception. It must be preceded by try block which means we can't use catch block alone. It can be followed by finally block later.

**e.g.**
```java

```