---
aliases:
tags:
- Java
- Java/Class/Constructor
- Java/Class/Abstract
- Java/Class/Inheritance
- Java/Class/AccessModifier
---
**[[Java|HOME [Java]]]**

---
## Access Modifiers
1. **Private**: The access level of a private modifier is only within the class. It cannot be accessed from outside the class.
2. **Default**: The access level of a default modifier is only within the package. It cannot be accessed from outside the package. If you do not specify any access level, it will be the default.
3. **Protected**: The access level of a protected modifier is within the package and outside the package through child class. If you do not make the child class, it cannot be accessed from outside the package.
4. **Public**: The access level of a public modifier is everywhere. It can be accessed from within the class, outside the class, within the package and outside the package.

Access level modifiers determine whether other classes can use a particular field or invoke a particular method. There are two levels of access control:
$\quad$ ▪ At the top level—`public`, or _package-private_ (no explicit modifier)
$\quad$ ▪  At the member level—`public`, `private`, `protected`, or _package-private_ (no explicit modifier)

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