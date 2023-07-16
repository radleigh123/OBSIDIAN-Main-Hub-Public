---
cssclass:
aliases:
tags:
- Java
- Java/Streams/Byte/BufferedInputStream
---
**[[JavaBufferedInputStream|BACK]]**

---
>[!INFO|bg-gray no-i collapse ttl-c] RESULT:
> This is a text content

```java
import java.io.*;

public class Main {
    public static void main(String[] args) {
        try {
            FileInputStream myFile = new FileInputStream("source.txt");
            BufferedInputStream buff = new BufferedInputStream(myFile);

            int i;
            while ((i = buff.read()) != -1) {
                System.out.print((char) i);
            }
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
```txt
# source.txt
This is a text content
```