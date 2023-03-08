---
cssclass:
aliases:
tags:
- Java
- Java/Lecture
- Java/this
---
**[[Javathis|BACK]]**

---
```java
class myClass {

    int m_num1;
    String m_name;
    double m_num2;

    myClass(int m_num1, double m_num2, String m_name) {
        this.m_num1 = m_num1;
        this.m_num2 = m_num2;
        this.m_name = m_name;
    }

    myClass(int m_num1, String m_name) {
        this(m_num1, 45.3, m_name);
    }

}
```