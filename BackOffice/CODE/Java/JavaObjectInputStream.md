---
cssclass:
aliases:
tags:
- Java
- Java/Serialization
- Java/Streams/ObjectInputStream
---
**[[JavaSerialization|BACK]]**

---
**Steps to deserialize:**
1. Declare your object (DON'T INSTANTIATE)
2. Your class should implement `Serializable` interface
3. add import `java.io.Serializable;`
4. `FileInputStream fileIn = new FileInputStream(file path);` 
5. `ObjectInputStream in = new ObjectInputStream(fileIn);`
6. `objectName = (className) in.readObject();`
7. `in.close();` $\,$ `fileIn.close();`

<br>

---
```java
import java.io.*;

public class Proto2 {
    public static void main(String[] args) throws FileNotFoundException, ClassNotFoundException, IOException {

        User user = null;
        FileInputStream fileIn = new FileInputStream("D:\\Users\\For WEBTOON\\PROGRAMMING\\Java\\Proto1\\UserInfo.ser");
        ObjectInputStream in = new ObjectInputStream(fileIn);

        user = (User) in.readObject();
        in.close();
        fileIn.close();

        System.out.println("Username: " + user.name);
        System.out.println("Password: " + user.password);
        System.out.println();
        user.printHello();

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

More examples:
- [[JavaObjectInputStreamSample0|More complex use of ObjectInputStream]]