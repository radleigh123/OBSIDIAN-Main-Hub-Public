---
title: JavaFileClass
creation-date: 2023-02-17
aliases:
tags:
- Java
- Java/Lecture
- Java/java.io/File
- Java/File/getPath
- Java/File/getAbsolutePath
- Java/File/isFile
---
**[[Java|HOME [Java]]]**

---
<center><strong>package:</strong> java.io.File</center>

# File Class
Java’s representation of a file or directory pathname. Because file and directory names have different formats on different platforms, a simple string is not adequate to name them.

**e.g.**
```java
import java.io.File;

public class Proto {
    public static void main(String[] args) {
        File file = new File("hello.txt");

        if (file.exists()) {
            System.out.println("File exists");
            System.out.println(file.getPath());
            System.out.println(file.getAbsoluteFile()); // prints detailed path
            System.out.println(file.isFile()); // if Folder, will return false

            file.delete();
        } else {
            System.out.println("The file doesn't exists");
        }
    }
}
```

<br>

---
>[!column|flex no-t]
>>[!INFO|clean no-t collapse]
>>- **[[JavaFileClassCreatingFile|Creating a Directory & File]]**
>>- **[[JavaFileClassReadingFile|Reading the contents of a directory]]**
>
>>[!INFO|clean no-t collapse]
>>- **[[JavaFileClassFileWriter|FileWriter]]**
>>- **[[JavaFileClassFileReader|FileReader]]**

<br>

# 
---
- https://docs.oracle.com/javase/7/docs/api/java/io/File.html
- https://www.geeksforgeeks.org/file-class-in-java/