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
**[[Java|HOME [Java]]]**

---
# Serialization
To **serialize** an [[JavaClass&Object|object]] means to <mark class="hltr-lightgreen">convert its state to a byte stream</mark> so that the byte stream can be reverted back into a copy of the object. A Java object is *serializable* if its class or any of its superclasses implements either the `java.io.Serializable` interface or its subinterface, `java.io.Externalizable`.
- This byte stream can be saved as a file, sent over a network, or sent to a different machine
- Byte stream can be saved as file(`.ser`) which is platform independent

<br>

**Deserialization** is the process of converting the serialized form of an object back into a copy of the object.
*"Think of this as if you're loading a saved file"*

- [[JavaSerializationSample|Steps to Serialize]]
- [[JavaSerializationSample1|Steps to Deserialize]]

>[!WARNING|alt-co] REMEMBER
>▪ children classes of a parent class that implements `Serializable` will do so as well
>▪ `static fields` are not serialized (they belong to the class, not an individual object)
>▪ the class's definition ("*class file*") itself is not recorded, cast it as the object type
>▪ Fields declared as `transient` aren't serialized, they're ignored
>▪ `serialVersionUID` is a unique version ID

<br>

# 
---
- https://docs.oracle.com/javase/7/docs/api/java/io/Serializable.html
	- **[Serializable Objects](https://docs.oracle.com/javase/tutorial/jndi/objects/serial.html)**
- https://www.baeldung.com/java-serialization
- [[JavaSerializationELI5|STILL DUMB ENOUGH TO UNDERSTAND]] ^370fd8