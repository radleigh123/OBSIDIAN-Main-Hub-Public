---
cssclass:
aliases:
tags:
- Java
- Java/Streams/Byte
---
**[[JavaStreamsByte|BACK]]**

---
>[!INFO|collapse no-i ttl-c] RESULT:
> 84 104 105 115 32 105 115 32 97 32 116 101 115 116 32 102 105 108 101 -1 
> D:\Users\For WEBTOON\PROGRAMMING\Java\Practice_Project

```java
/**
 * Main.java
 */
import java.io.FileInputStream;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        FileInputStream myFile = null;
        try {
            myFile = new FileInputStream("test.dat");
            boolean eof = false;

            while (!eof) {
                int byteValue = myFile.read();
                System.out.print(byteValue + " ");
                if (byteValue == -1) {
                    eof = true;
                }
            }
        } catch (IOException e) {
            System.out.println("Could not read file: " + e.toString());
        } finally {
            if (myFile != null) {
                try {
                    myFile.close();
                } catch (Exception e1) {
                    e1.printStackTrace();
                }
            }
        }

        System.out.println("\n" + System.getProperty("user.dir"));
    }
}
```
```dat
#test.dat
This is a test file
```