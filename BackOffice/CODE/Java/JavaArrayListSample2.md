---
cssclass:
aliases:
tags:
- Java
- Java/ArrayList
- Java/Vector
- Java/Operators/TypeComparison/instanceof
---
**[[JavaArrayListVector|BACK]]**

---
The following code will throw the **IllegalCastException** on the third iteration of the loop:
```java
int totalElem = customers.size(); // number of elements

for (int i=0; i< totalElem;i++) {
	Customer currentCust = (Customer) customers.get(i);
	currentCust.doSomething();
}
```

Avoiding the exception using `instanceof` ^8661b0
>[!aside|show-title right]+ RESULT:
> Keane Radleigh
> Rhiz Caballero
> Fubuki 

```java
import java.awt.DisplayMode;
import java.util.ArrayList;

public class Main {

    String name1;

    Main(String name1) {
        this.name1 = name1;
    }

    public static void main(String[] args) {
        ArrayList customers = new ArrayList(3);

        Main cust1 = new Main("Keane Radleigh");
        Main cust2 = new Main("Rhiz Caballero");
        Main cust3 = new Main("Fubuki");

        customers.add(cust1);
        customers.add(cust2);
        customers.add(cust3);

        int totalElem = customers.size();

		System.out.println(customers.get(2).name1); // print individually

        for (int i = 0; i < totalElem; i++) {
            Object currElement = customers.get(i);
            if (currElement instanceof Main) {
                Main currentCust = (Main) customers.get(i);
                currentCust.display();
            } else {
                System.out.println("Does not exit!");
            }
        }

    }

    void display() {
        System.out.println(name1);
    }

}
```