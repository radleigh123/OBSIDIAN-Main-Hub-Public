---
aliases:
tags:
- Java
- Java/Exceptions/finally
---
**[[JavaExceptionHandling|BACK]]**

---
## `finally` block
is used to execute the necessary code of the program. It is executed whether an exception is handled or not.

The code can exit the [[JavaExceptionHandlingtrycatch|try/catch]] block in several ways:
$\quad$▪$\,$The code inside the *try block* successfully ends and the program continues.
$\quad$▪$\,$The code inside the *try block* runs into a `return` statement.
$\quad$▪$\,$The code inside the *try block* throws an exception and control goes to the *catch block*.

> If you are not planning to handle exceptions in the current [[JavaMethod|method]], they will be propagated to the calling one. In this case you can use the *finally clause* without the catch clause.

**e.g.**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            System.out.print("Input two numbers: ");
            int z = sc.nextInt() / sc.nextInt();

            System.out.println("result: " + z);
        } catch (ArithmeticException e) {
            System.out.println(e.getMessage());
        } finally {
            System.out.println("This will always print");

            sc.close(); // Good thing for closing
        }
    }
}
```
Result:
>[!INFO|collapse alt-co clean no-t]
> Input two numbers: **150** **0**
> / by zero
> This will always print