---
cssclass:
aliases:
tags:
- Java
- Java/Lambda 
- Java/Interface 
---
**[[JavaLambdaFunctionalInterfaces|BACK]]**

---
## Consumer Interfaces
It is a functional interface defined in java.util.function package. It contains an abstract `accept()` and a [[JavaDefault|default]] `andThen()` method. It can be used as the assignment target for a lambda expression or method reference.

The Consumer Interface accepts a single argument and does not return any result.
>[!aside|right]-
> ```
> Hello World
> Earth World
> ```

```java
import java.util.*;
import java.util.function.*;

public class Solution {
    public static void main(String[] args) {
        Consumer<String> con = s -> System.out.print(s);
        Consumer<String> con2 = s -> {
            System.out.println(" World");
        };

        // ANDTHEN
        con.andThen(con2).accept("Hello");

        // OR
        Consumer<String> con3 = con.andThen(con2);
        con3.accept("Earth");
    }
}
```

<br>

# 
---
- [Java 8 Consumer Interface - javatpoint](https://www.javatpoint.com/java-consumer-interface)
- [Java 8 BiConsumer Interface - javatpoint](https://www.javatpoint.com/java-biconsumer-interface)