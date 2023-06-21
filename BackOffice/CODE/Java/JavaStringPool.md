---
cssclass:
aliases:
tags:
- Java
- Java/String 
---
**[[UpdateJava#Java Memory Management|HOME [Java]]]**

---
## String Pool
is nothing but a storage area in the [[JavaMemoryManagementStack|heap]] where string literals stores. It is also known as **String Intern Pool** or **String Constant Pool**. It is just like object allocation.

![[JavaStringPool.png|center wm-tl]]

To decrease the number of `String` objects created in the JVM the [[JavaString|String class]] keeps a pool of strings. When we create a string literal, the JVM first check that literal in the String pool.
$\quad$▪ If the literal is already present in the pool, it returns a reference to the pooled instance.
$\quad$▪ If the literal is not present in the pool, a new `String` object takes place in the String pool.

>[!aside|right show-title]- RESULT:
> (s1 == s2): TRUE
> (s1 == s3): FALSE
> (s1 == s4): TRUE
```java
package StringPool;

public class Main {
    public static void main(String[] args)
    {
        String s1 = "Java";
        String s2 = "Java";
        String s3 = new String("Java");
        String s4 = new String("Java").intern();

        Boolean bool = (s1 == s2);
        System.out.println("(s1 == s2): " + bool.toString().toUpperCase());

        bool = (s1 == s3);
        System.out.println("(s1 == s3): " + bool.toString().toUpperCase());

        bool = (s1 == s4);
        System.out.println("(s1 == s4): " + bool.toString().toUpperCase());
    }
}

/*
In the above example, we have seen that whenever we use a new operator to create a string it creates a new string object in the Java heap. We can forcefully stop this feature by using the intern() method of the String class.
*/

```
> Remember that all the string literals created with the `new` keyword take place in the <u>heap</u>, not in the String pool.

<br>

**`intern()` method**
The `String.intern()` method puts the string in the String pool or refers to another String object from the string pool having the same value. It returns a string from the pool if the string pool already contains a string equal to the String object. It determines the string by using the `String.equals(Object)` method. If the string is not already existing, the String object is added to the pool, and a reference to this String object is returned.
```java
String str1 = new String("Hello");
// statement creates the string in the Java heap

String str2 = new String("Hello").intern();
// stores the string literal in the String pool
```

<br>

# 
---
- [String Pool in Java - Javatpoint](https://www.javatpoint.com/string-pool-in-java)