---
cssclass:
aliases:
tags:
- Java
- Java/Arrays 
- Java/Collections 
---
**[[JavaArrayList|BACK]]**

---
`Arrays.asList()`

>[!ASIDE|right]-
> Dog, Cat, Rat, 
> [Dog, Cat, Rat]

```java
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        String[] name = new String[] { "Dog", "Cat", "Rat" };

        for (String s : name) {
            System.out.print(s + ", ");
        }

        System.out.println();

        List list = new ArrayList<>(Arrays.asList(name)); // pasing the string array
        System.out.println(list);
    }
}
```