---
cssclass:
aliases:
tags:
- Java
- Java/java.io
- Java/java.util
- Java/Properties
- Java/FileWriter
---
**[[JavaProperties|BACK]]**

---
```java
import java.io.*;
import java.util.*;

class Proto {
    public static void main(String[] args) throws IOException {

        Properties p = new Properties();

        // add properties
        p.setProperty("name", "Hershey Chocolate");
        p.setProperty("email", "keaneradleigh123@gmail.com");

        // store properties to a file
        p.store(new FileWriter("info.properties"), "Storing properties example");

        System.out.println("Successfully stored the properties");

    }

}
```
**Result:**
```properties
#Storing properties example
#Mon Mar 20 19:57:15 PST 2023
name=Hershey Chocolate
email=keaneradleigh123@gmail.com

```