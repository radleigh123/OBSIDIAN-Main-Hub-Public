---
cssclass:
title: JavaSerializationExternalizable
creation-date: 2023-04-13
aliases:
tags:
- Java
- Java/Interface
- Java/Serialization
- Java/Serializable/Externalizable
---
**[[UpdateJava#Java Serialization|HOME [Java]]]**

---
# Externalizable Interface
Externalization serves the purpose of custom [[JavaSerialization|Serialization]], where we can decide what to store in stream, which is a subclass of [[JavaSerialization|Serializable]].

It consist of two methods which we have to override to write/read object into/from stream which are:
$\quad$ ▪ `readExternal()` - to read object from stream
$\quad$ ▪ `writeExternal()` - to write object into stream

>[!EXAMPLE]- SERIALIZABLE vs EXTERNALIZABLE
> **Serialization responsibility**
> The key difference here is how we handle the serialization process. When a class implements the `java.io.Serializable` interface, the JVM takes full responsibility for serializing the class instance. <u>In case of Externalizable, it's the programmer who should take care of the whole serialization and also deserialization process.</u>
> **Use Case**
> If we need to serialize the entire object, the Serializable interface is a better fit. On the other hand, <u>for custom serialization, we can control the process using Externalizable.</u>
> **Performance**
> The java.io.Serializable interface uses reflection and metadata which causes relatively slow performance. By comparison, the <u>Externalizable interface gives you full control over the serialization process.</u>
> **Reading Order**
> <u>While using Externalizable, it's mandatory to read all the field states in the exact order as they were written.</u> Otherwise, we'll get an exception.
>> For example, if we change the reading order of the code and name properties in the Country class, a java.io.EOFException will be thrown.
>
> Meanwhile, the Serializable interface doesn't have that requirement.
> **Custom Serialization**
> We can achieve custom serialization with the Serializable interface by marking the field with [[JavaSerializationtransient|transient]] keyword. <u>The JVM won't serialize the particular field but it'll add up the field to file storage with the default value.</u> That's why it's a good practice to use Externalizable in case of custom serialization.

Example of externalization:
```java

// Java program to demonstrate working of Externalization
// interface
import java.io.*;

class Car implements Externalizable {
    static int age;
    String name;
    int year;

    public Car() {
        System.out.println("Default Constructor called");
    }

    Car(String n, int y) {
        this.name = n;
        this.year = y;
        age = 10;
    }

    @Override
    public void writeExternal(ObjectOutput out)
            throws IOException {
        out.writeObject(name);
        out.writeInt(age);
        out.writeInt(year);
    }

    @Override
    public void readExternal(ObjectInput in)
            throws IOException, ClassNotFoundException {
        name = (String) in.readObject();
        year = in.readInt();
        age = in.readInt();
    }

    @Override
    public String toString() {
        return ("Name: " + name + "\n"
                + "Year: " + year + "\n"
                + "Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {
        Car car = new Car("Shubham", 1995);
        Car newcar = null;

        // Serialize the car
        try {
            FileOutputStream fo = new FileOutputStream("gfg.txt");
            ObjectOutputStream so = new ObjectOutputStream(fo);
            so.writeObject(car);

            so.flush();
            so.close();
        } catch (Exception e) {
            System.out.println(e);
        }

        // Deserialization the car
        try {
            FileInputStream fi = new FileInputStream("gfg.txt");
            ObjectInputStream si = new ObjectInputStream(fi);
            newcar = (Car) si.readObject();

            si.close();
        } catch (Exception e) {
            System.out.println(e);
        }

        System.out.println("The original car is:\n" + car);
        System.out.println("The new car is:\n" + newcar);
    }
}
```
```txt
# gfg
RANDOM_CHARACTERS_BECAUSE_OF_SERIALIZATION
```
>[!INFO|clean no-i collapse ttl-c] RESULT:
> Default Constructor called
> The original car is:
> Name: Shubham       
> Year: 1995
> Age: 1995
> The new car is:
> Name: Shubham
> Year: 10
> Age: 1995

<br>

# 
---
- https://www.developer.com/design/externalizable-interface-java/
- https://www.geeksforgeeks.org/externalizable-interface-java/
- https://www.baeldung.com/java-externalizable