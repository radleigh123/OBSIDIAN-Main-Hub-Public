---
cssclass: 
aliases:
---
**tags:** #C/File_Handling #C/stdio/fgetc #C/stdio/fputc 
**[[Cfilehandling|BACK]]**

---
>[!recite|no-i collapse] Copy contents of a file into another using [[CFILE_HANDLINGfgetc|`fgetc`]] and [[CFILE_HANDLINGfputc|`fputc`]]
```C
#include <stdio.h>
#include <stdlib.h>

int main() {
	char ch;
    FILE *fptr1, *fptr2;
    if ((fptr1 = fopen("proto.txt", "r")) == NULL || (fptr2 = fopen("proto2.txt", "w")) == NULL) {
        printf("Error!");
        exit(1);
    }
    
    char ch;
    while (1) {
        ch = fgetc(fptr1);
        if (ch == EOF) {
            break;
        }
        fputc(ch, fptr2);
    }

    fclose(fptr1);
    fclose(fptr2);
    return 0;
}
```
# 

<br>

---
**Sources:**
- [Copy contents of a file into another using fgetc( ) and fputc( ) in c programming - YouTube](https://www.youtube.com/watch?v=S6eYzS0jlfg&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=18)