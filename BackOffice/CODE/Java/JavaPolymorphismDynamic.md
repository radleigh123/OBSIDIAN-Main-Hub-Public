---
aliases:
tags:
- Java
- Java/Class/Polymorphism/Dynamic
---
**[[Java#Packages, Interfaces, and Encapsulation|HOME [Java]]]**

---
## Dynamic Polymorphism
is a process or mechanism in which a call to an overridden method is to resolve at runtime rather than compile-time.
> a case where an object to be used is unknown, and will be known during runtime

**e.g.**
```java
import java.util.Scanner;

abstract class Animal {
    abstract void speak();
}

class Dog extends Animal {
    @Override
    public void speak() { System.out.println("Dog::speak() called..."); }
}

class Cat extends Animal {
    @Override
    public void speak() { System.out.println("Cat::speak() called..."); }
}

public class Proto {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Animal animal;

        System.out.print("Which animal? [1]-Dog  [2]-Cat:  ");
        int choice = sc.nextInt();
        sc.close();

        if (choice == 1) {
            animal = new Dog();
            animal.speak();
        } else {
            animal = new Cat();
            animal.speak();
        }
    }
}
```

<br>

# 
---
- https://www.javatpoint.com/dynamic-polymorphism-in-java