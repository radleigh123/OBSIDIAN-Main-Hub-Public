---
title: JavaWrapperClass
creation-date: 2023-02-05
aliases:
tags:
- Java
- Java/Lecture
- Java/Wrapper
---
**[[Java|HOME [Java]]]**

---
# Wrappers, AutoBoxing, & Unboxing
is a way to wrap a primitive data type with an object-oriented interface, allowing you to work with the primitive data type in a more object-oriented manner.
```java
public class Proto1 {
    public static void main(String[] args) {
	    int num1 = 150;
        Integer j = num1; // autoboxing
        Integer i = Integer.valueOf(num1); // alt... converting Integer explicitly

		Integer num2 = new Integer(154);
		int j = num2; // unboxing
		int i = num2.intValue(); // alt... converting int explicitly
    }
}
```

**autoboxing**
>[!BUG|alt-co]+ Redundant
> ```java
> myNumbers.add(new Integer (416));
> ```

The primitive value of `45` will automatically be wrapped into an instance of the `Integer` class:
```java
ArrayList myNumbers = new ArrayList();
myNumbers.add(45);
```

<br>

**unboxing**
`get(23)` will return the value of 24th element as an `Integer` object, that object will automatically be converted into a primitive:
```java
int lastNumbers = myNumbers.get(23);
```

<br>

# 
---
- https://www.geeksforgeeks.org/wrapper-classes-java/