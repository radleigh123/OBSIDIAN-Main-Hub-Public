---
cssclass:
aliases:
tags:
- Java
- Java/Collection/Set/HashSet
---
**[[UpdateJava#Collections|HOME [Java]]]**

---
## `HashSet` class
HashSet is one of the fundamental data structures in the Java Collections API. Let's recall the most important aspects of this implementation:
- It stores unique elements and permits nulls
- It's backed by a HashMap
- It doesn't maintain insertion order
- It's not thread-safe

Note that this internal HashMap gets initialized when an instance of the HashSet is created:
```java
public HashSet() {
    map = new HashMap<>();
}
```

>[!INFO|ttl-c]
> `List list = new ArrayList;`: By default, 10 places will be created.
> 
> `Set set = new HashSet;`: By default, 16 places will be created. Load factor/fill ratio (**1%** == **0.75**)
> `Set set = new HashSet(100);`: User-defined initialize size to 100, <mark class="hltr-lightblue">load factor still the same</mark>
> `Set set = new HashSet(100, 0.95);`: User-defined initialize size to **100** and load factor to **0.95**

<br>

# 
---
- [A Guide to HashSet in Java | Baeldung](https://www.baeldung.com/java-hashset)