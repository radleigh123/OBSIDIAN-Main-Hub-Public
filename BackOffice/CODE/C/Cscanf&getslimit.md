---
aliases:
---
**tags:** #C/Strings #C/Lecture #C/stdio/scanf #C/stdio/gets 
**[[CSTRINGreadingstring|BACK]]** | **[[C_IMPORTANT|IMPORTANT]]**

---
## `scanf()` & `gets()` limit
Both, `gets()` and `scanf(`) functions have no way to detect when the character is full. Both of them never checks the maximum limit of input character. By using **[%.ns](Cns.md)**, scanf()  has the way to set the limit for the number of characters to be stored in the character array.

```C
char a[10];
printf("Enter the string:\n");
scanf("%9s", a); // Youaremostwelcome
printf("%s", a);

/*
Youaremos
*/
```