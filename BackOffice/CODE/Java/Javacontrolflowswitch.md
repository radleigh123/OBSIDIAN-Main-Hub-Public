---
aliases:
tags:
- Java
- Java/Lecture
- Java/ControlFlow/switch
- Java/String/toLowerCase
---
**[[JavaControlFlow|BACK]]**

---
## The Switch Statement
**Using Strings**
```java
public class Proto1 {
    public static void main(String[] args) {
        String month = "NoVember";
        int monthNumber = 0;

        switch (month.toLowerCase()) {
            case "september":
                monthNumber = 9;
                break;
            case "october":
                monthNumber = 10;
                break;
            case "november":
                monthNumber = 11;
                break;
            case "december":
                monthNumber = 12;
                break;
            default:
                System.out.println("Unknown month");
        }

        System.out.println(monthNumber);
    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/nutsandbolts/switch.html