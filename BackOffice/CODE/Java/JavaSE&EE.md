---
cssclass:
aliases:
tags:
- Java
- Java/Lecture
- Java/SE
- Java/EE
---
**[[UpdateJava#Introduction|HOME [Java]]]**

---
## Java SE & EE
**Java Standard Edition**
is the widely used object-oriented programming language to develop and operate web-based or system-based applications. It is an eminent programming language used typically to implement several types of applications like the web application, mobile application with iOS & Android and UI oriented applications.
>[!INFO|clean no-i collapse]- Features of Java
> 1\. **Simple**
> ▪$\ \,$Java is an easy language to learn if you know the basic concepts of C/C++.
> ▪$\ \,$Compared to other programming languages, it has simple and easy syntax to understand.
> ▪$\ \,$Unlike other programming languages in which pointers overloading concepts are used, java has removed such features to overcome complexity.
> ▪$\ \,$The automatic Garbage collection feature is available in Java to remove the unused/unreferenced objects that are not available in most programming languages.
> 2\. **Object-Oriented**
> ▪$\ \,$Java is an Object-Oriented Programming Language. So, everything is an Object and can be implemented based on the object model.
> ▪$\ \,$OOP Language has few concepts that simplify software development and maintenance, such as Encapsulation, Abstraction, Polymorphism, Inheritance, etc., that can be implemented in Java.
> 3\. **Platform Independent**
> ▪$\ \,$Java is platform-independent because it is compiled in different machines.
> ▪$\ \,$It is a language that is written once and can be executed on any platform.
> ▪$\ \,$When Java code is compiled, it is compiled in independent byte code and is interpreted by JVM (Java Virtual Machine), installed in any platform OS.
> 4\. **Secured**
> ▪$\ \,$Java is known for its security because it develops virus-free and runs inside a Virtual Machine.
> ▪$\ \,$Java uses a byte code verifier that checks the code fragments for illegal code.
> ▪$\ \,$Java checks what resources can be accessed by a class, i.e. read, write to local disk.
> 5\. **Robust**
> ▪$\ \,$Unlike other programming languages, it avoids using pointers for security reasons.
> ▪$\ \,$Exception Handling and Type checking features are available in Java.
> ▪$\ \,$It makes an effort to reduce error-prone situations by giving more attention to compile time and run time error checking.
> 6\. **Portable**
> ▪$\ \,$Java is portable because it allows you to execute the byte code to any of the platforms.
> ▪$\ \,$Java’s implementation doesn’t depend on the platform and can be carried to any of the platforms, thus making it portable.
> 7\. **High Performance**
> ▪$\ \,$Java uses the “JIT” (Just in Time) compiler to compile the byte code to native machine code when any of the Java methods is called, thus increasing the execution’s performance.
> 8\. **Distributed**
> ▪$\ \,$This feature of Java allows us to access files by calling the methods from any remote system on the internet.
> 9\. **Multithreaded**
> ▪$\ \,$A thread is a small tiny program written in Java to execute it concurrently.
> ▪$\ \,$Multithreading is one of the main features of java to deal with multiple tasks.
> ▪$\ \,$The benefit of using multithreading is that it doesn’t take up much space for every thread as it uses a single common memory area.
> 10\. **Dynamic**
> ▪$\ \,$Java is dynamic as it supports a huge amount of run-time information.
> ▪$\ \,$It supports dynamic compilation, interpretation and automatic memory management.

---
Key differences between Java **SE** (Standard Edition) and Java **EE** (Enterprise Edition).
- Java SE is the core Java programming language. The Java <mark class="hltr-lightgreen">EE platform is built on top of the SE</mark> platform, used especially for large-scale applications.
- Java SE defines everything from the basic types and objects of the Java programming language, hence provides all core functionalities. The Java EE platform provides an API and runtime environment for developing and running large-scale applications.
- Java SE platform consists of a virtual machine, development tools, deployment technologies, and other libraries commonly used in Java. Java EE consists of Enterprise JavaBeans, Java Server Pages, Servlets.
- Java SE has no code separate into different layers, while Java EE is a multi-tier application; this helps the application be more robust and more secure. Typical Java EE application has the following layers:
	- **The Client Tier**
	  The client tier is where user interaction happens. Applications in this tier access Java Server, which is usually located on a different machine. A client sends a request, the server processes this request and sends a response back to the client.
	- **The Web Tier**
	  This layer handles the interaction between the client and the business tier.
	- **The Business Tier**
	  This tier consists of business logic and all core functionalities.

[[JavaSE&EEimage.png|SE vs EE image]]

<br>

# 
---
- **SE** - https://www.educba.com/what-is-java-se/
- https://www.educba.com/java-vs-java-ee/