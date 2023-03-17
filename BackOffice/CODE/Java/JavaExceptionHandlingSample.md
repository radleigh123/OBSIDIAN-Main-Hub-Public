---
cssclass:
aliases:
tags:
- Java
- Java/Exceptions
---
**[[UpdateJava#Error Handling|HOME [Java]]]**

---
## Creating your own Exceptions
Programmers can also create exceptions specific to their business applications. Such a [[JavaClass&Object|class]] has to be a subclass of one of the classes from the hierarchy of [[JavaExceptionHandlingHierarchy|Throwable]] objects.

###### Program example: Business of selling bikes and need to validate a customer's order
Create a new class, **TooManyBikesException**, and [[JavaExceptionHandlingthrow|throw]] it if someone tries to order more bikes than can fit into one container, as in the class **BikeOrder** shown in below.
```java
/**
 * TooManyBikesException.java
 */

public class TooManyBikesException extends Exception {

    TooManyBikesException(String msg) {
        super(msg);
    }

    public static void main(String[] args) {
        try {
            BikeOrder.validateOrder("Keane", 12); // since method is `static`
        } catch (TooManyBikesException e) {
            e.printStackTrace();
            // System.out.println("ERROR: " + e.toString());
        }
    }

}
```
```java
/**
 * BikeOrder.java
 */

public class BikeOrder {

    static void validateOrder(String bikeMode1,
            int quantity) throws TooManyBikesException {

        if (quantity >= 10) {
            throw new TooManyBikesException("Invalid model number: " + quantity + " " + bikeMode1);
        }

    }

}
```
Result:
>[!INFO|alt-co collapse clean no-t]
> TooManyBikesException: Invalid model number: 12 Keane
> $\quad$at BikeOrder.validateOrder(BikeOrder.java:7)
> $\quad$at TooManyBikesException.main(TooManyBikesException.java:9)