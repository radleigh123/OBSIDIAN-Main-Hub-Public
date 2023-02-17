---
aliases:
tags:
- Java/String
---
**[[JavaVariables|BACK]]**

---
## Program to swap variables
```cpp
public class Main {
    public static void main(String[] args) {
        String str1 = "String1", str2 = "String2";
        String temp = str1;

        str1 = str2;
        str2 = temp;

        System.out.println("str1: " + str1);
        System.out.println("str2: " + str2);
    }
}
```

<br>

# 
---
**Sources:**
- **null** - https://www.upwork.com/resources/what-is-null-in-java