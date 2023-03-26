---
cssclass:
title: JavaSet
creation-date: 2023-03-22
aliases:
tags:
- Java
- Java/java.util
- Java/Set/HashSet
---
**[[UpdateJava#Introduction to Collections|HOME [Java]]]**

---
# `Set` interface
![[JavaSet.png|center]]

It is an unordered collection of objects in which duplicate values cannot be stored. It is an interface that implements the mathematical set. This [[JavaInterface|interface]] contains the methods inherited from the [[JavaCollectionInterfaces|Collection interface]] and adds a feature that restricts the insertion of the duplicate elements.
&nbsp;
&nbsp;
List of names using `HashSet`:
>[!aside|show-title right]+ RESULT:
> map size: 4
> map contains("Name5"): true      
> map.isEmpty(): false
> 
> map: [Name4, Name5, Name1, Name2]
> 
> map.forEach: Name4Name5Name1Name2
> 
> Name4 Name5 Name1 Name2
> 
> numberList: [1, 2, 1]
> numberSet: [1, 2]

```java
import java.util.*;

public class Proto {

    public static void main(String[] args) {

        // HashSet implements the Set interface
        Set<String> map = new HashSet<>();

        map.add("Name1");
        map.add("Name2");
        map.add("Name3");
        map.add("Name4");
        map.add("Name5");
        map.add("Name2"); // duplicates ignored

        map.remove("Name3");
        System.out.println("map size: " + map.size()); // set size
        System.out.println("map contains(\"Name5\"): " + map.contains("Name5")); // check for matches
        System.out.println("map.isEmpty(): " + map.isEmpty());
        System.out.println();
        System.out.println("map: " + map); // no orders, unlike arrays or list
        System.out.println();

        System.out.print("map.forEach: ");
        map.forEach(System.out::print);

        System.out.println("\n");

        Iterator<String> mapIterator = map.iterator();
        while (mapIterator.hasNext()) {
            System.out.print(mapIterator.next() + " ");
        }

        // Adding an ArrayList to a Set

        System.out.println();

        List<Integer> numberList = new ArrayList<>();
        numberList.add(1);
        numberList.add(2);
        numberList.add(1);

        System.out.println("\nnumberList: " + numberList);

        Set<Integer> numberSet = new HashSet<>(numberList);

        System.out.println("numberSet: " + numberSet);

        map.clear(); // clear all

    }

}
```

<br>

# 
---
- [Set (Java Platform SE7) (Oracle)](https://docs.oracle.com/javase/7/docs/api/java/util/Set.html)
- [Set in Java (GeeksforGeeks)](https://www.geeksforgeeks.org/set-in-java/)
- [Set in Java (javatpoint)](https://www.javatpoint.com/set-in-java)