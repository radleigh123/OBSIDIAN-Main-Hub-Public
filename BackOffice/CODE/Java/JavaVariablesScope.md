---
cssclass:
aliases:
tags:
- Java
- Java/Lecture
---
**[[UpdateJava|HOME [Java]]]**

---
## Variables Scope
If you declare a [[JavaVariables|variable]] inside any [[JavaMethod|method]], the variable has a local scope. When the method completes its execution, all local variables are automatically removed from memory by Java’s *<u>garbage collector</u>*.

>[!NOTE|ttl-c c-green alt-co] If variable is declared with a **[[Javastatic|static qualifier]]**, it's shared by all [[JavaClass&Object|instances]] of the class

If a variable has to be accessible from more than one class method, declare it on a class level. As a result, this variable is "*alive*", they can be shared and reused by all methods within the class and, they can even be visible from external classes, e.g:
```java
public class Proto {

    static int num1 = 15;

    public static void main(String[] args) {
        System.out.println(num1 + 5); // 20
    }
}
```