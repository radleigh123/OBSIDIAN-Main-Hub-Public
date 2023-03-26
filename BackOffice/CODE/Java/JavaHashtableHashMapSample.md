---
cssclass:
aliases:
tags:
- Java
- Java/java.util
- Java/HashMap
---
**[[JavaHashtableHashMap#HashMap|BACK]]**

---
>[!aside|show-title right]+ RESULT:
> true
> true
> superboy
> {girl=wondergirl, boy=superman, gay=aquageh}

```java
import java.util.*;

public class Proto {
    public static void main(String[] args) {

        HashMap<String, String> map = new HashMap<>();
        map.put("boy", "superboy");
        map.put("girl", "wondergirl");
        map.put("gay", "aquageh");

        System.out.println(map.containsValue("aquageh")); // returns TRUE, if any value matches
        System.out.println(map.containsKey("gay")); // vice versa

        System.out.println(map.replace("boy", "superman")); // replaces the key's value

        System.out.println(map);

    }
}
```