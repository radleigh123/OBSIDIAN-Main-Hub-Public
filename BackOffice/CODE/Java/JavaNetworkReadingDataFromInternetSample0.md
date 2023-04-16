---
cssclass:
aliases:
tags:
- Java
---
**[[JavaNetworkReadingDataFromInternet|BACK]]**

---
The program below reads the content of the existing or generated file `index.html` from `google.com` and prints this content on the system console. For you to test this program your computer has to be connected to the Internet. The program may not work properly if your connection goes through a firewall.
```java
import java.net.*;
import java.io.*;

public class Main {
    public static void main(String[] args) {
        String nextLine;
        URL url = null;
        URLConnection urlCon = null;

        InputStreamReader inStream = null;
        BufferedReader buff = null;

        try {
            // index.html is a default URL's file name
            url = new URL("https://www.google.com");
            urlCon = url.openConnection();

            inStream = new InputStreamReader(urlCon.getInputStream(), "UTF8");
            buff = new BufferedReader(inStream);

            // Read and print the lines from index.html
            while (true) {
                nextLine = buff.readLine();

                if (nextLine != null) {
                    System.out.println(nextLine);
                } else {
                    break;
                }
            }
        } catch (MalformedURLException e) {
            System.out.println("Please check the URL: " + e.toString());
        } catch (IOException e1) {
            System.out.println("Can't read from the Internet: " + e1.toString());
        } finally {
            if (inStream != null) {
                try {
                    inStream.close();
                    buff.close();
                } catch (IOException e2) {
                    System.out.println("Can't close the streams: " + e2.getMessage());
                }
            }
        }
    }
}
```

>[!INFO|clean no-i ttl-c] RESULT:
> ```html
> <!doctype html>
> <html itemscope="" itemtype="http://schema.org/WebPage" lang="en-PH">
> 	<head>
> 		<meta content="text/html; charset=UTF-8" http-equiv="Content-Type">
> 		<meta content="/images/branding/googleg/1x/googleg_standard_color_128dp.png" itemprop="image">
> 		
> 		<title>Google</title>
> 		
> 		<script nonce="Hx5UVG7Cde5vArxQO51l5g">
> 			<!-- the rest of the codes -->
> 		</script>
> ```