---
cssclass:
aliases:
tags:
- Java
- Java/Streams/Byte/BufferedInputStream
---
**[[JavaStreamsBufferedInputStream|BACK]]**

---
>[!INFO|bg-gray no-i collapse ttl-c] RESULT:
> 84 104 105 115 32 105 115 32 116 104 101 32 116 101 120 116 32 99 111 110 116 101 110 116 -1

```java
import java.io.BufferedInputStream;
import java.io.FileInputStream;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        FileInputStream fStream = null;
        BufferedInputStream buff = null;

        try {
            fStream = new FileInputStream("source.txt");
            buff = new BufferedInputStream(fStream);

            boolean eof = false;

            while (!eof) {
                int byteValue = buff.read();
                System.out.print(byteValue + " ");
                if (byteValue == -1) {
                    eof = true;
                }
            }
        } finally {
            if (fStream != null) {
                try {
                    buff.close();
                    fStream.close();
                } catch (Exception e) {
                    e.printStackTrace();
                }
            }
        }
    }
}
```