---
aliases:
tags:
- Java
- Java/Lecture
- Java/java.util/Random
---
**[[Java|HOME [Java]]]**

---
## Random class
<center>package: <strong>java.util.Random</strong></center>

```java
import java.util.Random;

public class Proto1 {
    public static void main(String[] args) {
        Random rand = new Random();

        System.out.println(rand.nextInt(6) + 1);
        System.out.println(rand.nextBoolean());
    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/8/docs/api/java/util/Random.html