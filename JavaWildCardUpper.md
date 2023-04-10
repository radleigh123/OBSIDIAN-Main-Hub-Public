---
cssclass:
aliases:
tags:
- Java
- Java/Wildcards/UpperBounded
---
**[[JavaWildCard|BACK]]**

---
## Upper Bounded Wildcard
In *generics*, parameterized types are invariant. In other words, we know that, for instance, the `Long` class is a subtype of a `Number` class. However, it's important to understand that `List<Long>` isn't a subtype of `List<Number>`.
>[!aside|right show-title]+ RESULT:
> Total sum: 200

```java
import java.util.Arrays;
import java.util.List;

public class Main {

    public static void main(String[] args) {
        List<Integer> numbers = Arrays.asList(150, 5, 45);
        
        System.out.println("Total sum: " + Main.sum(numbers));
    }

    public static long sum(List<? extends Number> numbers) {
        return numbers.stream().mapToLong(Number::longValue).sum();
    }
}
```

<br>

# 
---
- [wildcard bounds (Baeldung)](https://www.baeldung.com/java-generics-type-parameter-vs-wildcard#bounds)