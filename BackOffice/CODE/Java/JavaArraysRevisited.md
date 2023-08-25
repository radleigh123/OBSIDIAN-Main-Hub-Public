---
cssclass:
aliases:
tags:
- Java
- Java/Arrays
- Java/ControlFlow/for-each
---
**[[Java#Collections|HOME [Java]]]**

---
## Arrays Revisited
**Limitations of an `array`**
- arrays are fixed in size
- arrays can only hold homogenous data elements
- ready made APIs support is not available in array

>[!aside|show-title right]+ RESULT:
> Keane Radleigh Inting Rhiz Caballero
> \------------------------
> Keane
> Radleigh
> Inting
> Rhiz
> Caballero

```java
import java.util.Scanner;

public class Main {

    String name;

    Main(String name) {
        this.name = name;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Main[] m_elements = new Main[5];

        for (int i = 0; i < 5; i++) {
            m_elements[i] = new Main(sc.next());
        }

        System.out.println("------------------------");

        for (Main j : m_elements) {
            System.out.println(j.name);
        }
        sc.close();
    }
}
```

<br>

See original:
- **[[JavaArrays|Arrays]]**