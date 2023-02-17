---
title: JavaInterface
creation-date: 2023-02-16
aliases:
tags:
- Java
- Java/Lecture
- Java/Class
- Java/Interface
---
**[[Java|HOME [Java]]]**

---
# Interface
is a reference type, similar to a class, that can contain _only_ constants, method signatures, default methods, static methods, and nested types.
> a template that can be applied to a class

**e.g.**
```java
class Rabbit implements Prey {
    @Override
    public void flee() {
        System.out.println("Rabbit::flee() called...");
    }
}

class Hawk implements Predator {
    @Override
    public void hunt() {
        System.out.println("Hawk::hunt() called...");
    }
}

// multiple interfaces
class Fish implements Prey, Predator {
    @Override
    public void flee() {
        System.out.println("Fish::flee() called...");
    }

    @Override
    public void hunt() {
        System.out.println("Fish::hunt() called...");
    }
}

public class Proto {
    public static void main(String[] args) {
        Rabbit rabbit = new Rabbit();
        Hawk hawk = new Hawk();
        Fish fish = new Fish();

        rabbit.flee();
        hawk.hunt();
        fish.flee();
        fish.hunt();
    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/IandI/createinterface.html