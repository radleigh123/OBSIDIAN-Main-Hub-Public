---
cssclass:
aliases:
tags:
- Java
- Java/typecasting
---
**[[JavaCasting|BACK]]**

---
**TestPayIncrease main**
>[!aside|show-title right]+ RESULT:
> Increasing salary by 30%. Person's name is Rhiz
> Sorry, can't increase hourly rate by more than 20%. Person's name is Person's name is Caballero
> Increasing salary by 30%. Person's name is Johnny

```java
public class TestPayIncrease {
    public static void main(String[] args) {
        Person workers[] = new Person[3];
        workers[0] = new Employee("Rhiz");
        workers[1] = new Contractor("Caballero");
        workers[2] = new Employee("Johnny");

        Employee currentEmployee;
        Contractor currentContractor;

        for (Person p : workers) {
            if (p instanceof Employee) {
                currentEmployee = (Employee) p;
                currentEmployee.increasePay(30);
            } else if (p instanceof Contractor) {
                currentContractor = (Contractor) p;
                currentContractor.increasePay(60);
            }
        }
    }
}
```

**Payable interface**
```java
public interface Payable {
    final int INCREASE_CAP = 20;

    boolean increasePay(int percent);
}
```

**Person base class**
```java
public class Person {
    private String name;

    public Person(String name) {
        this.name = name;
    }

    public String getName() {
        return ("Person's name is " + name);
    }
}
```

**Employee class**
```java
public class Employee extends Person implements Payable {

    String name;

    Employee(String name) {
        super(name);
    }

    @Override
    public boolean increasePay(int percent) {
        System.out.println("Increasing salary by " + percent + "%. " + getName());
        return true;
    }
}
```

**Contractor class**
```java
public class Contractor extends Person implements Payable {

    String name;

    Contractor(String name) {
        super(name);
    }

    @Override
    public boolean increasePay(int percent) {
        if (percent < INCREASE_CAP) {
            System.out.println("Increasing salary by 30%. Person's name is "
                    + name);

            return true;
        } else {
            System.out.println("Sorry, can't increase hourly rate by more than 20%. Person's name is "
                    + getName());

            return false;
        }
    }
}
```