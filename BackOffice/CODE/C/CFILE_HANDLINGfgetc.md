---
cssclass: no-m
aliases:
---
**tags:** #C/File_Handling 
**[[Cfilehandling|BACK]]**

---
## `fgetc()`
is used to obtain input from a file single character a time. This function returns the ASCII code of the character read by the function.

>[!EXAMPLE|no-i alt-co] Syntax: `fgetc(FILE *pointer);`

>[!aside|show-title]- File Text
> Hello World
```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    FILE *fptr;
    char var1;
    if ((fptr = fopen("proto.txt", "r")) == NULL) {
        printf("Error!");
        exit(1);
    }
    while (1) {
        var1 = fgetc(fptr);
        if (var1 == EOF) { // End Of File
            break;
        }
        printf("%c", var1);
    }

    fclose(fptr);
    return 0;
}
```

# 

<br>

---
**Sources:**
- [fgetc() and fputc() in C - GeeksforGeeks](https://www.geeksforgeeks.org/fgetc-fputc-c/)