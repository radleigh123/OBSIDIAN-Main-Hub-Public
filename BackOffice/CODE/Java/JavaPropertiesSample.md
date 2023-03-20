---
cssclass:
aliases:
tags:
- Java
- Java/java.io
- Java/java.util
- Java/Properties
- Java/FileReader
---
**[[JavaProperties|BACK]]**

---
>[!aside|show-title right]+ RESULT:
> Username: keanekiller
> Password: Lhlanders123

```properties
# info.properties
username = keanekiller
password = Lhlanders123
```
```java
/**
 * Proto.java
 */
import java.util.*;
import java.io.*;

class Proto {
    public static void main(String[] args) throws IOException {

        // Create a reader object on the properties file
        FileReader reader = new FileReader("info.properties");

        Properties p = new Properties();

        // Add a wrapper around reader object
        p.load(reader);

        // Access properties data
        System.out.println("Username: " + p.getProperty("username"));
        System.out.println("Password: " + p.getProperty("password"));

    }

}
```