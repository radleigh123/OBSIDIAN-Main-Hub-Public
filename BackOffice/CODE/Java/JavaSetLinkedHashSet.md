---
cssclass:
aliases:
tags:
- Java
- Java/Collection/Set/LinkedHashSet
---
**[[UpdateJava#Collections|HOME [Java]]]**

---
## LinkedHashSet class
> **initial capacity**: 16
> **load factor**: 0.75

is a [[JavaHashtableHashMap|HashTable]] and [[JavaLinkedList|LinkedList]] implementation of the [[JavaSet|Set interface]]. It inherits the [[JavaSetHashSet|HashSet class]] and implements the Set interface.

The important points about the LinkedHashSet class are:
$\quad$▪  contains unique elements only like HashSet.
$\quad$▪  provides all optional set operations and permits null elements.
$\quad$▪  is non-synchronized.
$\quad$▪  <mark class="hltr-lightgreen">maintains insertion order</mark>.

>[!WARNING|collapse ttl-c]
> Keeping the insertion order in the LinkedHashset has some additional costs, both in terms of extra memory and extra CPU cycles. Therefore, if it is not required to maintain the insertion order, <u>go for the lighter-weight HashMap or the HashSet instead</u>.

**Example:**
>[!aside|right]-
> Ravi
> Vijay
> Ajay

```java
import java.util.*;

class LinkedHashSet2 {
	public static void main(String args[]) {
		LinkedHashSet<String> al=new LinkedHashSet<String>();
		al.add("Ravi");
		al.add("Vijay");
		al.add("Ravi");
		al.add("Ajay");
		
		Iterator<String> itr=al.iterator();
		
		while(itr.hasNext()) {
			System.out.println(itr.next());
		}
	}
}
```

<br>

# 
---
- [LinkedHashSet in Java with Examples - GeeksforGeeks](https://www.geeksforgeeks.org/linkedhashset-in-java-with-examples/)
- [LinkedHashSet (Java Platform SE 8 ) (oracle.com)](https://docs.oracle.com/javase/8/docs/api/java/util/LinkedHashSet.html)