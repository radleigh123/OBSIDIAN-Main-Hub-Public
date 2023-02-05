---
aliases:
tags:
- Java
- Java/java.util/Scanner
- Java/Math/sqrt
- Java/Math/pow
---
**[[JavaMath|BACK]]**

---
## Finding hypotenuse of a triangle
```java
import java.util.Scanner;

public class Proto1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double x, y, z;

        System.out.print("Enter x value: ");
        x = Double.parseDouble(sc.nextLine());
        System.out.print("Enter y value: ");
        y = Double.parseDouble(sc.nextLine());
        sc.close();

        z = Math.sqrt(Math.pow(x, 2) + Math.pow(y, 2));
        System.out.print("Hypotenuse: " + z);
    }
}
```