---
cssclass:
aliases:
tags:
- Java
- Java/java.io
- Java/Serializable
- Java/serialVersionUID
---
**[[JavaSerialization|BACK]]**

---
## `serialVersionUID`
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

<br>

# 
---
- 