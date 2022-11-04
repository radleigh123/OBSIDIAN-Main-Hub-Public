---
cssclass: no-m
aliases:
tags:
- C/File_Handling 
---
**[[Cfilehandling|BACK]]**

---
>[!recite|collapse no-i] Merge contents of two files

>[!aside|show-title bg-purple]+ Results
> **proto.txt**
> Hello
>
> **proto2.txt**
> World
> 
> **proto3.txt**
> Hello
> World
```C
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *fptr1, *fptr2, *fptr3;
    if ((fptr1 = fopen("proto.txt", "r")) == NULL || (fptr2 = fopen("proto2.txt", "r")) == NULL || (fptr3 = fopen("proto3.txt", "w")) == NULL) {
        printf("Error!");
        exit(1);
    }
    char ch;
    while (1) {
        ch = fgetc(fptr1);
        if (feof(fptr1)) {
            break;
        }
        fputc(ch, fptr3);
    }

    fputc('\n', fptr3);

    while (1) {
        ch = fgetc(fptr2);
        if (feof(fptr2)) {
            break;
        }
        fputc(ch, fptr3);
    }

    fclose(fptr1);
    fclose(fptr2);
    fclose(fptr3);
    return 0;
}
```
# 

<br>

---
**Sources:**
- [Merge contents of two files into third file using file handling in c programming | by Sanjay Gupta - YouTube](https://www.youtube.com/watch?v=0pGPfeDAnuY&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=28)