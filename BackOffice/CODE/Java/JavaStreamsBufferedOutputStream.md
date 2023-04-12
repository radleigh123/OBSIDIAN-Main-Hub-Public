---
cssclass:
aliases:
tags:
- Java
- Java/Streams/Byte/BufferedOutputStream
---
**[[JavaStreamsBuffered|BACK]]**

---
## `BufferedOutputStream` Class
is used for buffering an output stream. It internally uses a buffer to store data. It adds more efficiency than to write data directly into a stream. So, it makes the performance fast.

Example: BufferedOutputStream to write data to a File
```java
import java.io.*;

public class Main {
    public static void main(String[] args) {
        String data = "Rhiz Caballero!";

        try {
            FileOutputStream myFile = new FileOutputStream("source.txt");
            BufferedOutputStream buffOut = new BufferedOutputStream(myFile);

            byte[] array = data.getBytes();

            buffOut.write(array);
            buffOut.close();
        } catch (Exception e) {
            e.getStackTrace();
        }

        System.out.println("Successfully written");
    }
}
```
```txt
# source.txt
Rhiz Caballero!
```

More examples:
- [[JavaStreamsBufferedOutputStreamSample0|Using the flush() Method]]

<br>

# 
---
- https://www.javatpoint.com/java-bufferedoutputstream-class
- https://www.programiz.com/java-programming/bufferedoutputstream