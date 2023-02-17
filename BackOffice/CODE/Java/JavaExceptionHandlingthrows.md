---
aliases:
tags:
- Java
- Java/Exceptions/throws
---
**[[JavaExceptionHandling|BACK]]**

---
## `throws` keyword
is used to declare exceptions. It specifies that there may occur an exception in the method. It doesn't throw an exception. It is always used with method signature.

**e.g.**
```java
import java.io.*;

class M {
    void method() throws IOException {
        throw new IOException("device error");
    }
}

public class Proto {
    public static void main(String args[]) throws IOException {// declare exception
        M m = new M();
        m.method();

        System.out.println("normal flow...");
    }
}
```

<br>

# 
---
- https://www.javatpoint.com/throws-keyword-and-difference-between-throw-and-throws