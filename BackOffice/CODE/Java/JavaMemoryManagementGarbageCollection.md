---
cssclass:
aliases:
tags:
- Java
- Java/finalize
---
**[[UpdateJava|HOME [Java]]]**

---
## Garbage Collection Eligibility
> Any object on the heap which cannot be reached through a reference from the stack is "*eligible for garbage collection*".
> ![[JavaMemoryManagementGarbageCollectionImage1.png|wm-tl center]]

Java avoids memory leaks by:
$\quad$▪ Running on a virtual machine
$\quad$▪ Adopts a Garbage Collection strategy

**Soft leaks** - an object is referenced on the stack even though it will never be used again.

>[!FAIL|bg-gray] Finalize <u>(deprecated)</u>
> Correctly using the `finalize()` method
> 
> ![[JavaMemoryManagementGarbageCollectionImage2.png|center wm-tl]]


<br>

# 
---
- [Understanding Memory Leaks in Java | Baeldung](https://www.baeldung.com/java-memory-leaks)