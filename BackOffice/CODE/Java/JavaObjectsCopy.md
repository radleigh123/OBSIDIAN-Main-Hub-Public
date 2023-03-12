---
aliases:
tags:
- Java
- Java/Class
- Java/Class/Constructor/Copy
- Java/Class/Constructor/Overloading
---
**[[JavaClass&Object#^1a283e|BACK]]**

---
## Copy of Objects
When we want to copy an object in Java, there are two possibilities that we need to consider, a [[JavaObjectsCopy#^d812ae|shallow copy and a deep copy]].
- [[JavaObjectsCopysample0|Using Assignment operator]]

**Using copy method**
```java
class Person1 {
    Person1(String a, int b) {
        this.name = a;
        this.age = b;
    }

	// overloaded constructor
    Person1(Person1 z) {
        this.copy(z);
    }

    public String getName() { return name; }
	public int getAge() { return age; }

    public void setName(String name) { this.name = name; }
	public void setAge(int age) { this.age = age; }

	// copy method
    public void copy(Person1 z) {
        this.setName(z.getName());
        this.setAge(z.getAge());
    }

    String name;
    int age;
}

public class Proto {
    public static void main(String[] args) {
        Person1 p1 = new Person1("Keane", 21);
        
        // Person1 p2 = new Person1("Rhiz", 20);
        // p1.copy(p2);
        Person1 p2 = new Person1(p1);

        System.out.println(p1);
        System.out.println(p2);
        System.out.println("-----------------");
        System.out.println(p1.getName());
        System.out.println(p1.getAge());
        System.out.println("-----------------");
        System.out.println(p2.getName());
        System.out.println(p2.getAge());
    }
}
```

<br>

# 
---
- [Deep copy of an object](https://www.baeldung.com/java-deep-copy)
	- [Deep copy vs Shallow copy](https://www.baeldung.com/cs/deep-vs-shallow-copy) ^d812ae
- [Clone() method](https://www.geeksforgeeks.org/clone-method-in-java-2/)