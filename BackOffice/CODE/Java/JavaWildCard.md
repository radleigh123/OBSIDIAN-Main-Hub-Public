---
cssclass:
title: JavaWildCard
creation-date: 2023-03-13
aliases:
tags:
- Java
- Java/Wildcards
---
**[[UpdateJava#^406387|HOME [Java]]]**

---
# Wildcards
The question mark `?` is known as the *wildcard* in generic programming. It <mark class="hltr-lightgreen">represents an unknown type</mark>.

Generic-type bounding allows us to restrict what types can be used instead of the generic type. This Java feature makes it possible to treat generics polymorphically. For instance, a method that operates on numbers might only want to accept instances of the Number class or its subclasses. This is what bounded type parameters are for.
- [[JavaWildCardUpper|Upper Bounded Wildcards]]: `extends`
- [[JavaWildCardLower|Lower Bounded Wildcards]]: `super`
- [[JavaWildCardUnbounded|Unbounded Wildcards]] 

>[!FAQ]
> **Covariance** - 
> **Contravariance**
> **Invariance**

<br>

# 
---
- [wildcards in java (geeksforgeeks)](https://www.geeksforgeeks.org/wildcards-in-java/)
- [(3) Generics and Wildcards in Java | Part 2 | Invariance vs Covariance vs Contravariance | Geekific - YouTube](https://www.youtube.com/watch?v=FXAUXvPNKi8)
- [java - Covariance, Invariance and Contravariance explained in plain English? - Stack Overflow](https://stackoverflow.com/questions/8481301/covariance-invariance-and-contravariance-explained-in-plain-english)