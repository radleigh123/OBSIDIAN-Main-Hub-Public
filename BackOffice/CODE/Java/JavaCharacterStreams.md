---
cssclass:
title: JavaStreamsCharacter
creation-date: 2023-04-11
aliases:
tags:
- Java
- Java/Streams/Character
---
**[[Java#Working with Streams|HOME [Java]]]**

---
# Character Streams
The java.io package provides Character Stream classes to overcome the limitations of [[JavaByteStreams|Byte Stream classes]], which can only handle the 8-bit bytes and is not compatible to work directly with the Unicode characters. Character Stream classes are used to work with **16-bit Unicode characters**. They can perform operations on characters, char arrays and Strings.
> are mainly used to read characters from the source and write them to the destination.

```java
import java.io.*;
public class CharacterStreamExample {

   public static void main(String args[]) throws IOException {
      FileReader in = null;
      FileWriter out = null;

       // Reading source file using read method 
        // and write to file using write method
      try {
         in = new FileReader("source.txt");
         out = new FileWriter("destination.txt");
         int c;
         while ((c = in.read()) != -1) {
            out.write(c);
         }
      }
       finally {
         if (in != null) {
            in.close();
         }
         if (out != null) {
            out.close();
         }
      }
   }
}
```
```txt
# source.txt
Hi, we are learning about character stream. 
```
```txt
# destination.txt
Hi, we are learning about character stream. 
```

<br>

# 
---
- https://www.javatpoint.com/characterstream-classes-in-java
- https://www.scaler.com/topics/java/byte-stream-in-java/