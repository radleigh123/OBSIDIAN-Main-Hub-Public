---
aliases:
tags:
- Java
- Java/java.util/Random
---
**[[Java#Java Basics|HOME [Java]]]**

---
## Random class
<center>package: <strong>java.util.Random</strong></center>

>[!aside|right]-
> ```
> 2
> 2
> 4
> 3
> 4
> 5
> 6
> 0
> 7
> 8
> ```

```java
import java.util.Random;

public class Raffle {
    public static void main(String[] args) {
        Random ladyLuck = new Random(); // create Random object ladyLuck

        for (int i = 0; i < 10; i++) {
            // Draw and print a random number
            int randomNumber = ladyLuck.nextInt(10);
            System.out.println(randomNumber);
        }
    }
}

/*
Above we create an instance of the Randomclass. It has nextInt method, which gets an integer as a parameter. The method returns a random number between [0, integer[ or 0..(integer -1).
*/
```

<br>

# 
---
- https://docs.oracle.com/javase/8/docs/api/java/util/Random.html