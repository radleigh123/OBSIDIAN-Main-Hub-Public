---
aliases:
tags:
- Java
- Java/Exceptions/throws
- Java/java.util/Scanner
- Java/java.io/File
- Java/java.io/FileNotFoundException
---
**[[JavaExceptionHandling|BACK]]**

---
## `throws` keyword
is used to declare exceptions. It specifies that there may occur an exception in the method. It doesn't throw an exception. It is always used with method signature.

**e.g.**
```java
import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

public class Proto {
    static void readFile(String fileName) throws FileNotFoundException {
        File file = new File(fileName);
        Scanner sc = new Scanner(file);
    }

    public static void main(String[] args) {
        String fileName = "myFile.txt";
        try {
            readFile(fileName);
        } catch (FileNotFoundException e) {
            System.out.println("The file " + fileName + " could not be found");
        }
    }
}
```

<br>

# 
---
- https://www.javatpoint.com/throws-keyword-and-difference-between-throw-and-throws