---
cssclass:
aliases:
tags:
- Java
- Java/Streams/stream/reduce
---
**[[JavaStreams|BACK]]**

---
## Stream.`reduce()`
```java
T reduce(T identity, BinaryOperator<T> accumulator);
```
The reduce operation takes two arguments:
- **identity**: The identity element is both the initial value of the reduction and the default result if there are no elements in the stream.
- **accumulator**: The accumulator function takes two parameters: a partial result of the reduction. It returns a new partial result. For example, the accumulator function is a lambda expression that adds two `Integer` values and returns an `Integer` value `(a, b) -> a + b`
> The reduction stream operations allow us to produce one single result from a sequence of elements, by repeatedly applying a combining operation to the elements in the sequence.

```java
Integer totalAgeReduce = roster
   .stream()
   .map(Person::getAge)
   .reduce(
       0,
       (a, b) -> a + b);
```

<br>

# 
---
- See also:
	- [[JavaStreamscollect|Stream.collect()]]
	- [Reduction (The Java™ Tutorials > Collections > Aggregate Operations) (oracle.com)](https://docs.oracle.com/javase/tutorial/collections/streams/reduction.html#reduce)
- [Guide to Stream.reduce() | Baeldung](https://www.baeldung.com/java-stream-reduce)
- [Stream.reduce() in Java with examples - GeeksforGeeks](https://www.geeksforgeeks.org/stream-reduce-java-examples/)