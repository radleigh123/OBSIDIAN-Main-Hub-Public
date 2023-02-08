---
aliases:
tags:
- Java
- Java/Arrays
- Java/WrapperClass
- Java/java.util/ArrayList/add
- Java/java.util/ArrayList/get
- 
---
**[[Java|HOME [Java]]]**

---
## `ArrayList`
a resizable array, store reference data types
```java
import java.util.ArrayList;

public class Proto1 {
    public static void main(String[] args) {
        ArrayList<String> food = new ArrayList<String>();
        food.add("Pizza");
        food.add("World");
        food.add("Chicken");

		food.set(0, "sushi"); // replaces "Pizza"
		food.remove(2); // removes "Chicken"

        for (String i : food) {
            System.out.println(i); // alternative, food.get(i)
        }

		food.clear(); // clears the ArrayList
    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html