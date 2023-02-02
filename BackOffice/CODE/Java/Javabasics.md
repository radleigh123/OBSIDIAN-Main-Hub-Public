---
title: Javabasics
creation-date: 2023-02-02
aliases:
tags:
- Java/Lecture
- Java/String
- Java/Method
---
**[[Java|HOME [Java]]]**

---
# Basics
```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello" + " " + "World");
    }
}
```
<br>

**Method**
```java
public class Main {
    public static void main(String[] args) {
        String greet = "Hello";

        System.out.print(addNumbers(greet));
    }

    public static String addNumbers(String s) {
        return s + "!";
    }
}
```
<br>

**Multiple files**
>[!column|flex clean no-t]
>>[!INFO|clean no-i ttl-c] Main.java
>> ```java
>> public class Main {
>>     public static void main(String[] args) {
>>         Main2 f1 = new Main2();
>> 
>>         System.out.print(f1.main2());
>>     }
>> }
>> ```
>
>>[!INFO|clean no-i ttl-c] Main2.java
>> ```java
>> public class Main2 {
>>     public static String main2() {
>>         return "I am hotdog";
>>     }
>> }
>> ```

<br>

**Arrays** - missing variables arr1 not used
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> arr1 = new ArrayList<Integer>();
    }
}
```
<br>

**Try catch**
```java
try {
	// Runs the code here
} catch(Exception e) {
	// Goes here, if there's error
}
```