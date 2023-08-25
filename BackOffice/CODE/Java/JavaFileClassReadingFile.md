---
aliases:
tags:
- Java
- Java/java.io/File
- Java/File
---
**[[JavaFileClass|BACK]]**

---
## Reading the contents in Directory
>[!aside|right show-title]+ RESULT:
> .vscode
> image.png
> Main.java
> target.txt

```java
import java.io.File;

public class Main {
    public static void main(String[] args) {
        File file = new File("D:\\Users\\For WEBTOON\\PROGRAMMING\\Java\\Practice_Project");

        File[] files = file.listFiles();

        for (File i : files) {
            System.out.println(i.getName());
        }
    }
}
```