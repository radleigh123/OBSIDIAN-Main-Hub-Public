---
cssclass: no-m
aliases:
tags:
- C/File_Handling 
- C/stdio/fputs 
---
**[[Cfilehandling|BACK]]**

---
>[!recite|no-i collapse] Store strings into files using [[CFILE_HANDLINGfputs|`fputs()`]]

>[!aside|show-title right]+ File Text
> Hello World
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
    printf("Enter a line of text: ");
    gets(str);

    fputs(str, fptr); // stores string into a file

    fclose(fptr);
    return 0;
}
```
# 

<br>

---
**Sources:**
- [How to store strings into files using fputs( ) in c programming | by Sanjay Gupta - YouTube](https://www.youtube.com/watch?v=pfaDXV_M7eE&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=23)