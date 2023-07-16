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
**Intermediate operations**
[[JavaStreamsmap|map]]: The map method is used to return a stream consisting of the results of applying the given function to the elements of this stream.
```java
List number = Arrays.asList(2,3,4,5);
List square = number.stream().map(x -> x * x).collect(Collectors.toList());
```

[[JavaStreamsfilter|filter]]: The filter method is used to select elements as per the Predicate passed as an argument.
```java
List names = Arrays.asList("Reflection","Collection","Stream");
List result = names.stream().filter(s -> s.startsWith("S")).collect(Collectors.toList());
```

[[JavaStreamssorted|sorted]]: The sorted method is used to sort the stream.
```java
List names = Arrays.asList("Reflection","Collection","Stream");  
List result = names.stream().sorted().collect(Collectors.toList());
```

<br>

**Terminal operations**
`collect`: The collect method is used to return the result of the intermediate operations performed on the stream.
```java
List number = Arrays.asList(2,3,4,5,3);  
Set square = number.stream().map(x -> x * x).collect(Collectors.toSet());
```

`forEach`: The forEach method is used to iterate through every element of the stream.
```java
List number = Arrays.asList(2,3,4,5);
number.stream().map(x -> x * x).forEach(y->System.out.println(y));
```

`reduce`: The reduce method is used to reduce the elements of a stream to a single value. The reduce method takes a [[JavaBinaryOperator|BinaryOperator]] as a parameter.
```java
List number = Arrays.asList(2,3,4,5);
int even = number.stream().filter(x -> x % 2 == 0).reduce(0,(ans,i)-> ans+i);
```

<br>

# 
---
- [Stream (Java Platform SE 8 ) (oracle.com)](https://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html)
- [A Guide to Java Streams in Java 8: In-Depth Tutorial With Examples (stackify.com)](https://stackify.com/streams-guide-java-8/)