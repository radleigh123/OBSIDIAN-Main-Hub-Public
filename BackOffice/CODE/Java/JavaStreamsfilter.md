---
cssclass:
aliases:
tags:
- Java
- Java/Streams/stream/filter
---
**[[JavaStreams|BACK]]**

---
## `filter()` Operation
>[!aside|right]-
> ```
> [2, 4]
> 2  4  
> 24
> ```

```java
import java.util.*;
import java.util.stream.*;

public class Solution {
    public static void main(String args[]) {
        List<Integer> list = Arrays.asList(1, 2, 3, 4);
        List<Integer> evenList = new ArrayList<>();

        /*
        // w/out using streams
        for (Integer i : list) {
			if (i % 2 == 0)
			evenList.add(i);
        }
        */

        // Passing to another collection
        evenList = list.stream().filter(i -> i % 2 == 0).collect(Collectors.toList());

        // Directly printing
        list.stream().filter(i -> i % 2 == 0).forEach(i -> System.out.print(i + "  "));

        // ALTERNATIVE Since `System.out` is static method
        list.stream().filter(i -> i % 2 == 0).forEach(System.out::print);

    }
}
```

<br>

# 
---
- 