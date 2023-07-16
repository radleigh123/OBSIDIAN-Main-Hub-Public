---
cssclass:
aliases:
tags:
- Java
- 
---
**[[JavaLambdaFunctionalInterfaces|BACK]]**

---
## Predicate Interface
It is a functional interface which represents a predicate (boolean-valued function) of one argument. It is defined in the `java.util.functio`n package and contains test() a functional method.

Joining multiple Predicate interfaces: `and`, `or`, `negate`
>[!aside|right]-
> ```
> AND 30 40
> 
> OR 10 20 25 30 35 40
> 
> NEGATE 5 15
> ```

```java
import java.util.*;
import java.util.function.*;

public class Solution {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<>();
        list.addAll(Arrays.asList(5, 15, 20, 25, 30, 35, 40));

        Predicate<Integer> pred1 = i -> (i % 2 == 0);
        Predicate<Integer> pred2 = i -> (i > 20);

        for (Integer n : list) {
	        // AND
            if (pred1.and(pred2).test(n)) {
                System.out.print(n + " ");
            }
            
            System.out.println();

			// OR
            if (pred1.or(pred2).test(n)) {
                System.out.print(n + " ");
            }

			// NEGATE
			if (pred1.or(pred2).negate().test(n)) {
                System.out.print(n + " ");
            }
        }
    }
}
```

<br>

# 
---
- [Java 8 Predicate Interface - javatpoint](https://www.javatpoint.com/java-predicate-interface)