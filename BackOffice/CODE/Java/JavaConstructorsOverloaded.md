---
aliases:
tags:
- Java
- Java/Lecture
- Java/Class/Constructor/Overloading
---
**[[Java|HOME [Java]]]**

---
## Constructors Overloaded
can be defined as the concept of having more than one constructor with different parameters so that every constructor can perform a different task.
**e.g.**
```java
class Proto2 {
    Proto2(int m_num1) {
        System.out.println("Constructor called\n");
        this.m_num1 = m_num1;
    }

    Proto2(int m_num1, double m_num2) { this.m_num1 += m_num1 + (int) m_num2; }

    int m_num1;
}

public class Proto1 {
    public static void main(String[] args) {
        Proto2 proto21 = new Proto2((15 + 5), 14.5);

        System.out.println(proto21.m_num1); // 34
    }
}
```

<br>

# 
---
- https://www.javatpoint.com/constructor-overloading-in-java