---
cssclass:
title: JavaStreamsData
creation-date: 2023-04-12
aliases:
tags:
- Java
- Java/Streams/Data
---
**[[UpdateJava#Working with Streams|HOME [Java]]]**

---
# Data Streams
To deal with the binary I/O of primitive data type values as well as the String values Java provided the support of Data stream. `DataInput` or the `DataOutput` is the interface which is implemented by all the data streams classes.

![[JavaStreamsData.png|center]]
```java
FileInputStream myFile = new FileInputStream(“myData.dat”);
BufferedInputStream buff = new BufferedInputStream(myFile);
DataInputStream data = new DataInputStream(buff);

try {
	int num1 = data.readInt();
	int num2 = data.readInt();
	float num2 = data.readFloat();
	float num3 = data.readFloat();
	float num4 = data.readFloat();
	double num5 = data.readDouble();
} catch (EOFException eof) {...}
```
In this example `FileInputStream` opens the file *myData.dat* for reading, `BufferedInputStream` makes the read more efficient, and `DataInputStream` extracts from the buffer two integers, three floats, and a double. The assumption here is that the file myData.dat contains exactly these data types and in the specified order.

Such a file could have been created with the help of `DataOutputStream`, which allows you to write primitive Java data types to a stream in a portable way. It has a variety of methods to choose from: `writeInt()`, `writeByte()`, `writeFloat()`, and so on.

- [[JavaStreamsDataInputStream|DataInputStream Class]]
- [[JavaStreamsDataOutputStream|DataOutputStream Class]]

<br>

# 
---
- https://www.roseindia.net/java/example/java/io/iodatastreams.shtml