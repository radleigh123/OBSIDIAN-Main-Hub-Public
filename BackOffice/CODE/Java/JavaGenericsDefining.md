---
cssclass:
aliases:
tags:
- Java
- Java/Generics
---
**[[Java#Generics|HOME [Java]]]**

---
## Defining Generics
> Some developers use `<E>` for element; some prefer `<T>` for type. Such a letter will be replaced by a concrete type when used with generics’ notation during concrete variable declaration, e.g., the source code of the Java class [[JavaHashtableHashMap#Hashtable (legacy collection class)|Hashtable]] uses `<K, V>` for *key* and *value*, respectively.
>>[!INFO|clean collapse no-t txt-c]
>> $\,\,$**T** - Type
>> $\quad\,\,\,$**E** - Element
>> **K** - Key
>> $\quad\,\,\,$**N** - Number
>> $\,\,\,\,$**V** - Value

>[!aside|right show-title]+ RESULT:
> java.lang.String: Keane
> java.lang.Integer: 123

```java
public class Main {
    static <T> void display(T passedVar) {
        System.out.println(passedVar.getClass().getName() + ": " + passedVar);
    }

    public static void main(String[] args) {
        display("Keane");
        display(123);
    }
}
```