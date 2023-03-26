---
cssclass:
title: JavaBitSet
creation-date: 2023-03-25
aliases:
tags:
- Java
- Java/java.util
- Java/BitSet
---
**[[UpdateJava#Introduction to Collections|HOME [Java]]]**

---
# `BitSet` class
$\quad$▪ creates a special type of array that holds bit values.
$\quad$▪ can increase in size as needed. This makes it similar to a vector of bits.

> All bits are initially `false`.

Simple BitSet program
>[!aside|show-title right]+ RESULT: 
> Alex Smith
> VIP Customer
> Mary Lou

```java
/**
 * Main.java
 */

import java.util.BitSet;

public class Main {

    public static void main(String[] args) {

        BitSet report = new BitSet();
        report.set(0);
        report.set(1);
        report.set(2);

        new VendingMachine(report);

    }

}
```
```java
/**
 * VendingMachine.java
 */

import java.util.BitSet;

public class VendingMachine {

    VendingMachine(BitSet signal) {
        int size = signal.size();

        for (int i = 0; i < size; i++) {
            if (signal.get(i)) {
                switch (i) {
                    case 0:
                        System.out.println("Alex Smith");
                        break;
                    case 1:
                        System.out.println("VIP Customer");
                        break;
                    case 2:
                        System.out.println("Mary Lou");
                        break;
                    case 3:
                        System.out.println("Sim Monk");
                        break;
                    default:
                        System.out.println("Unknown person");
                        break;
                }
            }
        }
    }

}
```

<br>

# 
---
- [BitSet (Java SE7)](https://docs.oracle.com/javase/7/docs/api/java/util/BitSet.html)
- [A Guide to BitSet in Java](https://www.baeldung.com/java-bitset)
- [Java BitSet](https://www.tutorialspoint.com/java/java_bitset_class.htm)