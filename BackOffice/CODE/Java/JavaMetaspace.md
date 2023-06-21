---
cssclass:
aliases:
tags:
- Java
- 
---
**[[UpdateJava#Java Memory Management|HOME [Java]]]**

---
## Metaspace
>[!ERROR|bg-gray]- PermGen - (superseded)
> PermGen(Permanent Generation) is a special heap space separated from the main memory heap.
> 
> The JVM keeps track of loaded class metadata in the PermGen. Additionally, the JVM stores all the static content in this memory section. This includes all the static methods, primitive variables, and references to the static objects.

Metaspace is a new memory space – starting from the Java 8 version; **it has replaced the older PermGen memory space**. The most significant difference is how it handles memory allocation.

Specifically, **this native memory region grows automatically by default**.

We also have new flags to tune the memory:
$\quad$▪ _MetaspaceSize_ and _MaxMetaspaceSize –_ we can set the Metaspace upper bounds.
$\quad$▪ _MinMetaspaceFreeRatio –_ is the minimum percentage of class metadata capacity free after garbage collection
$\quad$▪ _MaxMetaspaceFreeRatio_ – is the maximum percentage of class metadata capacity free after a garbage collection to avoid a reduction in the amount of space

Additionally, the garbage collection process also gains some benefits from this change. The garbage collector now automatically triggers the cleaning of the dead classes once the class metadata usage reaches its maximum metaspace size.

Therefore, **with this improvement, JVM reduces the chance to get the _OutOfMemory_ error**.

<br>

# 
---
- [Permgen vs Metaspace in Java | Baeldung](https://www.baeldung.com/java-permgen-metaspace)