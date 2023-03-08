---
aliases:
tags:
- Java
- Java/Lecture
- Java/Class/super
- Java/Class/Constructor
- Java/Methods/Overriding
---
**[[Java|HOME [Java]]]**

---
## `super` keyword
is a reference variable which is used to refer immediate parent class object.
**e.g.**
>[!aside|show-title right]+ RESULT:
> Name: Keane
> Age: 21
> Salary: 12.316

```java
class BaseClass {
    int age;
    String name;

    BaseClass(int age, String name) {
        this.age = age;
        this.name = name;
    }

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

class DerivedClass extends BaseClass {
    float salary;

    DerivedClass(int age, String name, float salary) {
        // resuing the parent constructor
        super(age, name);
        this.salary = salary;
    }

    @Override
    void display() {
        super.display(); // invoking parent method
        System.out.println("Salary: " + salary);
    }
}

public class Proto {
    public static void main(String[] args) {
        DerivedClass derived = new DerivedClass(21, "Keane", 12.316f);

        derived.display();
    }
}
```

<br>

# 
---
- https://www.javatpoint.com/super-keyword