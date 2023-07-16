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
## Function Interface
It is a functional interface. It is used to refer method by specifying type of parameter. It returns a result back to the referred function.

Function Chaining
`andThen()`
`compose()`
>[!aside|right]-
> ```
> andThen(): 10
> compose(): true
> ```

```java
import java.util.*;
import java.util.function.*;

public class Solution {
    public static void main(String[] args) {
        Function<Integer, Boolean> func = i -> {
            if (i >= 5) {
                return true;
            }

            return false;
        };

        Function<Boolean, Integer> func2 = j -> j ? 10 : -10;

        // ANDTHEN
        System.out.println("andThen(): " + func.andThen(func2).apply(5));

        // COMPOSE
        System.out.println("compose(): " + func.compose(func2).apply(true));
    }
}
```

<br>

# 
---
- [Java 8 Function Interface - javatpoint](https://www.javatpoint.com/java-function-interface)