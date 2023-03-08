---
cssclass:
title: JavaClass&Object
creation-date: 2023-03-04
aliases:
tags:
- Java
- Java/Lecture
- Java/Class
---
**[[UpdateJava|HOME [Java]]]**

---
# Classes and Objects
A Java class is like a blueprint in engineering, and until you build real objects based on this blueprint you can’t use them.

Creating **objects**, aka **instances**, based on classes is the equivalent of building real cars based on blueprints. To <mark class="hltr-lightgreen">create an instance of a class means to create the object in the computer’s memory</mark> based on the class definition.
```java
// Superclass and Subclass

class Car {
	// Some code goes here
}

class SportsCar extends Car {
	// Some code goes here
}
```

>[!CITE|alt-co] An entity that has state and behavior is known as an object e.g., chair, bike, marker, pen, table, car, etc.

```java
// Instantiating a class

myClass class1 = new myClass();
myClass class2 = new myClass();
```
![[JavaObjectsimage0.png|ws-med cover center]]

<br>

---
**Learn more**
- [[JavaObjectsarrays|Array of Objects]]
- [[JavaObjectsCopy|Copy objects]] ^1a283e

<br>

# 
---
- https://docs.oracle.com/javase/7/docs/api/java/lang/Object.html
- https://www.javatpoint.com/object-and-class-in-java