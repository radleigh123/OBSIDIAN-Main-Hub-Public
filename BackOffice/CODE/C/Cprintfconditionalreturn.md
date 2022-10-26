---
aliases:
---
**tags:** #C/stdio/printf  #C/Lecture 
**[[C_IMPORTANT#^bfb088|BACK]]**

---
## printf() conditional return
- **printf()** returns the amount of letters printed.
> `printf ("")` is considered to be 0. As nothing is printed.

```C
int i = 0;
    for (printf("one\n"); i < 3 && printf(""); i++){
        printf("Hi!\n");
    }
		// output: one
```