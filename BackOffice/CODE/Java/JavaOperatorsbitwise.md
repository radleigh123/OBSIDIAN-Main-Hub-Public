---
aliases:
tags:
- Java
- Java/Lecture
- Java/Operators/Bitwise
---
**[[JavaOperators|BACK]]**

---
## Bitwise & Bit Shift Operators
The bitwise **&** operator performs a bitwise AND operation.
The bitwise **^** operator performs a bitwise exclusive OR operation.
The bitwise **|** operator performs a bitwise inclusive OR operation.

The following program, BitDemo, uses the bitwise AND operator to print the number "2" to standard output.
```java
class BitDemo {
    public static void main(String[] args) {
        int bitmask = 0x000F;
        int val = 0x2222;
        // prints "2"
        System.out.println(val & bitmask);
    }
}
```

<br>

# 
---
- https://docs.oracle.com/javase/tutorial/java/nutsandbolts/op3.html