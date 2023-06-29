---
aliases:
tags:
- Java
- Java/Lecture
- Java/Arrays
- Java/Vector
- Java/ArrayList
- Java/WrapperClass
---
**[[UpdateJava#Collections|HOME [Java]]]**

---
<center>package: <strong>java.util.Collections</strong></center>

## `ArrayList` & `Vector` Classses
these classes that don’t have this restriction, and you can add more elements to a collection during the run time if needed. Internally both <mark class="hltr-lightblue">collections use the array for storage</mark>, but when you keep adding elements to these collections they internally increase the size of the array (`ArrayList` increases the size by smaller increments), and as elements are deleted these collections shrink.

In both Vector and `ArrayList` you can store only objects — only [[JavaVariables#^3c12e4|primitives]] are allowed. Having said this, keep in mind that Java supports [[JavaWrapperClass|autoboxing]], and if you’ll try to add a primitives to a collection, it’ll be automatically converted into the corresponding wrapper object.
- [[JavaArrayList|ArrayList Class]]
- [[JavaVector|Vector Class]] (deprecated)

<br>

>[!WARNING|ttl-c alt-co]+
> `ArrayList` is a little slower than the array as it needs to do internal array copying to change the collection’s size, and `Vector` is even slower because it supports [[UpdateJava#Digging Deeper into ConCurrent Execution|thread synchronization]]. `Vector` became less popular, after the introduction of more efficient concurrent collections, you can achieve its synchronized functionality by using the method `Collections.synchronizedList()` on an `ArrayList` object.