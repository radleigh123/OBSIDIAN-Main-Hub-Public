---
cssclass:
aliases:
tags:
- Java
- Java/java.util
- Java/LinkedList
- Java/Iterator
---
**[[JavaLinkedList|BACK]]**

---
>[!aside|show-title right]+ RESULT:
> LinkedList: \[Cow, Cat, Dog]
> 
> Accessing linked list elements:
> Cow, Cat, Dog,

```java
import java.util.LinkedList;

class Main {

    public static void main(String[] args) {

        // Creating a linked list
        LinkedList<String> animals = new LinkedList<>();
        animals.add("Cow");
        animals.add("Cat");
        animals.add("Dog");
        System.out.println("LinkedList: " + animals);

        // Using forEach loop
        System.out.println("Accessing linked list elements:");
        for (String animal : animals) {
            System.out.print(animal);
            System.out.print(", ");
        }

    }

}
```