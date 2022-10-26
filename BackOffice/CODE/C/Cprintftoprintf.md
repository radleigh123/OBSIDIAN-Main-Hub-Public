---
aliases:
---
**tags:** #C/stdio/printf #C/Lecture  
**[[C_IMPORTANT#^bfb088|BACK]]**

---
## printf to printf
1st printf() function will read how many characters lies in 2nd printf() function.
```C
printf("Total chars: %d", printf("66\t")); 
//66 Total chars: 3

// 2nd printf has to be executed first, before 1st printf can get the value out of it
```