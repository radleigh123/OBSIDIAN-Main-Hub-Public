---
cssclass:
aliases:
tags:
- Java
- Java/Generics
- Java/WrapperClass
---
**[[JavaGenerics|BACK]]**

---
>[!aside|show-title right]+ RESULT:
> 1 2 3 4 5 
> B Y E

```java
public class Proto {
    public static void main(String[] args) {
        Integer[] intArray = { 1, 2, 3, 4, 5 };
        String[] stringArray = { "B", "Y", "E" };

        printArray(intArray);
        printArray(stringArray);
    }

    public static <T> void printArray(T[] array) {
        for (T x : array) {
            System.out.print(x + " ");
        }
        System.out.println();
    }
}
```

<br>

# 
---
- See also:
	- [[JavaTypeErasure|Type Erasure]]