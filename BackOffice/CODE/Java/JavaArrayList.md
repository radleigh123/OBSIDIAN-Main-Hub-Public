---
cssclass:
aliases:
tags:
- Java
- Java/Arrays
- Java/WrapperClass
- Java/List
- Java/ArrayList
- Java/Collections
- Java/Arrays/Multidimensional
---
**[[JavaArrayListVector|BACK]]**

---
<center>package: <strong>java.util.List</strong></center>
<center>package: <strong>java.util.ArrayList</strong></center>

### `ArrayList`
![[JavaArrayList.png|right]]
a resizable array, store reference data types. The *ArrayList* in Java can have the duplicate elements also. It implements the List interface so we can use all the methods of the List interface here. The *ArrayList* maintains the insertion order internally.
- can contain duplicate elements.
- maintains insertion order.
- is non synchronized.
- allows random access because the array works on an index basis.
- manipulation is a little bit slower than the LinkedList in Java because a lot of shifting needs to occur if any element is removed from the array list.
- primitive types are not allowed. It is required to use the required [[JavaWrapperClass|wrapper class]] in such cases.

Simple program list of foods 
```java
import java.util.*;

public class Proto1 {
    public static void main(String[] args) {
        ArrayList<String> food = new ArrayList<>();
        food.add("Pizza");
        food.add("World");
        food.add("Chicken");

		food.set(0, "sushi"); // replaces "Pizza"
		food.remove(2); // removes "Chicken"

		System.out.println(food);
        for (String i : food) {
            System.out.println(i); // alternative, food.get(i)
        }

		food.clear(); // clears the ArrayList

		Collections.sort(food, Collections.reverseOrder()); // sort in reverse
    }
}
```
>[!EXAMPLE]+ Ways of getting data from the list
> ```java
> List list = new ArrayList(List.of(1, "Python", 1.523, true));
> 		
> // for loop
> for (int i = 0; i < list.size(); i++) {
> 	System.out.print(list.get(i) + " ");
> }
> 		
> System.out.println();
> 		
> // for each loop
> for (Object i : list) {
> 	System.out.print(i + " ");
> }
> 		
> System.out.println();
> 		
> // iterator()
> Iterator it = list.iterator();
> while (it.hasNext()) {
> 	System.out.print(it.next() + " ");
> }
> ```

Program to populate *ArrayList* w/ Objects
```java
ArrayList customers = new ArrayList();

Customers cust1 = new Main("Keane", "Radleigh");
customers.add(cust1);

Customers cust2 = new Main("Rhiz", "Caballero");
customers.add(cust2);

// Responsibility of the programmer to provide proper casting
Customers bestCustomers = (Main) customers.get(0);
```

The method `get()` is used to extract a particular element from `ArrayList`. Because `ArrayList` is <mark class="hltr-lightblue">generic storage for any type of object</mark>, the method `get()` returns elements as **Object** data types.

See more:
- [[JavaArrayListSample0|Converting arrays into ArrayList]]
- [[JavaArrayListSample1|Two-dimensional ArrayList]]
- [[JavaArrayListSample2|ArrayList and instance of]]

<br>

# 
---
- https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html
- [ArrayList in Java (javatpoint)](https://www.javatpoint.com/java-arraylist)
- [ArrayList (w3schools)](https://www.w3schools.com/java/java_arraylist.asp)