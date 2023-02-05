---
aliases:
tags:
- Java
- Java/Lecture
- Java/Operators/TypeComparison
---
**[[JavaOperators|BACK]]**

---
## Type Comparison Operators
The `instanceof` operator compares an object to a specified type.
You can use it to test if an object is an instance of a class, an instance of a subclass, or an instance of a class that implements a particular interface.
```java
class InstanceofDemo {
    public static void main(String[] args) {

        Parent obj1 = new Parent();
        Parent obj2 = new Child();

        System.out.println("obj1 instanceof Parent: "
            + (obj1 instanceof Parent));
        System.out.println("obj1 instanceof Child: "
            + (obj1 instanceof Child));
        System.out.println("obj1 instanceof MyInterface: "
            + (obj1 instanceof MyInterface));
        System.out.println("obj2 instanceof Parent: "
            + (obj2 instanceof Parent));
        System.out.println("obj2 instanceof Child: "
            + (obj2 instanceof Child));
        System.out.println("obj2 instanceof MyInterface: "
            + (obj2 instanceof MyInterface));
    }
}

class Parent {}
class Child extends Parent implements MyInterface {}
interface MyInterface {}
```
**output:**
```
obj1 instanceof Parent: true
obj1 instanceof Child: false
obj1 instanceof MyInterface: false
obj2 instanceof Parent: true
obj2 instanceof Child: true
obj2 instanceof MyInterface: true
```

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/nutsandbolts/op2.html