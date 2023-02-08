---
title: JavaWrapperClass
creation-date: 2023-02-05
aliases:
tags:
- Java
- Java/Lecture
- Java/WrapperClass/Integer
---
**[[Java|HOME [Java]]]**

---
# Wrapper Class
is a way to wrap a primitive data type with an object-oriented interface, allowing you to work with the primitive data type in a more object-oriented manner.
```java
public class Proto1 {
    public static void main(String[] args) {
	    int num1 = 150;
        Integer j = num1; // autoboxing
        Integer i = Integer.valueOf(num1); // converting Integer explicitly

		Integer num2 = new Integer(154);
		int j = num2; // unboxing
		int i = num2.intValue(); // converting int explicitly
    }
}
```

<br>

# 
---
- https://www.geeksforgeeks.org/wrapper-classes-java/