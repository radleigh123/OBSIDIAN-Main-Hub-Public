---
title: Javauserinput
creation-date: 2023-02-03
aliases:
tags:
- Java
- Java/java.util/Scanner
---
**[[Java#Java Basics|HOME [Java]]]**

---
<center>package: <strong>java.util.Scanner</strong></center>

# Scanner class
- A Scanner breaks its input into tokens using a delimiter pattern, which by default matches whitespace.
- The resulting tokens may then be converted into values of different types using the various next methods.
	- **nextLine()**: Reads the next line of text as a `String`.
	- **nextInt()**: Reads the next token as an `int`.
	- **nextFloat()**: Reads the next token as a `float`.
	- **nextDouble()**: Reads the next token as a `double`.
	- **nextBoolean()**: Reads the next token as a `boolean`.
	- **nextLong()**: Reads the next token as a `long`.

**e.g.**
```cpp
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Enter name: ");
        String name = sc.nextLine();
        System.out.print("Enter age: ");
        int age = sc.nextInt();
        System.out.print("Enter height: ");
        double height = sc.nextDouble();
        System.out.print("Are you boy: ");
        boolean sex = sc.nextBoolean();
        
        sc.close(); // closing

        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Height: " + height);
        System.out.println("Are you !geh: " + sex);
    }
}
```

---
- [[JavaScannersample0|Solution for program skipping inputs]]
- [[JavaScannersample1|Multiple inputs in a single line]]

<br>

# 
---
**Sources:**
- https://docs.oracle.com/javase/7/docs/api/java/util/Scanner.html