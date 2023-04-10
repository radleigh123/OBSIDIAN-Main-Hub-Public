---
cssclass:
aliases:
tags:
- Java
- Java/Generics
- Java/Methods
---
**[[UpdateJava#Generics|HOME [Java]]]**

---
## Generic Methods
We write generic methods with a single method declaration, and we can call them with arguments of different types. The compiler will ensure the correctness of whichever type we use.

These are some properties of generic methods:
$\quad$▪ Generic methods have a type parameter (the diamond operator enclosing the type) before the return type of the method declaration.
$\quad$▪ Type parameters can be bounded (we explain bounds later in this article).
$\quad$▪ Generic methods can have different type parameters separated by commas in the method signature.
$\quad$▪ Method body for a generic method is just like a normal method.

```java
// Here's an example of defining a generic method to convert an array to a list

public <T> List<T> fromArrayToList(T[] a) {
    return Arrays.stream(a).collect(Collectors.toList());
}
```
The `<T>` in the method signature implies that the method will be dealing with generic type `T`. This is needed even if the method is returning void. As mentioned, the method can deal with more than one generic type. Where this is the case, we must add all generic types to the method signature.
```java
// Here is how we would modify the above method to deal with type T and type G

public static <T, G> List<G> fromArrayToList(T[] a, Function<T, G> mapperFunction) {
    return Arrays.stream(a)
      .map(mapperFunction)
      .collect(Collectors.toList());
}
```
We're passing a function that converts an array with the elements of type `T` to list with elements of type `G`.

```java
// An example would be to convert `Integer` to its `String` representation

public void givenArrayOfIntegers_thanListOfStringReturnedOK() {
    Integer[] intArray = {1, 2, 3, 4, 5};
    List<String> stringList
      = Generics.fromArrayToList(intArray, Object::toString);
 
    assertThat(stringList, hasItems("1", "2", "3", "4", "5"));
}
```

>[!NOTE|collapse alt-co]
> Note that Oracle recommendation is to use an uppercase letter to represent a generic type and to choose a more descriptive letter to represent formal types. In Java Collections, we use `T` for type, `K` for key and `V` for value.

<br>

More example:

>[!aside|right show-title]+ RESULT:
> 45.21!!!
> true!!!!
> returned value: 45.21

```java
public class Main {

    public static void main(String[] args) {
        System.out.println("returned value: " + shout(45.21, true));
    }

    private static <T, K> T shout(T a, T b) {
        System.out.println(a + "!!!");
        System.out.println(b + "!!!!");

        return a;
    }
}
```

<br>

# 
---
- [Generic Methods (oracle)](https://docs.oracle.com/javase/tutorial/java/generics/methods.html)
- [Java Generics (Baeldung)](https://www.baeldung.com/java-generics#generic-methods)
- [Java - Generics (tutorialspoint)](https://www.tutorialspoint.com/java/java_generics.htm)