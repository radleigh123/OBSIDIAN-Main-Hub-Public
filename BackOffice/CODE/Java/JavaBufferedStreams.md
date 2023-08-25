---
cssclass:
aliases:
tags:
- Java
- Java/Streams/Byte
---
**[[Java#Working with Streams|HOME [Java]]]**

---
## Buffered Streams
In `unbuffered I/O`, each read or writes request is handled directly by the underlying OS. This can make a program much less efficient since each such request often triggers <mark class="hltr-lightblue">disk access</mark>, <mark class="hltr-lightblue">network activity</mark>, or some other <mark class="hltr-lightblue">operation</mark> that is <mark class="hltr-lightblue">relatively expensive</mark>.

To reduce this kind of overhead, the Java platform implements *<u>buffered I/O streams</u>*. Buffered input streams read data from a memory area known as a **buffer**; the native input API is called only when the buffer is empty. Similarly, buffered output streams write data to a buffer, and the native output API is called only when the buffer is full.

There are four buffered stream classes used to wrap unbuffered streams:
$\quad$▪ [[JavaBufferedInputStream|BufferedInputStream]]
$\quad$▪ [[JavaBufferedOutputStream|BufferedOutputStream]]
$\quad$▪ [[JavaBufferedReader|BufferedReader]]
$\quad$▪ [[JavaBufferedWriter|BufferedWriter]]