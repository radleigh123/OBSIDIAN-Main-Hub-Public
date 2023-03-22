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
- The initial default capacity of Java HashMap class is 16 with a load factor of 0.75.

>[!aside|show-title right]+ RESULT:
> {Inting=25, Keane=23, Radleigh=24}
> 
> \[Inting, Keane, Radleigh]
> \[25, 23, 24]
> 
> person.get("Keane"): 23
> 
> key = Inting    values: 25
> key = Keane     values: 23
> key = Radleigh  values: 24
> 
> key = Inting    values: 25
> key = Keane     values: 23
> key = Radleigh  values: 24

```java
/**
 * HashMap example
 */

import java.util.HashMap;
import java.util.Map;

class Main {
    public static void main(String[] args) {

        HashMap<String, Integer> person = new HashMap<>();
        person.put("Keane", 23);
        person.put("Radleigh", 24);
        person.put("Inting", 25);

        // print all
        System.out.println(person);

        System.out.println();

        // print all keys
        System.out.println(person.keySet());
        // print all values
        System.out.println(person.values());

        System.out.println();

        // print single value
        System.out.println("person.get(\"Keane\"): " + person.get("Keane"));

        System.out.println();

        // using for-each
        for (String i : person.keySet()) {
            System.out.println("key = " + i
                    + "\tvalues: " + person.get(i));
        }

        System.out.println();

        // using Map
        for (Map.Entry m : person.entrySet()) {
            System.out.println("key = " + m.getKey()
                    + "\tvalues: " + m.getValue());
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