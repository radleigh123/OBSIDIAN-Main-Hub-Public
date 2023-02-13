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
```java
class Proto2 {
    int age;
    String name;

    Proto2(int age, String name) {
        this.age = age;
        this.name = name;
    }

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

class Proto3 extends Proto2 {
    float salary;

    Proto3(int age, String name, float salary) {
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

public class Proto1 {
    public static void main(String[] args) {
        Proto3 proto3 = new Proto3(21, "Keane", 12.316f);

        proto3.display();
    }
}
```

<br>

# 
---
- https://www.javatpoint.com/super-keyword