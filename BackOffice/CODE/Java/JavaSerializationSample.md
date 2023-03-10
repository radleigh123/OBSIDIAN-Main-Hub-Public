---
cssclass:
aliases:
tags:
- Java
- Java/Serialization
- Java/Exceptions/throws
---
**[[JavaSerialization|BACK]]** | [[JavaSerializationSample1|Deserialize]]

---
**Steps to Serialize:**
1. Your object class should implement Serializable interface
2. add import `java.io.Serializable`
3. `FileOutputStream fileOut = new FileOutputStream(file path)`
4. `ObjectOutputStream out = new ObjectOutputStream(fileOut);`
5. `out.writeObject(objectName)`
6. `out.close();` $\,$ `fileOut.close();`

<br>

---
```java
import java.io.*;

public class Proto {
    public static void main(String[] args) throws FileNotFoundException, IOException {

        User user = new User();

        user.name = "Rhiz Caballero";
        user.password = "123";

        FileOutputStream fileOut = new FileOutputStream("UserInfo.ser");
        ObjectOutputStream out = new ObjectOutputStream(fileOut);
        out.writeObject(user);

        out.close();
        fileOut.close();

        System.out.println("Object info saved!");

    }
}
```
```java
/**
* User class
*/

import java.io.Serializable;

public class User implements Serializable {

    String name;
    String password;

    public void printHello() {
        System.out.println("Hello " + name);
    }

}
```