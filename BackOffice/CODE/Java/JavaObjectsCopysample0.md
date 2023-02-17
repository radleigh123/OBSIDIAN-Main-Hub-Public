---
aliases:
tags:
- Java
- Java/Lecture
- Java/Class/Constructor/Copy
---
**[[JavaObjectsCopy|BACK]]**

---
## Using Assignment Operator to create a copy of the reference variable
```java
class Test {
    int m_num1 = 10;
}

public class Proto {
    public static void main(String[] args) {
        Test t1 = new Test();
        Test t2 = t1;

        System.out.println(t1);
        System.out.println(t2);
        System.out.println("---------");
        System.out.println(t1.m_num1);
        System.out.println(t2.m_num1);
    }
}

/*
Test@36baf30c
Test@36baf30c
---------    
10
10
*/
```