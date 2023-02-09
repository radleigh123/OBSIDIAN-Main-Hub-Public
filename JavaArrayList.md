---
aliases:
tags:
- Java
- Java/Lecture
- Java/Arrays
- Java/WrapperClass
- Java/java.util/List
- Java/java.util/Arrays
- Java/java.util/ArrayList
- Java/java.util/Collections
- Java/Arrays/Multidimensional
---
**[[Java|HOME [Java]]]**

---
<center>package: <strong>java.util.List</strong></center>
<center>package: <strong>java.util.Arrays</strong></center>
<center>package: <strong>java.util.ArrayList</strong></center>
<center>package: <strong>java.util.Collections</strong></center>

## `ArrayList`
a resizable array, store reference data types. Ways of efficiently initializing ArrayList:
- [[JavaArraysasList|Arrays.asList method]]
- [[JavaCollectionArrays|Collection method]]
- <mark class="hltr-lightgreen">[[JavaListArrays|List method (Java 9 and later) (recommended)]]</mark>

<br>

**e.g.**
```java
import java.util.ArrayList;
import java.util.List;

public class Proto1 {
    public static void main(String[] args) {
        List<String> food = new ArrayList<String>();
        food.add("Pizza");
        food.add("World");
        food.add("Chicken");

		food.set(0, "sushi"); // replaces "Pizza"
		food.remove(2); // removes "Chicken"

		System.out.println(food); // prints all elements
        for (String i : food) {
            System.out.println(i); // alternative, food.get(i)
        }

		food.clear(); // clears the ArrayList
    }
}
```
<br>

## 2D ArrayList
```java
import java.util.ArrayList;

public class Proto1 {
    public static void main(String[] args) {
        ArrayList<ArrayList<String>> newArray = new ArrayList<ArrayList<String>>();

        ArrayList<String> bakeryList = new ArrayList<String>();
        bakeryList.add("Choco");
        bakeryList.add("Cheese");
        bakeryList.add("Ube");
        System.out.println(bakeryList + " " + bakeryList.size());

        ArrayList<String> chickList = new ArrayList<String>();
        chickList.add("Jelailou");
        chickList.add("Mariah");
        System.out.println(chickList + " " + chickList.size());

        newArray.add(bakeryList);
        newArray.add(chickList);

        System.out.println(newArray + " " + newArray.size());
        System.out.println(newArray.get(0).get(2));

        bakeryList.clear();
        chickList.clear();
        newArray.clear();
    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html