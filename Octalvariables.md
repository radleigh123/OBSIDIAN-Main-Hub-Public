#C #Clecture #Cvariables #Coctal #Cconversion 

Variables that start with zero(0) is treated as an octal value not decimal value.
`5 * 8¹  +  2 * 8⁰  =  40 + 2  =  42`

```C
int var = 052; // an octal value
printf("%d", var); // 42

// '%o' format specifier for octal values no need of conversion
printf("%o", var); // 52
```

---
**[BACK](C_IMPORTANT)**