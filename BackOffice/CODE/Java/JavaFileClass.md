---
title: JavaFileClass
creation-date: 2023-02-17
aliases:
tags:
- Java
- Java/java.io/File
- Java/File/getPath
- Java/File/getAbsolutePath
- Java/File/isFile
---
**[[Java#I/O Stream|HOME [Java]]]**

---
<center><strong>package:</strong> java.io.File</center>

# File Class
Java’s representation of a file or directory pathname. Because file and directory names have different formats on different platforms, a simple string is not adequate to name them.
- `createNewFile()`: Creates a new, empty file named according to the file name used during the file instantiation. Creates a new file only if a file with this name does not exist.
- `delete()`: Deletes file or directory
- `renameTo()`: Renames a file.
- `length()`: Returns the length of the file in bytes.
- `exists()`: Tests whether the file with the specified name exists.
- `list()`: Returns an array of strings containing file and directory.
- `lastModified()`: Returns the time that the file was last modified.
- `mkDir()`: Creates a directory.

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