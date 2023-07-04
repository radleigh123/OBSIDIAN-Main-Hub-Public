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
> <u>`extends` is read-only</u>, meaning if you try to edit, e.g., `numbers.add(123213);`, you would get an error

In *generics*, parameterized types are invariant. In other words, we know that, for instance, the `Long` class is a subtype of a `Number` class. However, it's important to understand that `List<Long>` isn't a subtype of `List<Number>`.
>[!aside|right]-
> Total sum: 711

```java
import java.util.*;
import java.util.stream.Collectors;

public class Solution {
    public static void main(String[] args) {
        List<Long> numbers = new ArrayList<>();

        // converting `List<Integer>` to `List<Long>`
        numbers.addAll(List.of(123, 233, 355).stream()
			.map(Long::valueOf)
				.collect(Collectors.toList()));

        System.out.println("Total sum: " + sum(numbers));
    }

    public static long sum(List<? extends Number> numbers) {
        return numbers.stream()
			.mapToLong(Number::longValue)
				.sum();
    }
}
```

<br>

# 
---
- [wildcard bounds (Baeldung)](https://www.baeldung.com/java-generics-type-parameter-vs-wildcard#bounds)