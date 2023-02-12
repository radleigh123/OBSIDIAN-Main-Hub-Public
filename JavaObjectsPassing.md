---
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
**e.g.**
```java
public class Proto1 {
    public static void changeName(Proto2 p) {
        p.setName("Rhiz Caballero");
    }

    public static void main(String[] args) {
        Proto2 proto2 = new Proto2("Keane Radleigh");

        System.out.printf("Before: %s%n", proto2.getName());
        changeName(proto2);
        System.out.println("After: " + proto2.getName());
    }
}

class Proto2 {
    String name;

    // constructor
    public Proto2(String name) {
        this.name = name;
    }

    public String getName() { return name; }
    public void setName(String name) { this.name = name; }
}
```