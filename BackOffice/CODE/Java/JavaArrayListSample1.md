---
cssclass:
aliases:
tags:
- Java
- Java/java.util
- Java/ArrayList
---
**[[JavaArrayList|BACK]]**

---
>[!aside|show-title right]+ RESULT:
> \[Choco, Cheese, Ube] 3
> \[Jelailou, Mariah] 2
> \[\[Choco, Cheese, Ube], \[Jelailou, Mariah]] 2
> 
> newArray[0][2]: Ube

```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<ArrayList<String>> newArray = new ArrayList<ArrayList<String>>();

        ArrayList<String> bakeryList = new ArrayList<String>();
        bakeryList.add("Choco");
        bakeryList.add("Cheese");
        bakeryList.add("Ube");
        System.out.println(bakeryList + " " + bakeryList.size());

        ArrayList<String> chickList = new ArrayList<String>();
        chickList.add("Jelailou");
        chickList.add("Mariah");
        System.out.println(chickList + " " + chickList.size());

        newArray.add(bakeryList);
        newArray.add(chickList);

        System.out.println(newArray + " " + newArray.size());
        System.out.println();
        System.out.println("newArray[0][2]: " + newArray.get(0).get(2));

        bakeryList.clear();
        chickList.clear();
        newArray.clear();
    }
}
```