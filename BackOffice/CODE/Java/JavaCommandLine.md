---
cssclass:
- tag-outline
aliases:
tags:
- Java
- Java/Lecture
---
**[[UpdateJava|HOME [Java]]]**

---
## Command-Line Arguments
Java programs are deployed in production and will be started from a command line — usually you get an icon to click that runs a command to start a program, but <mark class="hltr-lightgreen">under the hood the OS executes a command that starts your program</mark>.

Java Commands:
`java -version` - checks Java version

`javac` `FILE_NAME.java` - compiler part of *JDK*
`java` `FILE_NAME` - starts *JVM*, runs the program

<br>

#Java/String #Java/Arrays #Java/WrapperClass 
The method **main**(`String[] args`) of the class receives the data as a [[JavaString|String array]] that I decided to call `args`. This array will be automatically created by JVM, and will be large enough to accommodate all the arguments entered from the command line. This array will be populated as follows:

```java
args[0] = "456";
args[1] = "Random Text";
args[2] = "1.5";
```

Command-line arguments are <mark class="hltr-lightgreen">always being passed to a program as String arrays</mark>. It’s the responsibility of the programmer to convert the data to the appropriate data type ([[JavaWrapperClass|Wrapper class]]). For example,
- [[JavaCommandLineSample0|Passing data from CLI to program]]

<br>

# 
---
- 