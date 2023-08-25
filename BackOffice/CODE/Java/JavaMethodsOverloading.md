---
aliases:
tags:
- Java\
- Java/Methods/Overloading
---
**[[JavaMethod|BACK]]**

---
## Method Overloading
having a class with more than one method having <mark class="hltr-lightgreen">the same name but different argument lists</mark>. A method can be overloaded not only in the same class but in a descendant too.

**e.g.**
>[!aside|show-title right]+ RESULT:
> int result: 3
> double result: 3.0

```java
public class Main {

  public int add(int a, int b) { return a + b; }
  public double add(double a, double b) { return a + b; }
  
  public static void main(String[] args) {
    Main obj = new Main();
    
    System.out.println("int result: " + obj.add(1, 2));
    System.out.println("double result: " + obj.add(1.0, 2.0));
  }

}
```

>[!FAQ|alt-co]- Why overload methods in classes?
> The function `println()` has been overloaded there to give Java developers the freedom to call “*the same*” method with different types of arguments. In reality they are calling different methods with the same name.
> 
> ![[JavaMethodsOverloading.png|center wm-tl]]

<br>

# 
---
- https://www.w3schools.com/java/java_methods_overloading.asp

<br>

**Similarities in C++:** [[C++functionsoverloading]]