---
cssclass:
aliases:
tags:
- Java
- Java/Class
- Java/final
- Java/Interface
---
**[[UpdateJava#^e6542d|HOME [Java]]]**

---
## Marker Interfaces
$\qquad$are those that don’t have any methods declared. One example of such an interface is [[JavaSerialization|Serializable]]. You don’t need to write any implementation of these [[JavaInterface|interfaces]]; the Java compiler will take care of this for you. Objects of a class that implements a marker interface will support a certain functionality. For example, if a class implements **Serializable**, [[JavaJDK&JRE|JVM]] will be able to serialize it — turn into a string of bytes (in the server’s JVM) in such a way that the string can be sent to another JVM (on the client’s machine), which will be able to recreate the [[JavaClass&Object|instance of the object]], or de-serialize it.

$\qquad$Also, Java has an operator [[JavaOperatorstypecomparison|instanceof]] that can check during the run time if an object is of a certain type. You can use the operator `instanceof` as shown below to check if the object implements a marker interface, or any other type of interface for that matter:
```java
if (receivedFromServerObj instanceof Serializable) {
	// TODO put code here
}
```

<br>

# 
---
- https://www.geeksforgeeks.org/marker-interface-java/
- https://www.baeldung.com/java-marker-interfaces

See also:
**[[JavaInterface|Interfaces]]**