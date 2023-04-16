---
cssclass:
aliases:
tags:
- Java
- Java/Streams/ObjectInputStream
---
**[[JavaObjectInputStream|BACK]]**

---
>[!INFO|clean no-i collapse ttl-c] RESULT:
> The Employee object has been deserialized
> &nbsp;
> First Name: John
> Last Name: Smith

```java
/**
 * Deserial
 */

import java.io.FileInputStream;
import java.io.IOException;
import java.io.ObjectInputStream;

public class Deserial {
    public static void main(String[] args) throws ClassNotFoundException {
        Employee bestEmp = null;
        FileInputStream fileIn = null;
        ObjectInputStream objIn = null;

        try {
            fileIn = new FileInputStream("UserInfo.ser");
            objIn = new ObjectInputStream(fileIn);

            bestEmp = (Employee) objIn.readObject();
        } catch (IOException e) {
            try {
                objIn.close();
                fileIn.close();
            } catch (IOException e1) {
                e1.printStackTrace();
            }
        }
        System.out.println("\nThe Employee object has been deserialized\n");
        System.out.println("First Name: " + bestEmp.fName);
        System.out.println("Last Name: " + bestEmp.lName);
        System.out.println("Salary: " + bestEmp.salary);
    }
}
```
```java
/**
 * Employee
 */

class Employee implements java.io.Serializable {
    String fName, lName;
    double salary;

    Employee(String fName, String lName, double salary) {
        this.fName = fName;
        this.lName = lName;
        this.salary = salary;
    }
}
```