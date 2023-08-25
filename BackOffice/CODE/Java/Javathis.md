---
cssclass:
aliases:
tags:
- Java
- Java/Class/Constructor
- Java/this
---
**[[Java|HOME [Java]]]**

---
## `this` Keyword
used to <mark class="hltr-lightgreen">refer to the current object</mark>, and it can be used to distinguish between instance variables and local variables that have the same name.

```java
class myClass {

    int m_num1;
    String m_name;

    myClass(String m_name, int m_num1) {
        this.m_name = m_name;
        this.m_num1 = m_num1;
    }

}
```
>[!ERROR|atl-co collapse ttl-c] $\ \,$Danger
> $\qquad$If we were to write **m_name$\;$ = $\;$name** instead, it would create a local variable called **m_name** within the constructor, which would shadow the instance variable with the same name. The instance variable would remain uninitialized, and any reference to **m_name** outside of the constructor would refer to the uninitialized instance variable.

<br>

More example:
- [[Javathissample0|Calling an overloaded constructor]]

<br>

# 
---
- [Using the this Keyword](https://docs.oracle.com/javase/tutorial/java/javaOO/thiskey.html)
- https://www.w3schools.com/java/ref_keyword_this.asp