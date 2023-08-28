---
cssclass:
aliases:
tags:
- Java
- Java/Operators/Shift 
---
**[[JavaOperatorsShift|BACK]]**

---
## Signed Left Shift Operator `<<`
The signed right shift operator shifts all bits towards the right by a certain number of specified bits.

```java
int num1 = 8;  
int num2 = -8;  
  
System.out.println(num1 >> 2); // prints 2  
System.out.println(num2 >> 2); // prints -2

/*
In the example above, the binary number 1000 (in decimal 8) becomes 0010 after shifting the bits to the right (in decimal 2).
*/
```

```java
char hex[]={
		'0','1','2','3','4','5',
		'6','7','8','9','a','b','c',
		'd','e','f'
};

byte b=(byte) 0xf1; // 0x indicates that it is a hexadecimal number

// AND operation: 1111 & 1111 equals to 1111
// byte max value: 127
System.out.println("b = 0x" + hex [(b>>4) & 0x0f] + hex[b & 0x0f]);
```