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
is a reference type, similar to a [[JavaClass&Object|class]], that can contain only [[Javafinal#^c164c7|constants]], [[JavaMethod|method signatures]], default methods, [[Javastatic|static]] methods, and nested types.
> a template that can be applied to a class

The interface will not have any implementations — just declarations. (There is an exception: [[JavaInterfaceMarker|Marker interfaces]] don’t even have declarations). When a class declares that it implements a certain interface, it guarantees that it contains implementation for all methods from this interface. And a class can implement more than one interface: just separate their names with commas.
**Every methods declared in the interfaces automatically becomes `public` and `abstract`**, and;
**all fields are by default `public`, `static`, and `final`**.

example:
```java
public interface Prey { public void flee(); }
public interface Predator { public void hunt(); }

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

$\qquad$Some software developers create Java *interfaces* that contain only `final` variables storing important application constants. Implementing such *interfaces* will make these constants available in the class that implements the *interface*(s). Not everyone approves such usage of interfaces, as it can create a messy situation when a class that implements interfaces with static constants exposes a new set of public [[JavaAPI|APIs]] (those final variables) rather than just using these values internally.

More examples:
- [[JavaInterfaceMarker|Marker Interfaces]]

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/IandI/createinterface.html