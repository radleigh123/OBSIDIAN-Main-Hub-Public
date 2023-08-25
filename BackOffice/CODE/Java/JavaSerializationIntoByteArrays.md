---
cssclass:
aliases:
tags:
- Java
- Java/Serialization
---
**[[Java#Java Serialization|HOME [Java]]]**

---
## Serializing into Byte Arrays
An interesting effect will be produced if you [[JavaObjectOutputStream|serialize]] your objects into an in-memory [[JavaArrays|array]] of bytes - `byte[]`. This can be the easiest way of creating a sort of memory blob that can be exchanged among different [[JavaJDK&JRE|VMs]]. The syntax of such [[JavaSerialization|serialization]] is pretty straightforward. Let’s assume that you have a class called XYZ that implements Serializable and contains all the elements of your report in the proper format. To prepare a byte array from it, write the code from below:
```java
XYZ myXyz = new XYZ();

// Code to fill myXyz with the content goes here
//...

ByteArrayOutputStream baOut = new ByteArrayOutputStream(5000);

ObjectOutputStream oOut = new ObjectOutputStream(new BufferedOutputStream(baOut));

//Here comes the serialization part
oOut.writeObject(myXyz);
oOut.flush();

// create a byte array from the stream
byte[] xyzAsByteArray = baOut.toByteArray();

oOut.close();
```
Another convenient use for serializing into a byte array is [[JavaObjectsCopy|object cloning]], which is the creation of an exact copy of an object instance. Even though the class Object, the root of all classes, includes the method `clone()`, it works only with objects that implement the `Cloneable` marker interface; otherwise the cloning will fail. Things may get more complicated when an object contains instances of other objects: You need to program a **deep copy of the object**.

Serialization into a byte array with immediate deserialization creates a deep copy of the object in no time. After executing the code from below you’ll get two identical objects in memory. The variable *bestEmployee* points at one of them, and the variable *cloneOfBestEmployee* points at another
```java
Employee bestEmployee = new Employee();

//Serialize into byte array
ByteArrayOutputStream baOut = new ByteArrayOutputStream();
ObjectOutputStream oOut = new ObjectOutputStream(baOut);
oos.writeObject(bestEmployee);

//Deserialize from byte array
ByteArrayInputStream baIn = new ByteArrayInputStream(baOut.toByteArray());
ObjectInputStream oIn = new ObjectInputStream(baIn);
Employee cloneOfBestEmployee = (Employee) oin.readObject();
```