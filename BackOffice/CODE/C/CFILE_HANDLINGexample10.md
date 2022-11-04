---
aliases:
tags:
- C/File_Handling
- C/stdio/fputs
---
**[[Cfilehandling|BACK]]**

---
>[!recite|collapse no-i] Store 3 lines of text in file using [[CFILE_HANDLINGfputs|`fputs()`]]

>[!aside|show-title right bg-purple]+ File Text
> Hello World
> C program
> 20 Earths
```C
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *fptr;
    if ((fptr = fopen("proto.txt", "w")) == NULL) {
        printf("Error!");
        exit(1);
    }
    char str[50];
    for (int i = 1; i <= 3; i++) {
        printf("Enter %dline: ", i);
        gets(str);
        fputs(str, fptr);
        fputs("\n", fptr);
    }

    fclose(fptr);
    return 0;
}
```
# 

<br>

---
**Sources:**
- [Store multiple lines of text into file using fputs( ) in c programming | by Sanjay Gupta - YouTube](https://www.youtube.com/watch?v=sRfObIsYPuo&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=25)