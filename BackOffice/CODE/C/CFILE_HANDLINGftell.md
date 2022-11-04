---
cssclass: no-m
aliases:
tags:
- C/File_Handling
- C/stdio/ftell
---
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `ftell()` function
returns the current file position of the specified stream with respect to the starting of the file.
>[!EXAMPLE|alt-co no-i] **Syntax:**
> `long int ftell(FILE *stream)`

>[!aside|show-title bg-purple]+ File text
> Hello World
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

    num = ftell(fptr);
    printf("Position of File Pointer %d", num); // 0

    fseek(fptr, 6, SEEK_SET);
    num = ftell(fptr);
    printf("\nNew Position of File Pointer %d", num); // 6

    fclose(fptr);
    return 0;
}
```

# 

<br>

---
**Sources:**
- [How to use ftell( ) function in file handling in c programming | by Sanjay Gupta - YouTube](https://www.youtube.com/watch?v=GQQySwSIALU&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=37)