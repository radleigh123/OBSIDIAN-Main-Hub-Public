---
cssclass:
aliases:
tags:
- Java
- Java/Serialization
- Java/Streams/ObjectOutputStream
---
**[[JavaObjectOutputStream|BACK]]**

---
>[!INFO|clean no-i ttl-c collapse] RESULT:
> The Employee object has been serialized.

```java
/**
 * Main
 */

import java.io.*;

class Main {
    public static void main(String[] args) {
        Employee emp = new Employee("John", "Smith", 50000);

        FileOutputStream fileOut = null;
        ObjectOutputStream objectOut = null;

        try {
            fileOut = new FileOutputStream("UserInfo.ser");
            objectOut = new ObjectOutputStream(fileOut);

            objectOut.writeObject(emp);
        } catch (IOException e) {
            // closing the streams
            try {
                objectOut.flush();
                objectOut.close();
                fileOut.close();
            } catch (IOException e1) {
                e1.printStackTrace();
            }
        }
        System.out.println("The Employee object has been serialized.");
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