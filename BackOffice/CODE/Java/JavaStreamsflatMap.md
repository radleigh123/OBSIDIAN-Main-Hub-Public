---
cssclass:
aliases:
tags:
- Java
- Java/Streams/stream/flatMap
---
**[[JavaStreams|BACK]]**

---
## Stream.`flatMap` Method
**Stream flatMap(Function mapper)** returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element.
```
<R> Stream<R> flatMap(Function<? super T, ? extends Stream<? extends R>> mapper);

where, R is the element type of the new stream. Stream is an interface and T is the type 
of stream elements. mapper is a stateless function which is applied to each element and 
the function returns the new stream.
```

**For example**
>[!aside|right]-
> ```
> 10 20 30 40 50 60
> ```

```java
List<Integer> flatList1 = Arrays.asList(1, 2);
List<Integer> flatList2 = Arrays.asList(3, 4);
List<Integer> flatList3 = Arrays.asList(5, 6);

List<List<Integer>> list = Arrays.asList(flatList1, flatList2, flatList3);
list.stream()
		.flatMap(Collection::stream) // l -> l.stream()
		.map(l -> l * 10)
		.forEach(l -> System.out.print(l + " "));
```

<br>

# 
---
- See also:
	- [[JavaStreamsmap|Stream.map Method]]
- [Stream flatMap() in Java with examples - GeeksforGeeks](https://www.geeksforgeeks.org/stream-flatmap-java-examples/)
- [The Difference Between map() and flatMap() | Baeldung](https://www.baeldung.com/java-difference-map-and-flatmap)