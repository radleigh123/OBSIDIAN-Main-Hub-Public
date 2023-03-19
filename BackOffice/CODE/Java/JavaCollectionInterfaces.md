---
cssclass:
aliases:
tags:
- Java
- Java/java.util
- Java/ArrayList
- Java/Collections
- Java/Interface
---
**[[UpdateJava#Introduction to Collections|HOME [Java]]]**

---
## Collection Interfaces
![[JavaCollectionInterfaces.png|center wm-tl]]

A typical collection class implements several [[JavaInterface|interfaces]], which represent a well-designed hierarchy.
> For example, [[JavaArrayListVector|ArrayList]] implements the **List** interface, which extends **Collection**.

Collection extends **[[JavaIterable|Iterable]]**; there are no classes that directly implement this interface. Only its descendent interfaces are implemented. You can use a [[JavaFlowControlfor|for-each loop]] with classes that implement **[[JavaIterable|Iterable]]**.

The **[[JavaList|List]]** interface is defined for the ordered collections: `ArrayList`, `Vector`, and `LinkedList`. It allows duplicate elements. For example, the following code snippet will create two elements in `ArrayList`:
```java
myArrayList.add(“Mary”);
myArrayList.add(“Mary”);
```

<br>

The **[[JavaSet|Set]]** interface is implemented by collections that don’t allow duplicate elements, e.g., `HashSet` and `SortedSet`. For example, the following code snippet will create one element in `HashSet`. The second line will find out that Mary already exists, and won’t change it and will return false:
```java
myHashSet.add(“Mary”);
myHashSet.add(“Mary”);
```

<br>

The **[[JavaMap|Map]]** interface is for storing key/value pairs. A map can’t contain duplicate keys and each key can be mapped to only one value (object). You’ll see some relevant code examples in [[JavaHashtableHashMap|Hashtable and HashMap classes]].

<br>

The **[[JavaQueue|Queue]]** interface is mainly for collections that require **first-in-first-out** (FIFO) operation (so-called priority queues are the exception). Every new element is added to the tail of the queue and the elements are retrieved from the head of the queue. You can restrict the size of the queue if need be. `LinkedList` is one of the classes that implement the *Queue* interface.

**See more:**
The *collection interfaces* are divided into two groups. The most basic interface, `java.util.Collection`, has the following descendants:
$\quad$▪ [[JavaSet|java.util.Set]]
$\quad$▪ [[JavaSortedSet|java.util.SortedSet]]
$\quad$▪ [[JavaNavigableSet|java.util.NavigableSet]]
$\quad$▪ [[JavaQueue|java.util.Queue]]
$\quad$▪ [[JavaBlockingQueue|java.util.concurrent.BlockingQueue]]
$\quad$▪ [[JavaTransferQueue|java.util.concurrent.TransferQueue]]
$\quad$▪ [[JavaDeque|java.util.Deque]]
$\quad$▪ [[JavaBlocingDequeue|java.util.concurrent.BlockingDeque]]

The other collection interfaces are based on `java.util.Map` and are not true collections. However, these interfaces contain *collection-view* operations, which enable them to be manipulated as collections. `Map` has the following offspring:
$\quad$▪ [[JavaSortedMap|java.util.SortedMap]]
$\quad$▪ [[JavaNavigableMap|java.util.NavigableMap]]
$\quad$▪ [[JavaConcurrentMap|java.util.concurrent.ConcurrentMap]]
$\quad$▪ [[JavaConcurrentNavigableMap|java.util.concurrent.ConcurrentNavigableMap]]

<br>

# 
---
- [Collections Framework Overview](https://docs.oracle.com/javase/8/docs/technotes/guides/collections/overview.html)
- [Complete list of Collections in Java](https://www.javatpoint.com/collections-in-java)