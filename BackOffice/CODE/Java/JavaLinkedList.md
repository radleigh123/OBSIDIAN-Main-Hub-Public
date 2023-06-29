---
cssclass:
title: JavaLinkedList
creation-date: 2023-03-24
aliases:
tags:
- Java
- Java/java.util
- Java/List
- Java/LinkedList
- Java/LinkedIterator
---
**[[UpdateJava#Introduction to Collections|HOME [Java]]]**

---
# `LinkedList` class
> Java [[JavaCollectionInterfaces|collection classes]] differ in how you can retrieve and insert objects.

that stores elements so that each contains a reference to the next (aka ***node***). Each element in a **doubly linked list** also contains a reference to the previous element. These features of the doubly-linked class *LinkedList* allow you to create queues (**FIFO**), and stacks (**last-in-first-out** or LIFO). Used if you need to work with a [[sequential]] list of objects and often insert the object into the list.

You can navigate through the list using the class `ListIterator`, which supports going through the list in both directions via its methods `next()` and `previous()`. An example, in which a standby passenger list is created at the boarding gate of some airline company:
>[!aside|show-title right]+ RESULT
> Alex Smith
> Mary Lou
> Sim Monk

```java
import java.util.*;

public class Proto {

    public static void main(String[] args) {

        LinkedList<String> list = new LinkedList<>();
        list.add("Alex Smith");
        list.add("Mary Lou");
        list.add("Sim Monk");

		list.addFirst("Rhiz"); // add in the first node
		list.addLAst("Caballero"); // add in the last node
		
		/*
		 * getFirst() - get first node
		 * getLast() - get last node
		 * 
		 * removeFirst()
		 * removeLast()
		*/

        // Get the list iterator and print every element of the list
        ListIterator iterator = list.listIterator();

        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }

    }

}
```

<br>

More example:
- [[JavaLinkedListSample|Iterating through LinkedList]]

<br>

# 
---
- [Use of java.util.LinkedList (oracle)](https://docs.oracle.com/javase/7/docs/api/java/util/LinkedList.html)
- **[LinkedList vs ArrayList (w3schools)](https://www.w3schools.com/java/java_linkedlist.asp)**
- [LinkList w/ Examples (programiz)](https://www.programiz.com/java-programming/linkedlist)