---
cssclass:
title: JavaStreamDiffer
creation-date: 2023-07-01
aliases:
tags:
- Java
- 
---
**[[UpdateJava#Java 8 Streams API|HOME [Java]]]**

---
There are two kinds of streams in Java - I/O streams, and Java 8 streams:

**I/O Streams**: These are sequences of bytes that you can read from (`InputStream` and its subclasses) or write to (`OutputStream` and its subclasses). They’re not very interesting, for three reasons:
1. They’re mostly just <mark class="hltr-lightgreen">Java’s wrapper for file handles</mark>, which function exactly like the corresponding I/O constructs in every other programming language.
2. They’ve been mostly supplanted by Reader and Writer, which do essentially the same thing only with characters rather than bytes. You can have I/O streams of objects, too; they’re basically just `serializers` or `deserializers` on top of output or input streams.
3. The main reason is that they’re passive. The only thing you can do with a stream is read from it or write to it, or if it’s an input stream test to see whether it’s empty.

**Java 8 Streams**: are something new (to Java — they’ve been around for a long time in functional programming languages), and much more interesting. Java 8 streams are basically a generalization of lists: they are sequences of objects; the difference is in how you use them.

<br>

# 
---
- [Java: Difference between Streams and I/O stream explained - Stack Overflow](https://stackoverflow.com/questions/39550670/java-difference-between-streams-and-i-o-stream-explained)
- [What exactly are streams? : learnjava (reddit.com)](https://www.reddit.com/r/learnjava/comments/f3tkwa/what_exactly_are_streams/)