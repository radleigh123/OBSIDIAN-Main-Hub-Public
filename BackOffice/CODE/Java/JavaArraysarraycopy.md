---
aliases:
tags:
- Java
- Java/Arrays
---
**[[JavaArrays|BACK]]**

---
## `arraycopy` Method
```java
public static void arraycopy(Object src, int srcPos,
                             Object dest, int destPos,
                             int length)
```

**e.g.**
```java
public class Proto1 {
    public static void main(String[] args) {
        String[] src = {
                "Hello ", "World",
                "Keane ", "Radleigh" };

        String[] dest = new String[src.length];
        System.arraycopy(src, // source of string
                2, // where to start copying
                dest, // destination
                0, // where to start putting copied string
                (src.length - 2)); // size of string to be copied

        for (String str : dest) {
            System.out.print(str + " ");
        }
    }
}
```