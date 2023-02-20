---
aliases:
tags:
- Java
- Java/Lecture
- Java/java.io/FileWriter
- Java/java.io/IOException
- Java/FileWriter
- Java/FileWriter/write
- Java/FileWriter/append
- Java/FileWriter/close
---
**[[JavaFileClass|BACK]]**

---
## FileWriter
class is used to write character-oriented data to a file. It is **character-oriented class** which is used for file handling in java.

**e.g.**
```java
import java.io.FileWriter;
import java.io.IOException;

public class Proto {
    public static void main(String[] args) {
        try {
            FileWriter writer = new FileWriter("hello.txt");

            writer.write("Rose are read\nViolet are blue");
            writer.close();
        } catch (IOException e) {
            System.out.println("File already existed");
            e.printStackTrace();
        }
    }
}
```

<br>

# 
---
- https://www.javatpoint.com/java-filewriter-class