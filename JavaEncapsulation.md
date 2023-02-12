---
aliases:
tags:
- Java
- Java/Lecture
- Java/Class/AccessModifier
- Java/Class/Constructor
- Java/Class/Inheritance
- Java/Class/getter
- Java/Class/setter
---
**[[Java|HOME [Java]]]**

---
## Encapsulation
is a <mark class="hltr-blue">process of wrapping code and data together into a single unit</mark> e.g., a capsule which is mixed of several medicines.
**e.g.**
```java
public class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    String getName() { return name; }
	void setName(String name) { this.name = name; }

    int getAge() { return age; }
    void setAge(int age) { this.age = age; }
}

```

<br>

# 
---
- https://www.javatpoint.com/encapsulation