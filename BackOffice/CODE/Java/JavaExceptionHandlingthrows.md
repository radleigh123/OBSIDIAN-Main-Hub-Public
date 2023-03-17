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
is used to declare exceptions. It specifies that <mark class="hltr-lightgreen">there may occur an exception in the method</mark>. It doesn't throw an exception. It is always used with [[JavaMethod|method signature]].
> In some cases it makes more sense to handle an exception not in the method where it happened, but in the calling one.

Using throws clause sample
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
            System.out.println(e.toString());
            System.out.println("The file " + fileName + " could not be found");
        }
    }
}
```
Result:
>[!INFO|collapse alt-co clean no-t]
> java.io.FileNotFoundException: **myFile.txt** (The system cannot find the file specified)
> The file **myFile.txt** could not be found

<br>

# 
---
- https://www.javatpoint.com/throws-keyword-and-difference-between-throw-and-throws