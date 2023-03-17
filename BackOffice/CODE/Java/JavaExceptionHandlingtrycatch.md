---
aliases:
tags:
- Java
- Java/Exceptions/try
- Java/Exceptions/catch
---
**[[JavaExceptionHandling|BACK]]**

---
## `try` / `catch` block
>[!column|no-t clean atl-co flex]
>>[!INFO|clean no-t]
>> **try**
>> used to specify a block where we should place an exception code. It means we can't use try block alone. The try block must be followed by either catch or finally.
>
>>[!INFO|clean no-t]
>> **catch**
>> is used to handle the exception. It must be preceded by try block which means we can't use catch block alone. It can be followed by finally block later.

Sample try/catch (ArithmeticException):
>[!aside|show-title right]+ RESULT:
> Input two numbers: **5** **0**
> java.lang.ArithmeticException: / by zero
> $\qquad$at Main.main(Main.java:8)

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
	        // e.getMessage() short detail
	        // e.toString() long detail
            e.printStackTrace(); // complete detail
        } catch (Exception e) {
            // It's generally useful to use specific exception to let the user know
            System.out.println("Something went very wrong");
        }
    }
}
```

The order of the catch statements may be important if the exceptions being caught belong to the same inheritance branch. For example, the class `EOFException` is a subclass of the more generic `IOException`, and you have to put the catch block for the subclass first. If you place the catch block for `IOException` before the one for `EOFException`, the latter block will never be reached — the end-of-file errors will be <u>intercepted by the `IOException`</u> catch block.