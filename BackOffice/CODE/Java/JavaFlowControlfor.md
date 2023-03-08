---
aliases:
tags:
- Java
- Java/Lecture
- Java/ControlFlow/for
- Java/ControlFlow/for-each
- Java/java.util/ArrayList
- Java/Arrays
---
**[[JavaFlowControl|BACK]]**

---
## The for Statement
```java
for (initialization; termination; increment) {
	statement(s)
}
```
-   The <mark class="hltr-blue">initialization</mark> expression initializes the loop; it's executed once, as the loop begins.
-   When the <mark class="hltr-blue">termination</mark> expression evaluates to **false**, the loop terminates.
-   The <mark class="hltr-blue">increment</mark> expression is invoked after each iteration through the loop; it is perfectly acceptable for this expression to increment _or_ decrement a value.

---
**for-each** loop
- traversing technique to iterate through the elements in an array/collection
- `:` means ***in***, e.g.:
	- "*for each element in array*"

```java
ArrayList<Integer> arr1 = new ArrayList<Integer>();
arr1.add(45);
arr1.add(5);
arr1.add(12);

// for every integer index in arr1
for (int i : arr1) {
	System.out.println(i);
}
```

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/nutsandbolts/for.html