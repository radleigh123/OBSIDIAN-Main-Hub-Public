---
cssclass:
aliases:
tags:
- Java
- Java/Generics
- Java/Class
- Java/ArrayList
---
**[[UpdateJava#Generics|HOME [Java]]]**

---
## Generic Classes
> Not only Java methods can have parameters, but classes can have them as well.

Example: Using generics in the collection (<mark class="hltr-lightred">COMPILER ERROR</mark>)
```java
import java.util.ArrayList;

public class TestGenericCollection {

	public static void main(String[] args) {

		ArrayList<Customer> customers = new ArrayList<Customer>();
		Customer cust1 = new Customer(“David”,”Lee”);
		customers.add(cust1);
		
		Customer cust2 = new Customer(“Ringo”,”Starr”);
		customers.add(cust2);
		
		Order ord1= new Order();
		customers.add(ord1); // Compiler error
	}

}
```

Getting an error during compilation is better than getting run-time cast exceptions. What makes the [[JavaArrayList|ArrayList]] class capable of rejecting the unwanted data types? <mark class="hltr-lightblue">Open the source code of the ArrayList itself</mark> (pressing **F12** in VScode shows the source code of any [[JavaClass&Object|class]] or [[JavaInterface|interface]], if available). It starts as follows:
```java
public class ArrayList<E> extends AbstractList<E>
        implements List<E>, RandomAccess, Cloneable, java.io.Serializable {
    ...
}
```

<br>

This magic `<E>` after the class name tells the Java compiler that some types of elements will be stored in this class, but which ones will remain unknown until a concrete instance of [[JavaArrayList|ArrayList]] is created. In the example above the **type parameter** `<Customer>` replaces `<E>`, and from now on the collection `customers` will accept only instances of `Customer` objects.

I’d like to stress that this `<E>` notation is used only during the declaration of the type. The code above does not include `<E>`. The compiler replaces `<E>` with `Customer` and erases the parameterized data type. This process is known as **type erasure** — it’s done for compatibility with code written in older versions of Java that didn’t have generics.

Now the code from [[JavaArrayListSample2|ArrayList Sample 2]] can be simplified by removing casting (see code below). Why? Because with *generics*, when the compiler sees a specific type, it automatically generates the *bytecode*, which performs casting internally! That’s why you don’t even need to cast the data returned by the method `get(i)` from `Object` to `Customer` any longer. Besides, you’re guaranteed that the collection `customers` will have only `Customer` instances.

>[!aside|right bg-c-green]+
> **brev·i·ty**
> *(noun)* concise and exact use of words in writing or speech.

Example: Iterating through customers w/out casting
```java
ArrayList<Customer> customers = new ArrayList<Customer>();

// The code to populate customers is omited for brevity
// Iterate through the list customers and do something with each element of this collection. No casting required.

for (Customer c: customers) {
	c.doSomething();
}
```

More examples:
- [[JavaGenericsTypessample|Basic sample of generic classes]]
- [[JavaGenericsTypessample1|Multiple Type Parameters in generic classes]]