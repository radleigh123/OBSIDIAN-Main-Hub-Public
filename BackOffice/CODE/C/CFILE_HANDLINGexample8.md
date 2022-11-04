---
cssclass: 
aliases:
---
**tags:** #C/File_Handling #C/stdio/fgetc 
**[[Cfilehandling|BACK]]**

---
>[!recite|no-i collapse] Display *source code* as output on output screen
```C
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *fptr;
    if ((fptr = fopen("PROTO1.c", "r")) == NULL) {
        printf("Error!");
        exit(1);
    }
    char ch;
    while (1) {
        ch = fgetc(fptr);
        if (ch == EOF) {
            break;
        }
        printf("%c", ch);
    }

    fclose(fptr);
    return 0;
}
```
# 

<br>

---
**Source:**
- [Display source code as output on output screen in c programming | by Sanjay Gupta - YouTube](https://www.youtube.com/watch?v=RvQj5epLpJ0&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=19)