---
aliases:
tags:
- Java/java.util/Scanner
---
**[[JavaScanner|BACK]]**

---
## Solution for program skipping inputs
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Name: ");
        String name = sc.nextLine();
        System.out.print("Age: ");
        int age = sc.nextInt();
        sc.nextLine(); // consumes the newline character
        System.out.print("School: ");
        String school = sc.nextLine();

        System.out.println("Name is " + name);
        System.out.println(age + " years old");
        System.out.println("Studies at " + school);
    }
}
```