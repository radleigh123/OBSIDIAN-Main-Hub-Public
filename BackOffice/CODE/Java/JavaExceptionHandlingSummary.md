---
cssclass:
aliases:
tags:
- Java
- Java/Exceptions
---
**[[Java#Error Handling|HOME [Java]]]**

---
## Summary
$\quad$In distributed [[JavaSE&EE|Java EE]] applications an exception can travel through several tiers (such as **JMS**, **EJB**, **Servlet**, **Swing client**), and not only does having a custom property inside the exception object ensure that the valuable information won’t be lost, but each tier can add more specifics to this custom property, helping in tracing the error.

There is also a class called `RemoteException`, with a field called `detail`, that’s used for reporting communication errors. You can extend this class to make remote exceptions more descriptive. This subject may be more appropriate for the lessons about the [[Java#Java EE 6 Overview|server-side technologies]].

Keep in mind that a Java program can communicate with *non-Java systems*, and that throwing `RemoteException` or its subclass is a proper way to handle cross-language errors. For example, this technique is used for communications based on *Adobe’s AMF* protocol between server-side Java and a rich Internet client application written with *Adobe Flex*.

See more:
- [Lesson: Exceptions (oracle)](https://docs.oracle.com/javase/tutorial/essential/exceptions/)