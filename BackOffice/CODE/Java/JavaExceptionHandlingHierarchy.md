---
cssclass:
aliases:
tags:
- Java
- Java/Exceptions
---
**[[Java#Error Handling|HOME [Java]]]**

---
## Exception Handling Hierarchy
![[JavaExceptionHandlingimage0.png|center]]

Subclasses of Exception are called **[[JavaExceptionHandling#^4a4a2d|checked exceptions]]** and have to be handled in your code. You can declare and throw your own application-specific exception, for example `BadShipmentAddressException`.

Subclasses of the class Error are fatal [[JavaJDK&JRE|JVM]] errors and are called **[[JavaExceptionHandling#^4a4a2d|unchecked]]**. You are not required to put them in [[JavaExceptionHandlingtrycatch|try/catch]] blocks as there is not much you can do if, say the JVM runs out of memory and crashes.