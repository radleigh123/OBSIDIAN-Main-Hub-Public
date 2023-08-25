---
cssclass:
aliases:
tags:
- Java
- 
---
**[[Java#Collections|HOME [Java]]]**

---
## Common methods in the Collection interface
`add(Object o)`
`addAll(Collection c)` - adds all of the elements in the specified `Collection` to the target `Collection`.
`remove(Object o)`
`removeAll(Collection c)` -  removes from the target `Collection` all of its elements that are also contained in the specified `Collection`.
`retainAll(Collection c)` - removes from the target `Collection` all its elements that are _not_ also contained in the specified `Collection`. That is, it retains only those elements in the target `Collection` that are also contained in the specified `Collection`.

`clear()` - removes all elements from the `Collection`.
`isEmpty()`
`size()`
`contains(Object o)`
`containsAll(Collection c)` - returns `true` if the target `Collection` contains all of the elements in the specified `Collection`.

<br>

# 
---
- [The Collection Interface (The Java™ Tutorials > Collections > Interfaces) (oracle.com)](https://docs.oracle.com/javase/tutorial/collections/interfaces/collection.html)