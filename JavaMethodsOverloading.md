---
aliases:
tags:
- Java
- Java/Lecture
- Java/Methods/Overloading
---
**[[JavaMethods|BACK]]**

---
## Overloading Methods
in Java is a feature that allows you to have multiple methods with the same name in the same class, as long as they have different parameters.
**e.g.**
```java
public class Main {
  public int add(int a, int b) { return a + b; }
  public double add(double a, double b) { return a + b; }
  
  public static void main(String[] args) {
    Main obj = new Main();
    
    System.out.println("Int result: " + obj.add(1, 2));
    System.out.println("Double result: " + obj.add(1.0, 2.0));
  }
}
```

<br>

# 
---
- https://www.w3schools.com/java/java_methods_overloading.asp

<br>

**Similarities in C++:** [[C++functionsoverloading]]