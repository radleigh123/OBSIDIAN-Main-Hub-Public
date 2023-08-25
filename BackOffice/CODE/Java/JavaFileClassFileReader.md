---
aliases:
tags:
- Java
- Java/java.io/FileReader
- Java/java.io/FileNotFoundException
- Java/java.io/IOException
- Java/FileReader
- Java/FileReader/read
- Java/FileReader/close
---
**[[JavaFileClass|BACK]]**

---
## FileReader
> reads the contents of a file as a stream of characters. One by one `read()` returns an `int` value which contains the byte value when `read()` returns <u>**-1** there is no more data to be read</u>

class is used to read data from the file. It returns data in byte format like `FileInputStream` class. It is **character-oriented class** which is used for file handling in java.

**e.g.**
```java
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.IOException;

public class Proto {
    public static void main(String[] args) {
        try {
            FileReader reader = new FileReader("hello.txt");
            int data = reader.read();

            while (!(data < 0)) {
                System.out.print((char) data);
                data = reader.read();
            }
            reader.close();
        } catch (FileNotFoundException e) {
            System.out.println("File not Found");
            e.printStackTrace();
        } catch (IOException e) {
            System.out.println("Something went wrong writing the file");
            e.printStackTrace();
        }
    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/8/docs/api/java/io/FileReader.html
- https://www.javatpoint.com/java-filereader-class