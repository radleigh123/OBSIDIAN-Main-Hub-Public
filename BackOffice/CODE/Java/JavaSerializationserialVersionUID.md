---
cssclass:
aliases:
tags:
- Java
- Java/java.io
- Java/Serialization
- Java/Serializable
- Java/serialVersionUID
---
**[[Java#Java Serialization|HOME [Java]]]**

---
## Class Versioning
During [[JavaSerialization|serialization]], JVM automatically calculates a special value: the **serial version unique ID**, which is based on the properties of the serializable object, the class name, the implemented interfaces, and the signatures of non-private methods.

But if your class explicitly defines and initializes a static final variable called `serialVersionUID`, Java will use your value instead of trying to generate one. For example,
```java
public static final serialVersionUID = 456123;
```

More complex example:
**Serial folder**
```java
import java.io.*;

public class Proto {
    public static void main(String[] args) throws FileNotFoundException, IOException {

        User user = new User();

        user.name = "Keane Radleigh";
        user.password = "Lhlanders";

        FileOutputStream fileOut = new FileOutputStream("UserInfo.ser");
        ObjectOutputStream out = new ObjectOutputStream(fileOut);
        out.writeObject(user);

        out.close();
        fileOut.close();

        System.out.println("Object info is now saved!\n");

        long serialVersionUID = ObjectStreamClass.lookup(user.getClass()).getSerialVersionUID();
        System.out.println(serialVersionUID);

    }
}
```
```java
import java.io.Serializable;

public class User implements Serializable {

    private static final long serialVersionUID = 1;

    String name;
    transient String password;

    public void printHello() {
        System.out.println("Hello " + name);
    }

}
```

**Deserial folder**
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

        long serialVersionUID = ObjectStreamClass.lookup(user.getClass()).getSerialVersionUID();
        System.out.println("\n" + serialVersionUID);

    }
}
```
```java
import java.io.Serializable;

public class User implements Serializable {

    private static final long serialVersionUID = 1;

    String name;
    transient String password;

    public void printHello() {
        System.out.println("Hello " + name);
    }

}
```