---
cssclass:
aliases:
tags:
- Java
- Java/Wildcards/UnBounded
---
**[[JavaWildCard|BACK]]**

---
## Unbounded Wildcard
This wildcard type is specified using the wildcard character `?`. This is called a list of unknown types. These are useful in the following cases –
$\quad$▪ When writing a method that can be employed using functionality provided in Object class.
$\quad$▪ When the code is using methods in the generic class that doesn’t depend on the type parameter.

>[!aside|right show-title]+ RESULT:
> \[1, 2, 3]
> \[1.1, 2.2, 3.3]

```java
import java.util.Arrays;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<Integer> list1 = Arrays.asList(1, 2, 3);
        printlist(list1);

        List<Double> list2 = Arrays.asList(1.1, 2.2, 3.3);
        printlist(list2);
    }

    private static void printlist(List<?> list) {
        System.out.println(list);
    }
}
```

<br>

# 
---
- [wildcard bounds (Baeldung)](https://www.baeldung.com/java-generics-type-parameter-vs-wildcard#bounds)