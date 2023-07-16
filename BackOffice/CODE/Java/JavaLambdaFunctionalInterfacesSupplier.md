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
## Supplier Interface
It represents a function which does not take in any argument but produces a value of type `T`. It represents a function which does not take in any argument but produces a value of type `T`.
>[!aside|right]-
> ```
> 15
> ```

```java
import java.util.*;
import java.util.function.*;

public class Solution {
    public static void main(String[] args) {
        Supplier<Integer> sup = () -> 15;

        System.out.println(sup.get());
    }
}
```
>[!aside|right]-
> ```
> 0.5685808855697841
> ```

```java
import java.util.function.Supplier;

public class Solution {
    public static void main(String args[]) {
        Supplier<Double> randomValue = () -> {
            return Math.random();
        };

        System.out.println(randomValue.get());
    }
}
```

<br>

# 
---
- [Supplier (Java Platform SE 8 ) (oracle.com)](https://docs.oracle.com/javase/8/docs/api/java/util/function/Supplier.html)
- 