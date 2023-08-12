---
cssclass:
aliases:
tags:
- Java
- Java/Lecture
- Java/Packages
---
**[[UpdateJava#Packages, Interfaces, and Encapsulation|HOME [Java]]]**

---
## Java Packages
A decently size project can have hundreds of Java classes and you need to organize them in packages (like *file directories*). This will allow you to categorize files, control access to your classes (see “**[[JavaAccessModifiers|Access Levels]]**”), and avoid potential naming conflicts.

Java classes are also organized into packages and the fully qualified name of a class consists of the package name followed by the class name. For example, the full name of the Java class **Double** is `java.lang.Double`, where `java.lang` is the package name.

>[!EXAMPLE]-
> Let’s say your class needs to connect to some URL on the Net with the help of the class [[JavaURL|URL]] located in the `java.net package`:
> ```java
> java.net.URL sampleURL = new java.net.URL (“http://www.acme.com”);
> ```
> But instead of using this rather long notation, include the `import` statement right above the class declaration, and then use just the name of the class:
> ```java
> import java.net.URL;
> 
> class myClass {
> 	URL sampleURL = new URL("http://www.acme.com");
> 	...
> }
> ```

**Importing several classes from the same package** (*[[JavaWildCard|wild card]]* or `*`)
```java
import java.net.*;
```

**Custom packages**
Tools package
![[JavaPackagesiamge.png]]

Toolbox class
```java
package Tools;

public class Toolbox {
    // TODO Put code here
}
```

Main class
```java
import Tools.Toolbox;

public class Proto {
    public static void main(String[] args) {
        Toolbox toolbox = new Toolbox();
    }
}
```

<br>

# 
---
- [Java Packages (w3schools.com)](https://www.w3schools.com/java/java_packages.asp)
- [Java Package - javatpoint](https://www.javatpoint.com/package)