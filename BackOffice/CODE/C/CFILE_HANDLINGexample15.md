---
cssclass: no-m
aliases:
tags:
- C/File_Handling
---
**[[Cfilehandling|BACK]]**

---
>[!recite|alt-co collapse no-i] Find out size of file
```C
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *fptr;
    if ((fptr = fopen("proto.txt", "r")) == NULL) {
        printf("Error!");
        exit(1);
    }
    int num;
    fseek(fptr, 0, SEEK_END);
    num = ftell(fptr);
    printf("Size of file: %d", num);

    fclose(fptr);
    return 0;
}
```
# 

<br>

---
**Sources:**
- [How to find out size of file using file handling in c programming | by Sanjay Gupta - YouTube](https://www.youtube.com/watch?v=CYpp9OduyJM&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=38)