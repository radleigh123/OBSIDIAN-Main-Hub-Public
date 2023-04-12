---
cssclass:
aliases:
tags:
- Java
- Java/Streams/Byte
---
**[[JavaStreamsBuffered|BACK]]**

---
## `BufferedInputStream` Class
![[JavaStreamsBufferedInputStream.png|center wsmall]]
is used to read information from the stream. It internally uses the buffer mechanism to make the performance fast.

The important points about *BufferedInputStream* are:
$\quad$▪ When the bytes from the stream are skipped or read, the internal buffer automatically refilled from the contained input stream, many bytes at a time.
$\quad$▪ When a *BufferedInputStream* is created, an internal buffer array is created.

Example
>[!aside|right show-title]+ RESULT:
> Hello World Testing

```java
// Main
import java.io.BufferedInputStream;
import java.io.FileInputStream;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try (FileInputStream fin = new FileInputStream("source.txt");
                BufferedInputStream bin = new BufferedInputStream(fin);) {
            int i;
            while ((i = bin.read()) != -1) {
                System.out.print((char) i);
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```
```txt
Hello World Testing
```

More examples:
- [[JavaStreamsBufferedInputStreamSample0|Basic use of BufferedInputStream]]
- [[JavaStreamsBufferedInputStreamSample1|Using BufferedInputStream to get byte values]]

<br>

# 
---
- https://www.javatpoint.com/java-bufferedinputstream-class
- https://www.programiz.com/java-programming/bufferedinputstream