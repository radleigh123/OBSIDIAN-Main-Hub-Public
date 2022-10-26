---
aliases:
---
**tags:** #C/Miscellaneous/octal #C/Variables  #C/Miscellaneous/conversion #C/Lecture  
**[[C_IMPORTANT#^1a632a|BACK]]**

---
Variables that start with zero(0) is treated as an octal value not decimal value.
`5 * 8¹  +  2 * 8⁰  =  40 + 2  =  42`

```C
int var = 052; // an octal value
printf("%d", var); // 42

// '%o' format specifier for octal values no need of conversion
printf("%o", var); // 52
```