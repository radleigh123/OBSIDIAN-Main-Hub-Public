---
cssclass:
aliases:
tags:
- Java
- Java/Streams/DataInputStream
---
**[[JavaDataStreams|BACK]]**

---
## `DataInputStream` Class
class allows an application to read primitive data from the input stream in a machine-independent way.
> Java application generally uses the data output stream to write data that can later be read by a data input stream.

Example: Reading the data from the file *test.txt* file.
>[!INFO|clean no-i ttl-c collapse alt-co] RESULT:
> Hello World

```java
/**
 * Main
 */
import java.io.*;

public class Main {
    public static void main(String[] args) throws IOException {
        FileInputStream myFile = new FileInputStream("test.txt");
        DataInputStream inst = new DataInputStream(myFile);

        int count = myFile.available();
        byte[] ary = new byte[count];
        inst.read(ary);
        for (byte bt : ary) {
            char k = (char) bt;
            System.out.print(k);
        }
    }
}
```
```txt
# test
Hello World
```

<br>

# 
---
- https://www.javatpoint.com/java-datainputstream-class