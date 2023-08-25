---
aliases:
tags:
- Java
- Java/Operators/Shift
---
**[[JavaOperators|BACK]]**

---
## Shift Operators
By shifting the bits of its first operand right or left, a shift operator performs bit manipulation on data.

| <center>Operator</center>                                 | <center>Sign</center> | <center>Description</center>                                                                                         |
| --------------------------------------------------------- | --------------------- | -------------------------------------------------------------------------------------------------------------------- |
| [[JavaOperatorsShiftLeft\|Signed Left Shift]]             | `<<`                  | The left shift operator moves all bits by a given number of bits to the left.                                        |
| [[JavaOperatorsShiftRight\|Signed Right Shift]]           | `>>`                  | The right shift operator moves all bits by a given number of bits to the right.                                      |
| [[JavaOperatorsShiftRightUnsigned\|Unsigned Right Shift]] | `>>>`                 | It is the same as the signed right shift, but the vacant leftmost position is filled with 0 instead of the sign bit. |

<br>

## Bitwise Operators
The bitwise **&** operator performs a bitwise AND operation.
The bitwise **^** operator performs a bitwise exclusive OR operation.
The bitwise **|** operator performs a bitwise inclusive OR operation.
The bitwise **~** operator performs a bitwise NOT operation.

The following program, BitDemo, uses the bitwise `AND`(`&`) operator to print the number **2** to standard output.
```java
class BitDemo {
    public static void main(String[] args) {
        int bitmask = 0x000F;
        int val = 0x2222;
        
        System.out.println(val & bitmask); // prints 2
    }
}
```

<br>

# 
---
- [Shift Operator in Java - GeeksforGeeks](https://www.geeksforgeeks.org/shift-operator-in-java/)
- [Java Bitwise and Shift Operators (With Examples) (programiz.com)](https://www.programiz.com/java-programming/bitwise-operators)
- https://docs.oracle.com/javase/tutorial/java/nutsandbolts/op3.html