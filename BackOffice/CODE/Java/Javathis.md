---
cssclass:
aliases:
tags:
- Java
- Java/Class/Constructor
- Java/this
---
**[[UpdateJava|HOME [Java]]]**

---
## `this` Keyword
> is is useful when you need to refer to the instance of the class from its method.

**e.g.**
```java
class myClass {

    int m_num1;
    String m_name;

    myClass(int m_num1, String m_name) {
        this.m_num1 = m_num1;
        this.m_name = m_name;
    }

}
```

<br>

More example:
- [[Javathissample0|Calling an overloaded constructor]]

<br>

# 
---
- 