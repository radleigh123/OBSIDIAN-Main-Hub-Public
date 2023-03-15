---
aliases:
tags:
- Java
- Java/Lecture
- Java/Class/Constructor
- Java/Class/Abstract
- Java/Class/Inheritance
- Java/Class/AccessModifier
---
**[[Java|HOME [Java]]]**

---
## Access Modifiers
Access level modifiers determine whether other classes can use a particular field or invoke a particular method. There are two levels of access control:
-   At the top level—`public`, or _package-private_ (no explicit modifier)
-   At the member level—`public`, `private`, `protected`, or _package-private_ (no explicit modifier)

**main**
```java
import package1.*; // or `*` to import all packages

class Asub extends A {
    void displayDefault() {
        System.out.println(defaultMessage);
    }

    void displayProtected() {
        System.out.println(protectedMessage);
    }
}

public class Proto1 {
    public static void main(String[] args) {
        Asub asub = new Asub();

        // default, package-private (ERROR! only within package)
        System.out.println(asub.defaultMessage);

        // public access
        System.out.println(asub.publicMessage);

        // protected access (main() here can't access, not a child class)
        asub.displayProtected();

        // private access (ERROR! only parent class can access)
        System.out.println(a.privateMessage);
    }
}
```
**package1**
```java
package package1;

public class A {
    String defaultMessage = "Default Message";
    public String publicMessage = "Public Message";
    protected String protectedMessage = "Protected Message";
    private String privateMessage = "Private Message";
}

class B extends A {
    String str = defaultMessage;
}
```

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html
- https://www.javatpoint.com/access-modifiers