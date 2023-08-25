---
cssclass:
aliases:
tags:
- Java
---
**[[Java#Java Memory Management|HOME [Java]]]**

---
## Memory Leak
A Memory Leak is a situation <mark class="hltr-lightred">where there are objects present in the heap that are no longer used, but the **[[JavaMemoryManagementIntro#Working of Garbage Collector|GC]]** (garbage collector) is unable to remove them from memory</mark>, and therefore, they're unnecessarily maintained.

There are two different types of objects that reside in Heap memory, **referenced** and **unreferenced**. 
$\quad$▪ Referenced objects are those that still have active references within the application, whereas;
$\quad$▪ unreferenced objects don't have any active references.

![[Pasted image 20230620140331.png|center wm-tl]]

The GC removes unreferenced objects periodically, but it never collects the objects that are still being referenced. This is <mark class="hltr-lightred">where memory leaks can occur</mark>.

<br>

# 
---
- [Understanding Memory Leaks in Java | Baeldung](https://www.baeldung.com/java-memory-leaks)