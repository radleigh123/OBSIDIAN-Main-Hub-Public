---
aliases:
tags:
- Java
- Java/java.io/File
- Java/File
---
**[[JavaFileClass|BACK]]**

---
## Creating Files & Directories
**Creating a directory**
```java
import java.io.File;

public class Proto {
    public static void main(String[] args) {
        File file = new File("sampleFile"); // will be created in the same directory

        if (file.mkdir()) {
            System.out.println("Directory created");
        } else {
            System.out.println("Directory not created");
        }
    }
}
```

<br>

**Creating a file**
```java
import java.io.File;
import java.io.IOException;

public class Proto {
    public static void main(String[] args) {
        File file = new File("hello.txt");

        try {
            if (file.createNewFile()) {
                System.out.println("Created file");
            } else {
                System.out.println("File already exists");
            }
        } catch (IOException e) {
            System.out.println("An error occured");
            e.printStackTrace();
        }
    }
}
```