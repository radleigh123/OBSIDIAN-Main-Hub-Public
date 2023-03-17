---
cssclass:
aliases:
tags:
- Java
- Java/Exceptions
- Java/StackTrace
---
**[[UpdateJava#Error Handling|HOME [Java]]]**

---
## Stack Trace
also called a *stack backtrace* or even just a backtrace, is a list of stack frames. These frames represent a moment during an application’s execution. A stack frame is information about a method or function that your code called. So the Java stack trace is a list of frames that starts at the current method and extends to when the program started.
```java
/**
 * Example stack trace divide by zero
 */

public class Main {
    Main() {
        divideByZero();
    }

    int divideByZero() {
        return (25 / 0);
    }

    public static void main(String[] args) {
        new Main();
    }
}
```
**Result:**
>[!INFO|alt-co clean no-t collapse]
> Exception in thread "main" java.lang.ArithmeticException: / by zero
> $\qquad$at Main.divideByZero(Main.java:**9**) 
> $\qquad$at Main.\<init>(Main.java:**4**)
> $\qquad$at Main.main(Main.java:**14**)

It shows that the program was executing the methods `main()`, `init()`, and `divideByZero()`. The line numbers **14**, **4**, and **9**, respectively, indicate where in the program these methods were called. After that the `ArithmeticException` was thrown — the code in line **9** tried to divide by zero.

Executing any Java program means running [[JavaThreadsMulti|multiple threads]], and the stack trace output reflects what was happening in the main thread of the sample *TestStackTrace program*.

<br>

# 
---
- https://www.sentinelone.com/blog/java-stack-trace-understanding/