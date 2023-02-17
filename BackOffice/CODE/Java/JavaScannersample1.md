---
aliases:
tags:
- Java/java.util/Scanner
---
**[[JavaScanner|BACK]]**

---
## Multiple inputs in a single line
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Enter all: ");
        String name = sc.next(); // alternative to `nextLine()`
        int age = sc.nextInt();
        float height = sc.nextFloat();
        boolean isStudent = sc.nextBoolean();
        
        sc.close();
        
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Height: " + height + " meters");
        System.out.println("Student: " + isStudent);
    }
}
```

<br>

**Direct one line input**
```java
Scanner sc = new Scanner(System.in);
int z = sc.nextInt() + sc.nextInt();

System.out.println("z: " + z);
```