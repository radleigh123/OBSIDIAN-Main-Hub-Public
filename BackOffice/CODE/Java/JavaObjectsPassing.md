---
cssclass:
- tag-outline
aliases:
tags:
- Java
- Java/Lecture
- Java/Class
- Java/Methods
- Java/this
---
**[[Java|HOME [Java]]]**

---
## Object Passing
refers to passing objects as arguments to a method or as an element in a collection.

**Passing by Value:**
are passed by value (meaning that an extra copy will be created in memory for each variable). If you create an instance of the class, there will be two copies of `name` and two copies of the variable dependents — one in **main** and the other one in **myClass**.

>[!aside|show-title right]+ RESULT:
> Keane Radleigh

```java
public class Proto {
    public static void main(String[] args) {
        String name = "Keane Radleigh";

        myClass myclass = new myClass(name); // creating a copy in myClass

        System.out.printf("%s", myclass.getName());
    }
}
```

<br>

**Passing by Reference:**
The variable is pointing to an instance of the object **myClass** in memory. In other words, the variable `myclass2` holds the reference (the address in memory) to an object. The code line will not create another copy of the **myClass** object in memory, but will copy its address to the variable `myclass2`.

>[!aside|show-title right]+ RESULT:
> Rhiz Caballero

```java
public class Proto {
    public static void main(String[] args) {
        myClass myclass = new myClass("Keane Radleigh");
        myClass myclass2 = myclass; // passing its reference to an object

		myclass2.setName("Rhiz Caballero");

        System.out.printf("%s", myclass.getName());
    }
}
```

<br>

#Java/GC
> The process of removal of unused objects from memory is called **garbage collection** (**GC**). [[JavaJDK&JRE|JVM]] runs GC automatically.