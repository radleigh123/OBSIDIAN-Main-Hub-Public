---
aliases:
tags:
- Java
- Java/Lecture
- Java/java.io/File
- Java/File
---
**[[JavaFileClass|BACK]]**

---
## Reading the contents in Directory
```java
import java.io.File;

public class Proto {
    public static void main(String[] args) {
        File file = new File("D:\\Users\\For WEBTOON\\PROGRAMMING\\Java\\Proto1");

        File[] files = file.listFiles();

        for (File i : files) {
            System.out.println(i.getName());
        }
    }
}
```

<br>

# 
---
- 