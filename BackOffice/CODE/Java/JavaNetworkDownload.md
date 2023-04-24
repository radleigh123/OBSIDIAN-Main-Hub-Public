---
cssclass:
aliases:
tags:
- Java
- 
---
**[[UpdateJava#Network Programming|HOME [Java]]]**

---
## How to Download Files from the Internet
Combine the class URL with the reading files techniques and you should be able to download practically any unprotected file (such as images, music, and binary files) from the Internet. The trick is in opening the file stream properly. The code below shows the code of a Java class, `FileDownload`, which takes the URL and the destination (local) file name as command-line arguments, connects to this resource, and downloads it into a local file.
```java
import java.io.FileOutputStream;
import java.io.InputStream;
import java.net.URL;
import java.net.URLConnection;

public class Main {
    public static void main(String[] args) {
        if (args.length != 2) {
            System.out.println("Proper Usage: java FileDownload URL OutputFileName");
            System.exit(0);
        }

        InputStream in = null;
        FileOutputStream fOut = null;

        try {
            URL remoteFile = new URL(args[0]);
            URLConnection fileStream = remoteFile.openConnection();

            fOut = new FileOutputStream(args[1]);
            in = fileStream.getInputStream();

            int data;
            while ((data = in.read()) != -1) {
                fOut.write(data);
            }
        } catch (Exception e) {
            e.printStackTrace();
        } finally {
            System.out.println("The file jas been download successfully");

            try {
                in.close();
                fOut.flush();
                fOut.close();
            } catch (Exception e1) {
                e1.printStackTrace();
            }
        }
    }
}
```
Note how this `FileDownload` program starts by checking the number of provided command parameters: If the number is anything but two, the program prints an error message and quits. Here’s an example of how you can run this program to download a W-4 tax form from the Internal Revenue Service website:
```
java FileDownload http://www.irs.gov/pub/irs-pdf/fw4.pdf w4form.pdf
```