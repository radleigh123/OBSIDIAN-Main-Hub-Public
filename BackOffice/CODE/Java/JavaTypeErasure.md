---
cssclass:
title: JavaTypeErasure
creation-date: 2023-08-12
aliases:
tags:
- Java
- Java/TypeErasure
---
**[[Java#Generics|HOME [Java]]]**

---
# Type Erasure
Generics were introduced to the Java language to provide tighter type checks at compile time and to support generic programming. <mark class="hltr-lightblue">To implement generics, the Java compiler applies type erasure to</mark>:
- Replace all type parameters in generic types with their bounds or `Object` if the type parameters are unbounded. The produced bytecode, therefore, contains only ordinary classes, interfaces, and methods.
- Insert type casts if necessary to preserve type safety.
- Generate bridge methods to preserve polymorphism in extended generic types.

<br>

**Erasure of Generic Types**
During the type erasure process, the Java compiler erases all type parameters and replaces each with its first bound if the type parameter is bounded, or Object if the type parameter is unbounded.
```java
public class Node<T> {
    private T data;
    private Node<T> next;

    public Node(T data, Node<T> next) {
        this.data = data;
        this.next = next;
    }

    public T getData() { return data; }
    // ...
}
```
Because the type parameter `T` is [[JavaWildCardUnbounded|unbounded]], the Java compiler replaces it with `Object`:
```java
public class Node {
    private Object data;
    private Node next;

    public Node(Object data, Node next) {
        this.data = data;
        this.next = next;
    }

    public Object getData() { return data; }
    // ...
}
```

<br>

# 
---
- [Type Erasure (The Java™ Tutorials > Learning the Java Language > Generics (Updated)) (oracle.com)](https://docs.oracle.com/javase/tutorial/java/generics/erasure.html)