---
cssclass:
title: JavaHashtableHashMap
creation-date: 2023-03-19
aliases:
tags:
- Java
- Java/java.util
- Java/Hashtable
- Java/HashMap
- Java/typecasting 
---
**[[UpdateJava#Introduction to Collections|HOME [Java]]]**

---
# `Hashtable` & `HashMap` Classes
The classes `Hashtable` and `HashMap` implement the **[[JavaMapInterfaces|Map]]** interface storing key/value pairs. These classes offer a convenient way of storing and accessing the elements of a collection: by key. You can assign a key to an instance of some Java object and use it as a reference. <mark class="hltr-lightgreen">The collections store objects as key/value pairs</mark>.

##### HashMap
implements the **[[JavaMapInterfaces|Map]]** interface which allows us _to store key and value pair_, where keys should be unique.

If you try to insert the duplicate key, it will replace the element of the corresponding key. It is easy to perform operations using the key index like updation, deletion, etc. *HashMap* class is found in the **java.util** package.
Since **Java 5**, it is denoted as `HashMap<K,V>`,where
$\quad$▪ <mark class="hltr-lightblue">`K` -  stands for key</mark> and;
$\quad$▪ <mark class="hltr-lightblue">`V` -  for value</mark>.
It inherits the `AbstractMap` class and implements the **[[JavaMapInterfaces|Map]]** interface.
- contains values based on the key.
- contains only unique keys.
- may have one null key and multiple null values.
- is non synchronized.
- maintains no order.
- The **initial default capacity** is 16 with a **load factor** of 0.75.

>[!aside|show-title right]- RESULT:
> ```
> [52=Mars, 50=Hello, 51=World]
> [52, 50, 51]
> [Mars, Hello, World]
> 
> Hello
> 
> containsKey(52): true
> containsValue("Mars"): true
> size: 3
> 
> 52: Mars 50: Hello 51: World 
> 52: Mars 50: Hello 51: World 
> 52: Mars 50: Hello 51: World
> ```

```java
import java.util.*;

public class Solution {
    public static void main(String[] args) {
        Map<Integer, String> map = new HashMap<>();

        map.putAll(Map.of(50, "Hello",
                51, "World",
                52, "Mars"));

        System.out.println(map.entrySet()); // same as `map
        System.out.println(map.keySet());
        System.out.println(map.values());

        System.out.println();
        System.out.println(map.get(50));
        System.out.println();

        System.out.println("containsKey(52): " + map.containsKey(52));
        System.out.println("containsValue(\"Mars\"): " + map.containsValue("Mars"));
        System.out.println("size: " + map.size());
        System.out.println();

        for (Map.Entry m : map.entrySet()) {
            System.out.print(m.getKey() + ": " + m.getValue() + " ");
        }

        System.out.println();

        // iterator
        Set s = map.entrySet();
        Iterator it = s.iterator();
        while (it.hasNext()) {
            Map.Entry m = (Map.Entry) it.next(); // typecasting involved
            System.out.print(m.getKey() + ": " + m.getValue() + " ");
        }

        System.out.println();

        // object type
        for (Object m : map.keySet()) {
            System.out.print(m + ": " + map.get(m) + " ");
        }
    }
}
```

More examples:
- [[JavaHashtableHashMapSample|Username and Password using HashMap]]

<br>

---
##### Hashtable (legacy collection class)
implements a `hashtable`, which maps keys to values. It inherits Dictionary class and implements the **[[JavaMapInterfaces|Map]]** interface.
-   A *Hashtable* is an array of a list. Each list is known as a <u>bucket</u>. The position of the bucket is identified by calling the `hashcode()` method.
	- contains values based on the key.
	- contains unique elements.
	- doesn't allow null key or value.
	- is synchronized.
-   The initial default capacity of Hashtable class is 11 whereas loadFactor is 0.75.

>[!aside|show-title right]+ RESULT:
>Key: 102        Value: Minglanilla
>Key: 101        Value: Caballero
>Key: 100        Value: Rhiz
> 
> data: {102=Minglanilla, 101=Caballero, 100=Rhiz}

```java
/**
 * Hashtable example
 */

import java.util.*;

class Main {
    public static void main(String[] args) {
        Hashtable<Integer, String> data = new Hashtable<>();

        data.put(100, "Rhiz");
        data.put(101, "Caballero");
        data.put(102, "Minglanilla");

        for (Map.Entry m : data.entrySet()) {
            System.out.println("Key: " + m.getKey()
                    + "\tValue: " + m.getValue());
        }
    }
}
```

# 
<br>

---
- **Hashtable** - https://www.javatpoint.com/java-hashtable
- **HashMap**
	- [HashMap (Java Platform SE8)(Oracle)](https://docs.oracle.com/javase/8/docs/api/java/util/HashMap.html)
	- [Java HashMap (javatpoint)](https://www.javatpoint.com/java-hashmap)
	- [HashMap (w3schools)](https://www.w3schools.com/java/java_hashmap.asp)