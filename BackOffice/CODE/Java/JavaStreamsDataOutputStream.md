---
cssclass:
aliases:
tags:
- Java
- Java/Streams/DataOutputStream
---
**[[JavaStreamsData|BACK]]**

---
## `DataOutputStream` Class
class allows an application to write primitive Java data types to the output stream in a machine-independent way.
> Java application generally uses the data output stream to write data that can later be read by a [[JavaStreamsDataInputStream|data input stream]].

Example: Writing the data to the file *target.txt* file.
>[!INFO|clean no-i ttl-c collapse alt-co] RESULT:
> Sucess

```java
import java.io.*;

/**
 * Main
 */
public class Main {
    public static void main(String[] args) throws IOException {
        FileOutputStream myFile = new FileOutputStream("target.txt");
        DataOutputStream data = new DataOutputStream(myFile);

        data.writeInt(65);
        data.flush();
        data.close();

        System.out.println("Success");
    }
}
```
```txt
# target
A
```

<br>

# 
---
- https://www.javatpoint.com/java-dataoutputstream-class