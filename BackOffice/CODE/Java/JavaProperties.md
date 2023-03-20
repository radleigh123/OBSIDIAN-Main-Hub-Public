---
cssclass:
title: JavaProperties
creation-date: 2023-03-19
aliases:
tags:
- Java
- Java/java.util
- Java/Properties
---
**[[UpdateJava#Introduction to Collections|HOME [Java]]]**

---
# `Properties` class
represents a persistent set of properties. The *Properties* can be saved to a stream or loaded from a stream. Each key and its corresponding value in the property list is a string.
$\quad$▪ extends [[JavaHashtableHashMap#Hashtable (legacy collection class)|Hashtable]]
$\quad$▪ used to maintain a list of values in which the key is a string and the value is also a string i.e.; it can be used to store and retrieve string type data from the properties file.
$\quad$▪ can specify other properties list as it’s the default. If a particular key property is not present in the original *Properties* list, the default properties will be searched.
$\quad$▪ *Properties* object does not require external synchronization and [[JavaThreadsMulti|Multiple threads]] can share a single *Properties* object.
$\quad$▪ it can be used to retrieve the properties of the system.

Listing the states and keys using the Iterator:
>[!aside|show-title right]+ RESULT:
> The capital of Cebu City is Cebu.
> The capital of Asturias is Balamban.     
> The capital of Lapulapu City is Lapulapu.
> 
> The capital of Florida is Not found.

```java
import java.util.*;

class Proto {
    public static void main(String[] args) {

        Properties capitals = new Properties();
        Set states;
        String str;

        capitals.put("Cebu City", "Cebu");
        capitals.put("Lapulapu City", "Lapulapu");
        capitals.put("Asturias", "Balamban");

        // Show all states and capitals in hashtable
        states = capitals.keySet(); // get set-view of keys
        Iterator itr = states.iterator();

        while (itr.hasNext()) {
            str = (String) itr.next();
            System.out.println("The capital of " + str + " is "
                    + capitals.getProperty(str) + ".");
        }
        System.out.println();

        // Look for state not in list -- specify default
        str = capitals.getProperty("Florida", "Not found");
        System.out.println("The capital of Florida is " + str + ".");

    }

}
```

More example:
- [[JavaPropertiesSample|Getting information from the properties file]]
- [[JavaPropertiesSample1|Creating the properties file]]

<br>

# 
---
- **[Properties (Java Platform SE 7) (Oracle)](https://docs.oracle.com/javase/7/docs/api/java/util/Properties.html)**
- [Java - The Properties Class (tutorialspoint)](https://www.tutorialspoint.com/java/java_properties_class)
- [Properties Class (GeeksforGeeks)](https://www.geeksforgeeks.org/java-util-properties-class-java/)