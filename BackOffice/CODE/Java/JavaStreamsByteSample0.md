---
cssclass:
aliases:
tags:
- Java
- Java/Streams/Byte
---
**[[JavaByteStreams|BACK]]**

---
>[!INFO|alt-co no-i clean ttl-c] RESULT:
> ```
> # destination.txt
> 101000010001111111
> ```

```java
/**
 * Main.java
 */
import java.io.*;

public class Main {
    public static void main(String[] args) throws IOException {
        FileInputStream sourceStream = null;
        FileOutputStream targetStream = null;

        try {
            sourceStream = new FileInputStream("source.txt");
            targetStream = new FileOutputStream("destination.txt");

            // Reading source file using read method
            // and write to file byte by byte using write method
            int temp;
            while ((temp = sourceStream.read()) != -1) {
                targetStream.write((byte) temp);
            }
        } finally {
            if (sourceStream != null) {
                sourceStream.close();
            }
            if (targetStream != null) {
                targetStream.close();
            }
        }
    }
}
```
```
# source.txt
101000010001111111
```