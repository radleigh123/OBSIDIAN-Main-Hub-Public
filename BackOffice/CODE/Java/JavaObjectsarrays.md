---
aliases:
tags:
- Java
- Java/Class
- Java/Arrays
---
**[[JavaClass&Object|BACK]]**

---
## Array of Objects
stores an array of [[JavaClass&Object|objects]]. Unlike the traditional array stores values like [[JavaString|String]], `integer`, `Boolean`, etc an *Array of Objects* stores objects that mean objects are stored as elements of an array. 
> Note that when we say Array of Objects it is not the object itself that is stored in the array but the reference of the object.

example:
>[!aside|show-title right]+ RESULT:
> Name: Rhiz      Age: 20
> Name: Caballero Age: 22
> Name: Keane     Age: 25

```java
public class Main {
    public static void main(String[] args) {
        myClass[] myclass = new myClass[3];

        myclass[0] = new myClass("Rhiz", 20);
        myclass[1] = new myClass("Caballero", 22);
        myclass[2] = new myClass("Keane", 25);

        for (myClass i : myclass) {
            i.printInfo();
        }
    }
}
```
```java
/**
* myClass.java
*/

public class myClass {
    private String name;
    private int age;

    myClass(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void printInfo() { System.out.println("Name: " + name + "\tAge: " + age); }
}
```

<br>

# 
---
- https://www.geeksforgeeks.org/how-to-create-array-of-objects-in-java/
- https://www.softwaretestinghelp.com/array-of-objects-in-java/