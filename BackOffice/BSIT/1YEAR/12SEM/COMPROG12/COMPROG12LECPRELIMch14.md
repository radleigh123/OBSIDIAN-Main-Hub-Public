---
aliases:
tags:
---
**[[COMPROG12LEC|BACK]]**

---
## Features of the Java Programming Language
Java was developed by **SunMicrosystems** as an object-oriented language for general-purpose business applications and for interactive, World Wide Web-based Internet applications. (Sun was later acquired by Oracle Corporation.) Some of the advantages that make Java a popular language are its security features and the fact that it is architecturally neutral: Unlike other languages, you can use Java to write a program that runs on any operating system (such as Windows, Mac OS, or Linux) or device (such as PCs, phones, and tablet computers).

![[COMPROG12LECPRELIMch4image0.png|center wm-sm]]
Java can be run on a wide variety of computers and devices because it does not execute instructions on a computer directly. Instead, Java runs on a hypothetical computer known as the Java Virtual Machine (JVM). When programmers call the JVM hypothetical, they mean it is not a physical entity created from hardware but is composed only of software.

Figure 1-3 shows the Java environment. Programming statements written in a high-level programming language are source code. When you write a Java program, you first construct the source code using a text editor such as Notepad or a development environment and a source code editor such as jGRASP, which you can download from the Web for free. A development environment is a set of tools that help you write programs by providing such features as displaying a language’s keywords in color. The statements are saved in a file; then, the Java compiler converts the source code into a binary program of bytecode. A program called the Java interpreter then checks the bytecode and communicates with the operating system, executing the bytecode instructions line by line within the Java Virtual Machine. Because the Java program is isolated from the operating system, it is also insulated from the particular hardware on which it is run. Because of this insulation, the JVM provides security against intruders accessing your computer’s hardware through the operating system. Therefore, Java is more secure than other languages. Another advantage provided by the JVM means less work for programmers—when using other programming languages, software vendors usually have to produce multiple versions of the same product (a Windows version, Macintosh version, UNIX version, Linux version, and so on) so all users can run the program. With Java, one program version runs on all these platforms. “Write once, run anywhere” (WORA) is the slogan developed by Sun Microsystems to describe the ability of one Java program version to work correctly on multiple platforms.

Java also is simpler to use than many other object-oriented languages. Java is modeled after C++. Although neither language is easy to read or understand on first exposure, Java does eliminate some of the most difficult-to-understand features in C++, such as pointers and multiple inheritance.