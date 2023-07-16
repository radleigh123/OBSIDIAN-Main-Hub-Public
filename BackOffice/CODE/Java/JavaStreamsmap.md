---
cssclass:
aliases:
tags:
- Java
- 
---
**[[JavaStreams|BACK]]**

---
## `map()` Operation
>[!aside|right]-
> ```
> [BUS, CAR, BICYCLE, FLIGHT, TRAIN]
> BUS
> CAR
> BICYCLE
> FLIGHT
> ETRAIN
> ```

```java
import java.util.*;
import java.util.stream.*;

public class Solution {
    public static void main(String args[]) {
        List<String> list = Arrays.asList("bus", "car", "bicycle", "flight", "train");
        List<String> list2 = new ArrayList<>();

        list2 = list.stream().map(name -> name.toUpperCase()).collect(Collectors.toList());
        System.out.println(list2);

        list.stream().map(name -> name.toUpperCase()).forEach(System.out::println);
    }
}
```

<br>

# 
---
- 