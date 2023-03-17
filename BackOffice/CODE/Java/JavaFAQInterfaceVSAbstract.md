---
cssclass:
aliases:
tags:
- Java
- Java/Lecture
- Java/Class/Abstract
- Java/Interface
---
**[[UpdateJava#Packages, Interfaces, and Encapsulation|HOME [Java]]]**

---
## Interfaces vs Abstract Classes
If two or more classes have lots of common functionality, but some methods should be implemented differently, you can create a common abstract ancestor and as many subclasses inheriting this common behavior as needed. Declare in the superclass as abstract those methods that subclasses should implement differently, and implement these methods in subclasses.

If several classes don’t have common functionality but need to exhibit some common behavior, do not create a common ancestor, but have them implement an interface that declares the required behavior. 

Interfaces and abstract classes are similar in that they ensure that required methods will be implemented according to required method signatures. But they differ in how the program is designed. While abstract classes require you to provide a common ancestor for the classes, interfaces don’t. Interfaces could be your only option if a class already has an ancestor that cannot be changed. Java doesn’t support multiple inheritance — a class can have only one ancestor. 
> For example, to write Java applets you must inherit your class from the class Applet, or in the case of [[JavaSwing|Swing]] applets, from [[JavaSwingJApplet|JApplet]]. Here using your own abstract ancestor is not an option.

<br>

# 
---
- [[JavaFAQInterfaceVSAbstractELI5|IF STILL DUMB ENOUGH]]