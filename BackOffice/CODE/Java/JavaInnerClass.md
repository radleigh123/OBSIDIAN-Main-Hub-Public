---
cssclass:
aliases:
tags:
- Java
- Java/Class
- Java/Class/Inner
---
**[[Java#Event Handling in UI|HOME [Java]]]**

---
## Nested Class
> **Terminology:** Nested classes are divided into two categories: non-static and static. Non-static nested classes are called _**inner classes**_. Nested classes that are declared `static` are called _**static nested classes**_.

A class defined inside another class is called *nested class*.
```java
class OuterClass {
	...
	class NestedClass {
		...
	}
}
```

<br>

**Anonymous Inner Class**
If an inner class does not have a name, it’s called *anonymous*.

ex:
```java
this.addWindowListener(new WindowAdapter() {
			public void windowClosing(WindowEvent e) {
				System.exit(0);
			}
		}
);
```

>[!SUCCESS]+ Why use Nested Classes?
> - **It is a way of logically grouping classes that are only used in one place**: If a class is useful to only one other class, then it is logical to embed it in that class and keep the two together. Nesting such "helper classes" makes their package more streamlined.
> - **It increases encapsulation**: Consider two top-level classes, A and B, where B needs access to members of A that would otherwise be declared `private`. By hiding class B within class A, A's members can be declared private and B can access them. In addition, B itself can be hidden from the outside world.
> - **It can lead to more readable and maintainable code**: Nesting small classes within top-level classes places the code closer to where it is used.

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/javaOO/nested.html
- https://www.w3schools.com/java/java_inner_classes.asp