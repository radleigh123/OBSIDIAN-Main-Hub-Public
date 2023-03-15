---
title: JavaPolymorphism
creation-date: 2023-02-17
aliases:
tags:
- Java
- Java/Lecture
- Java/Class/Polymorphism
- Java/LateBinding
---
**[[Java|HOME [Java]]]**

---
# Polymorphism
subclasses of a class can define their own unique behaviors and yet share some of the same functionality of the parent class.
>[!BUG]- Reason for <u>polymorphism</u>
> ```java
> Base base = new Base();
> derivedBase derivedbase = new derivedBase();
> 
> Base[] classes = {base, derivedbase}; // ERROR! only `base` is identified
> derivedBase[] classes = {base, derivedbase}; // ERROR! only `derivedbase` is identified
> ```

**e.g.**
```java
abstract class Base {
    abstract public void go();
}

class derived1 extends Base {
    @Override
    public void go() {
        System.out.println("derived1::go() called...");
    }
}

class derived2 extends Base {
    @Override
    public void go() {
        System.out.println("derived2::go() called...");
    }
}

public class Proto {
    public static void main(String[] args) {
        derived1 d1 = new derived1();
        derived2 d2 = new derived2();

        Base[] classList = { d1, d2 };
        for (Base i : classList) {
            i.go();
        }
    }
}
```

>[!FAQ|ttl-c c-green] run-time binding$\;$ or $\;$late binding
> Note that even though the loop variable `i` is of its ancestor’s type Base, at every iteration it actually points at either **derived1** or a **derived2** instance. The actual object type will be evaluated only during the run time.

See more:
▪$\ \,$[[JavaAbstraction|Abstract]]
▪$\ \,$[[JavaInterface|Interfaces]]

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/IandI/polymorphism.html
- https://www.w3schools.com/java/java_polymorphism.asp#:~:text=Polymorphism%20means%20%22many%20forms%22%2C,methods%20to%20perform%20different%20tasks.