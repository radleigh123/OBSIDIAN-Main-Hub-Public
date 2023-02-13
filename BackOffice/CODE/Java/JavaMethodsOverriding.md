---
aliases:
tags:
- Java
- Java/Lecture
- Java/Methods/Overriding
- Java/Class
---
**[[JavaMethods|BACK]]**

---
## Overriding Methods
> when subclass method is marked with the `@Override` annotation, it<mark class="hltr-blue"> tells the compiler to check</mark> it overrides in the <mark class="hltr-blue">superclass</mark>.

is a feature that allows a subclass to provide a different implementation of a method that is already defined in its superclass.
**e.g.**
```java
class Proto2 {
    public void draw() {
        System.out.println("Proto2::draw() called...");
    }
}

class Proto3 extends Proto2 {
	// this method is meant to override a superclass method
    @Override
    public void draw1() { // ERROR! mispelled name
        System.out.println("Proto3::draw() called...");
    }
}

public class Proto1 {
    public static void main(String[] args) {
        Proto2 proto21 = new Proto2();
        Proto2 proto22 = new Proto3();

        proto21.draw(); // Proto2...
        proto22.draw(); // Proto3...
    }
}
```

**More examples**
- [[JavaMethodsOverridingsample0|Bank scenario]]

<br>

# 
---
- https://www.javatpoint.com/method-overriding-in-java