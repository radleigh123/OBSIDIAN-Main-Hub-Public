**4.5** Nesting if and if... else Statements
Create your own Java program using nested if and if--else statements.
```java
public class Main {
    public static void main(String[] args) {
        int x = 50;

        if (x > 0) {
            if (!(x < 50)) {
                System.out.println(x + " is greater than 50.");
            } else {
                System.out.println(x + " is less than 50.");
            }
        } else {
            System.out.println(x + " is zero or a negative number");
        }
    }
}
```

**4.6** Using the switch Statement
Create your own Java program using switch statement.
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Choose a year [1]-First [2]-Second [3]-Third: ");

        switch (sc.nextInt()) {
            case 1:
                System.out.println("First Year");
                break;
            case 2:
                System.out.println("Second Year");
                break;
            case 3:
                System.out.println("Third Year");
                break;
            default:
                System.out.println("Invalid output");
                break;
        }
        sc.close();
    }
}
```

**4.7** Using Logical AND, OR, and NOT Operators
Create your own Java program using Logical operators.
```java
public class Main {
    public static void main(String[] args) {
        int x = 150;
        int y = 20;
        String result;

        result = (x > 0 && x > y) ? (x + " is a positive number and greater than " + y)
                : (x + " is either a negative or not greather than " + y);

        System.out.println(result);
    }
}
```