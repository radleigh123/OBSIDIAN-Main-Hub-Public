---
cssclass:
aliases:
tags:
- Java
- Java/Serialization/transient
---
**[[JavaSerialization|BACK]]**

---
## `transient` keyword
a variables modifier used in [[JavaSerialization|serialization]]. <mark class="hltr-lightgreen">When we mark any variable as _transient,_ then that variable is not serialized</mark>. Since _transient_ fields aren't present in the serialized form of an object, the de-serialization process would use the default values (which are `null` or `0`) for such fields when creating an object out of the serialized form.

The *transient* keyword is useful in a few scenarios:
$\quad$ ▪ We can use it for derived fields
$\quad$ ▪ It is useful for fields that do not represent the state of the object
$\quad$ ▪ We use it for any non-serializable references
$\quad$ ▪ When we want to store sensitive information and don't want to send it through the network

**transient and static**: Since [[Javastatic|static]] fields are not part of state of the object, there is no use/impact of using transient keyword with static variables. However there is no compilation error.

**transient and final**: [[Javafinal|final]] variables are directly serialized by their values, so there is no use/impact of declaring final variable as *transient*. There is no compile-time error though.

>[!INFO|clean collapse no-i ttl-c] RESULT:
> $\quad$ i = 10
> $\quad$ j = 20
> $\quad$ k = 0 
> $\quad$ transtatic = 40
> $\quad$ finstatic = 50

```java
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.ObjectInputStream;
import java.io.ObjectOutputStream;
import java.io.Serializable;

public class Main implements Serializable {
    // normal variables
    int i = 10, j = 20;

    // transient variables
    transient int k = 30;

    // use of `transient` here has no impact
    transient static int transtatic = 40;
    transient final int finstatic = 50;

    public static void main(String[] args) throws IOException, ClassNotFoundException {
        Main input = new Main();

        // Serialization
        FileOutputStream fileOut = new FileOutputStream("source.txt");
        ObjectOutputStream objOut = new ObjectOutputStream(fileOut);
        objOut.writeObject(input);

        // Deserialization
        FileInputStream fileIn = new FileInputStream("source.txt");
        ObjectInputStream objIn = new ObjectInputStream(fileIn);
        Main output = (Main) objIn.readObject();
        System.out.println("i = " + output.i);
        System.out.println("j = " + output.j);
        System.out.println("k = " + output.k);
        System.out.println("transtatic = " + output.transtatic); 
        System.out.println("finstatic = " + output.finstatic);

        objOut.flush();
        objOut.close();
        objIn.close();
        fileOut.close();
        fileIn.close();
    }
}
```

<br>

# 
---
- https://www.baeldung.com/java-transient-keyword
- https://www.geeksforgeeks.org/transient-keyword-java/