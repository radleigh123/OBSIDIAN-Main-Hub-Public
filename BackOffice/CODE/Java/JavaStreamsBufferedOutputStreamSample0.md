---
cssclass:
aliases:
tags:
- Java
- Java/Streams/Byte/BufferedOutputStream
---
**[[JavaStreamsBuffered|BACK]]**

---
### `flush()` Method
To clear the internal buffer, we can use the `flush()` method. This method forces the output stream to write all data present in the buffer to the destination file.

>[!INFO|ttl-c bg-gray collapse no-i] RESULT:
> Data is flushed to the file

```java
import java.io.*;

public class Main {
    public static void main(String[] args) throws IOException {
        String data = "This is a demo of the flush method";

        try {
            FileOutputStream myFile = new FileOutputStream("source.txt");
            BufferedOutputStream buff = new BufferedOutputStream(myFile);

            buff.write(data.getBytes());
            buff.flush();
            System.out.println("Data is flushed to the file");
            buff.close();
        } catch (Exception e) {
            e.getStackTrace();
        }
    }
}
```
```txt
# soure.txt

This is a demo of the flush method
```