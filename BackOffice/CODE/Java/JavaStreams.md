---
cssclass:
title: JavaStreams
creation-date: 2023-07-06
aliases:
tags:
- Java
- 
---
**[[UpdateJava#Java 8 Stream API|HOME [Java]]]**

---
# Streams API
Simply put, **streams** are wrappers around a data source, allowing us to operate with that data source and making bulk processing convenient and fast. A stream does not store data and, in that sense, is not a data structure. It also never modifies the underlying data source.

This functionality – `java.util.stream` – supports functional-style operations on streams of elements, such as map-reduce transformations on 
collections.

### Different operations on Streams
[[JavaStreamsIntermediate|Intermediate operations]]
[[JavaStreamsmap|map]]: The map method is used to return a stream consisting of the results of applying the given function to the elements of this stream.
```java
List number = Arrays.asList(2,3,4,5);
List square = number.stream()
	.map(x -> x * x)
	.collect(Collectors.toList());
```

[[JavaStreamsfilter|filter]]: The filter method is used to select elements as per the Predicate passed as an argument.
```java
List names = Arrays.asList("Reflection","Collection","Stream");
List result = names.stream()
	.filter(s -> s.startsWith("S"))
	.collect(Collectors.toList());
```

[[JavaStreamssorted|sorted]]: The sorted method is used to sort the stream.
```java
List names = Arrays.asList("Reflection","Collection","Stream");  
List result = names.stream()
	.sorted() // sorted(Comparator.reverseOrder())
	.collect(Collectors.toList());
```

[[JavaStreamsflatMap|flatMap]]: The combination of a map and a flat operation.
```java
List<String> extraList = Arrays.asList("5.6", "7.4", "4", "1", "2.3");
extraList.stream()
	.flatMap(Stream::of) // num -> Stream.of(num)
	.forEach(System.out::println);
```

[[JavaStreamsminmax|min/max]]: By using the [[JavaComparator|Comparator]], returns the minimum/maximum element.
```java
List<Integer> list = Arrays.asList(1, 2, 3, 4, 5, 2, 3);
list.stream()
	.min(Integer::compareTo) // min((i, j) -> i.compareTo(j))
	.ifPresent(i -> System.out.println("min: " + i));
```

<br>

[[JavaStreamsTerminal|Terminal operations]]
[[JavaStreamscollect|collect]]: The collect method is used to return the result of the intermediate operations performed on the stream.
```java
List number = Arrays.asList(2,3,4,5,3);  
Set square = number.stream()
	.map(x -> x * x)
	.collect(Collectors.toSet());
```

`forEach`: The forEach method is used to iterate through every element of the stream.
```java
List number = Arrays.asList(2,3,4,5);
number.stream()
	.map(x -> x * x)
	.forEach(y->System.out.println(y));
```

[[JavaStreamsreduce|reduce]]: The reduce method is used to reduce the elements of a stream to a single value. The reduce method takes a [[JavaBinaryOperator|BinaryOperator]] as a parameter.
```java
List number = Arrays.asList(2,3,4,5);
int even = number.stream()
	.filter(x -> x % 2 == 0)
	.reduce(0,(ans,i)-> ans+i);
```

[[JavaStreamsanyMatch|anyMatch]]: returns `true`, if any elements on the stream match the provided [[JavaLambdaFunctionalInterfacesPredicate|predicate]].
```java
Set<String> fruits = new HashSet<>();
fruits.add("one banana");
fruits.add("one mango");
fruits.add("two apple");

fruits.stream().anyMatch(i -> i.startsWith("two")) // true
```
[[JavaStreamsallMatch|allMatch]]: returns `true`, if all elements on the stream match the provided predicate.
```java
fruits.stream().allMatch(i -> i.startsWith("two")) // false
```
[[JavaStreamsnoneMatch|noneMatch]]: returns `true`, if no elements on the stream match the provided predicate.
```java
fruits.stream().noneMatch(i -> i.startsWith("two")) // false
```
`findAny()`, `findFirst()`: 
```java
List<Integer> list = Arrays.asList(1, 2, 3, 4, 5);

stringList.stream().findAny().get(); // 1
stringList.stream().findFirst().get() // 1
```

<br>

**Concatenating streams:** `concat()`
>[!aside|right]-
> ```
> 1 2 3 4 5 one two three four
> ```

```java
Stream
	.concat(list.stream(), stringList.stream())
	.forEach(i -> System.out.print(i + " "));
```

**Different ways to output the results** *(subject to change)*
>[!aside|right]-
> ```
> 1
> 2
> 3
> 4
> 5
> 
> 1
> 2
> 3
> 4
> 5
> ------------
> 1 2 3 4 5
> 1 2 3 4 5
> ```

```java
List<Integer> list = new ArrayList<>();  
list.addAll(Arrays.asList(1, 2, 3, 4, 5));

// list.stream().forEach(i -> System.out.println(i));  
list.stream().forEach(System.out::println);  
Stream.of(list.toArray()).forEach(System.out::println); // directly streaming  
  
System.out.println("------------");
  
System.out.println(list.stream()
				   .map(Object::toString)  
				   .collect(Collectors.joining(" ")));  
System.out.println(Stream.of(list.toArray())  
				   .map(Object::toString)  
				   .collect(Collectors.joining(" ")));
```

<br>

# 
---
- [Stream (Java Platform SE 8 ) (oracle.com)](https://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html)
- [A Guide to Java Streams in Java 8: In-Depth Tutorial With Examples (stackify.com)](https://stackify.com/streams-guide-java-8/)