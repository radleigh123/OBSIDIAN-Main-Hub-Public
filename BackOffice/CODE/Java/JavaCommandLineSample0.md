---
cssclass:
aliases:
tags:
- Java
- Java/String
- Java/WrapperClass/Double/parseDouble
- Java/WrapperClass/Integer/parseInt
---
**[[JavaCommandLine|BACK]]**

---
>[!grid]
> ![[JavaCommandLineSample0image.png]]
> ![[JavaCommandLineSample0image1.png]]

<br>

>[!aside|show-title right]+ RESULT:
> 456
> Cebu

```java
/**
* Passing data from Command Line Interface
* to the program
*/

class myClass {

    int m_address;
    String m_state;

    myClass(int m_address, String m_state) {
        this.m_address = m_address;
        this.m_state = m_state;
    }

}

public class Proto {

    public static void main(String[] args) {
        System.out.println(Integer.parseInt(args[0]));
        System.out.println(args[1]);
    }

}
```
