---
title: JavaWrapperClass
creation-date: 2023-02-05
aliases:
tags:
- Java
- Java/WrapperClass
---
**[[Java#Java Basics|HOME [Java]]]**

---
# Wrapper Class
is a way to wrap a primitive data type with an object-oriented interface, allowing you to work with the primitive data type in a more object-oriented manner. All primitive data types have corresponding wrapper classes that contain useful methods dealing with respective data types. The wrapper classes serve two purposes:
1. They contain a number of useful functions for manipulation with their primitive counterparts. For example, the class Integer offers such useful methods as conversion of a String into an `int`, or turning an `int` into a `float`, and etc. The **Integer class** also allows you to set the minimum and maximum values for the number in question.
2. Some Java collections can’t store [[JavaVariables|primitives]] (such as [[JavaArrayListVector|ArrayList]]) and so primitives have to be wrapped into objects e.g.,

**autoboxing**
The primitive value of `416` will automatically be wrapped into an instance of the `Integer` class, e.g.:
>[!column|clean no-t]
>>[!DONE] Efficient
>> ```java
>> ArrayList myNumbers = new ArrayList();
>> 
>> myNumbers.add(416); // autoboxing
>> ```
>
>>[!FAILURE] Redundant
>> ```java
>> ArrayList myNumbers = new ArrayList();
>> 
>> myNumbers.add(new Integer (416));
>> ```

**unboxing**
`get(23)` will return the value of 24th element as an **Integer object**, after that, the object will automatically be converted into a primitive:
```java
int lastNumbers = myNumbers.get(23); //unboxing
```

<br>

More example:
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

<br>

# 
---
- https://www.geeksforgeeks.org/wrapper-classes-java/