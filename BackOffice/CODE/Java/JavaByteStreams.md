---
cssclass:
title: JavaStreamsByte
creation-date: 2023-04-10
aliases:
tags:
- Java
- Java/Streams
---
**[[Java#Working with Streams|HOME [Java]]]**

---
# Byte Streams
Byte streams are used to perform **input** and **output** of **8-bit bytes**. They are used to read bytes from the input stream and write bytes to the output stream. Mostly, they are used to read or write raw binary data.

In Java, the byte streams have a <mark class="hltr-lightgreen">3 phase mechanism</mark>:
$\quad$▪ **Split**- The input data source is split into a stream by a spliterator. Java Spliterator interface is an internal iterator that breaks the stream into smaller parts for traversing over them.
$\quad$▪ **Apply**- The elements in the stream are processed.
$\quad$▪ **Combine**- After the elements are processed, they are again combined together to create a single result.

The ByteStream classes are divided into two types of classes, i.e., InputStream and OutputStream. These classes are abstract and the super classes of all the Input/Output stream classes.
>[!column|collapse ttl-c no-t] ByteStream Classes
>>[!INFO|clean no-i] InputStream
>> ▪ [[JavaFileInputStream|FileInputStream]]
>> ▪ [[JavaBufferedInputStream|BufferedInputStream]]
>
>>[!INFO|clean no-i] OutputStream
>>▪ [[JavaFileOutputStream|FileOutputStream]]
>>▪ [[JavaBufferedOutputStream|BufferedOutputStream]]

<br>

![[JavaStreamsByte.png|center hs-med]]

More examples:
- [[JavaStreamsByteSample0|ByteStream to copy the contents of one file to another]]
- [[JavaStreamsByteSample1|Using FileInputStream to read and print each byte's value]]

<br>

# 
---
- https://www.scaler.com/topics/java/byte-stream-in-java/
- https://www.javatpoint.com/bytestream-classes-in-java
- [Byte Streams (Oracle)](https://docs.oracle.com/javase/tutorial/essential/io/bytestreams.html)