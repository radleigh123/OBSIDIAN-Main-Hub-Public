---
cssclass:
aliases:
tags:
- Java
- 
---
**[[Java#Collections|HOME [Java]]]**

---
## Comparator Interface
What if you want to sort some objects in an order other than their natural ordering? Or what if you want to sort some objects that don't implement `Comparable`? To do either of these things, you'll need to provide a `Comparator` — an object that encapsulates an ordering. Like the `Comparable` interface, the `Comparator` interface consists of a single method.
>[!aside|right]-
> ```
> [93, 33, 15, 67]
> ```

```java
import java.util.*;

public class Solution {
    public static void main(String[] args) {
        Comparator<Integer> com = new Comparator<>() {
            @Override
            public int compare(Integer i, Integer j) {
                if (i % 10 > j % 10) {
                    return 1;
                } else {
                    return -1;
                }
            }
        };

        List<Integer> num = new ArrayList<>();
        num.addAll(List.of(15, 67, 33, 93));

        Collections.sort(num, com);

        System.out.println(num);
    }
}
```

>[!DONE] ALTERNATIVES
> Using lambda expressions
> ```java
> Comparator<Student> com = (Student i, Student j) -> {
> 	return i.age > j.age ? 1 : -1;
> };
> ```
> &nbsp;
> One line lambda expression
> ```java
> Comparator<Student> com = (i, j) -> i.age > j.age ? 1 : -1;
> ```

<br>

# 
---
- [Comparator (Java Platform SE 8 ) (oracle.com)](https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html)