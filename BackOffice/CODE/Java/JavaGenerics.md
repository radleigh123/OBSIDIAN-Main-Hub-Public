---
cssclass:
title: JavaGenerics
creation-date: 2023-03-10
aliases:
tags:
- Java
- Java/Generics
- Java/WrapperClass
---
**[[Java#Generics|HOME [Java]]]**

---
# Generics
> *Generics* add stability to your code by making more of your bugs detectable at compile time.

- enable types (classes and interfaces) to be parameters when defining: [[JavaClass&Object|classes]], [[JavaInterface|interfaces]], and [[JavaMethod|methods]]
- a benefit is to eliminate the need to create multiple versions of methods or classes for various data types

e.g.
```java
import java.util.ArrayList;

public class Main {
  public static void main(String[] args) {
  
    ArrayList<String> myList = new ArrayList<String>(); // create a new ArrayList that holds strings
    myList.add("hello");
    myList.add("world");
    System.out.println(myList);
    
  }
}

/*
In this example, we're using generics to specify that the ArrayList should hold strings (i.e., `ArrayList<String>`). This ensures that only strings can be added to the list and retrieved from it, which helps to avoid type mismatches and other errors.
*/
```

More examples:
- [[JavaGenericsSample|Efficient Code Using Generics]]
- [[JavaGenericsSample1|Generic Classes]]
	- [[JavaGenericsSample2|Multiple Generics]]
	- [[JavaGenericsSample3|Constraints in Generics]]

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/generics/index.html
	- **[Tutorial: Generics](https://docs.oracle.com/javase/tutorial/extra/generics/index.html)**
- https://www.baeldung.com/java-generics