---
aliases:
---
**tags:** #C/Miscellaneous/conversion #C/Variables #C/Miscellaneous/conversion #C/Miscellaneous/hexadecimal #C/Lecture  
**[[C_IMPORTANT#^eb9dae|BACK]]**

---
Placing `0x` in front of any value is treated as a Hexadecimal value.
```C
int var = 0x43FF;
// '%x' format specifier for hexadecimal values
printf("%x", var); // 43ff

// if '%X' ALL CAPS is used
printf("%X", var); // 43FF

// conversion of hexadecimal to decimal
printf("%d", var); // 17407
```