---
cssclass:
aliases:
tags:
- Java
---
**[[Java#Collections|HOME [Java]]]**

---
## Comparable Interface
```java
/**
 * Student class
 */

import java.util.*;

class Student implements Comparable<Student> {
    int age;
    String name;

    public Student(int age, String name) {
        this.age = age;
        this.name = name;
    }

    public String toString() {
        return "Student [age=" + age + ", name=" + name + "]";
    }

    @Override
    public int compareTo(Student that) {
        if (this.age > that.age) {
            return 1;
        } else {
            return -1;
        }
    }
}
```

```java
/**
 * Main class
 */

public class Main {
    public static void main(String[] args) {
       List<Student> num = new ArrayList<>();
        num.add(new Student(31, "John"));
        num.add(new Student(16, "Keane"));
        num.add(new Student(25, "Rhiz"));

        Collections.sort(num);

        for (Student s : num) {
            System.out.println(s);
        }
    }
}
```

<br>

# 
---
- [Comparable (Java Platform SE 8 ) (oracle.com)](https://docs.oracle.com/javase/8/docs/api/java/lang/Comparable.html)