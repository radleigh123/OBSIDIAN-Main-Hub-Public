---
cssclass:
aliases:
tags:
- Java
- 
---
**[[UpdateJava#Java Memory Management|HOME [Java]]]**

---
## The Stack and the Heap: How Scoping Works
##### Heap Example
```java
public static void main(String[] args) {
	List<Strings> myList = new ArrayList<String>();
	myList.add("One");
	myList.add("Two");
	myList.add("Three");
	printList(myList);
}

public static void printList(List<String> data) {
	System.out.println(data);
}
```

**Line 2:** `List<Strings> myList = new ArrayList<String>();`
![[JavaMemoryManagementStack1.png]]
The `new` keyword simply means:
> *"find some free space on the **heap** large enough to store this object and will reference this new object from the local variable called `myList`"*

<br>

**Line 3:** `myList.add("One");`
**Line 4:** `myList.add("Two");`
**Line 5:** `myList.add("Three");`
![[JavaMemoryManagementStack2.png]]
The lines are adding a `String` to the `List`, in which a `String` is an [[JavaClass&Object|object]] in Java.
> It is the same as: `myList.add(new String("Number"));`

Therefore, Java will create objects on the **heap** of type `String` with values of `One`, `Two`, and `Three`, and will be referenced from within the `List`.

<br>

**Line 6:** `printList(myList);`
**Line 9:** `public static void printList(List<String> data)`
![[JavaMemoryManagementStack3.png]]
A new local variable is created called `data` that points to the same object of `List`
> The `myList` variable is now out of scope.

<br>

**Expanding the `printList` method**
```java
public static void printList(List<String> data) {
	String value = data.get(1);
	data.add("Four");
	System.out.println(value);
}
```

**Line 1:** `String value = data.get(1);`
![[JavaMemoryManagementStack4.png]]
A new reference `value` is created on the **stack**.

<br>

**Line 2:** `data.add("Four");`
![[JavaMemoryManagementStack5.png]]
Creating another object on the **heap**.

<br>

![[JavaMemoryManagementStack6.png]]
Upon reaching the <u>closing bracket</u>, means that the values and variables that were created within the method are going to be removed from the **stack**.
> The `myList` variable is now in-scope. Which is now modified and updated.

