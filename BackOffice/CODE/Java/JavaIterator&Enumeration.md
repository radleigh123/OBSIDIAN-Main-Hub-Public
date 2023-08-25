---
cssclass:
title: JavaEnumeration
creation-date: 2023-03-23
aliases:
tags:
- Java
- Java/java.util
- Java/Iterator
- Java/Enumeration
---
**[[Java#Collections|HOME [Java]]]**

---
# Iterator
is an object that can be used to loop through collections, like [[JavaArrayList|ArrayList]] and [[JavaSet|HashSet]]. It is called an "**iterator**" because "*iterating*" is the technical term for [[JavaFlowControl#^217312|looping]].

Getting an Iterator
>[!aside|show-title right]+ RESULT:
> Volvo

```java
import java.util.*;

public class Proto {
    public static void main(String[] args) {

        ArrayList<String> cars = new ArrayList<String>();
        cars.add("Volvo");
        cars.add("BMW");
        cars.add("Ford");

        // Get the iterator
        Iterator<String> iterator = cars.iterator();

        // Print the first item
        System.out.println(iterator.next());
    }
}
```

<br>

### Enumeration (legacy interface)
>[!WARNING] different to the Java [[Javaenum|enum]] keyword

Creating Enumeration object:
>[!aside|show-title right]+ RESULT:
> January
> February
> March

```java
import java.util.*;

public class Proto {

    public static void main(String[] args) {

        Enumeration months;
        ArrayList<String> names = new ArrayList<>();

        names.add("January");
        names.add("February");
        names.add("March");
        months = Collections.enumeration(names);

        while (months.hasMoreElements()) {
            System.out.println(months.nextElement());
        }

    }

}
```

<br>

# 
---
- **Enumeration** - https://www.geeksforgeeks.org/enumeration-interface-in-java/
	- [Java Enumeration Interface (tutorialspoint)](https://www.tutorialspoint.com/java/java_enumeration_interface.htm)
- [Iterator (Java Platform SE 8)](https://docs.oracle.com/javase/8/docs/api/java/util/Iterator.html)
- [Java Iterator (w3schools)](https://www.w3schools.com/java/java_iterator.asp)