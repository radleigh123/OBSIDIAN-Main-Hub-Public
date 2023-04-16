---
cssclass:
title: JavaSerialization
creation-date: 2023-03-10
aliases:
tags:
- Java
- Java/java.io
- Java/Serializable
- Java/Serialization
- Java/Deserialization
- Java/serialVersionUID
---
**[[UpdateJava#Java Serialization|HOME [Java]]]**

---
### Serialization
The process of serialization converts the state of an [[JavaClass&Object|object]] into a stream of bytes. If we want to store an object in a file, it is necessary to convert it into bytes. A Java object is *serializable* if its class or any of its superclasses implements either the `java.io.Serializable` interface or its subinterface, `java.io.Externalizable`.
$\quad$ ▪ This byte stream can be saved as a file, sent over a network, or sent to a different machine
$\quad$ ▪ Byte stream can be saved as file(`.ser`) which is platform independent

### Deserialization
the process of converting the serialized form of an object back into a copy of the object, *"Think of this as if you're loading a saved file"*

>[!INFO|collapse clean no-i ttl-c] [[JavaSerializationELI5|ELI5 Serialization]]

- [[JavaObjectOutputStream|Serialize using ObjectOutputStream]]
- [[JavaObjectInputStream|Deserialize using ObjectInputStream]]

>[!WARNING|alt-co] REMEMBER
> $\quad$ ▪ children classes of a parent class that implements `Serializable` will do so as well
> $\quad$ ▪ `static fields` are not serialized (they belong to the class, not an individual object)
> $\quad$ ▪ the class's definition ("*class file*") itself is not recorded, cast it as the object type
> $\quad$ ▪ Fields declared as [[JavaSerializationtransient|transient]] aren't serialized, they're ignored
> $\quad$ ▪ `serialVersionUID` is a unique version ID

<br>

# 
---
- https://docs.oracle.com/javase/7/docs/api/java/io/Serializable.html
	- **[Serializable Objects](https://docs.oracle.com/javase/tutorial/jndi/objects/serial.html)**
- https://www.baeldung.com/java-serialization