---
cssclass: 
aliases:
---
**tags:** #C/File_Handling #C/stdio/fgetc 
**[[Cfilehandling|BACK]]**

---
>[!recite|no-i collapse] Count characters and words from file
```C
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *fptr;
    if ((fptr = fopen("proto.txt", "r")) == NULL) {
        printf("Error!");
        exit(1);
    }
    char ch;
    int num1, num2;
    num1 = num2 = 0;

    while (1) {
        ch = fgetc(fptr);
        if (ch == EOF) {
            break;
        }
        num1++;
        if (ch == ' ' || ch == '\n') {
            num2++;
        }
    }

    printf("Total characters: %d", num1);
    printf("\nTotal words: %d", num2 + 1);
    fclose(fptr);
    return 0;
}
```
# 

<br>

---
**Sources:**
- [Count characters and words from file in C language | C programming video tutorials series - YouTube](https://www.youtube.com/watch?v=jGjsa8_G_NU&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=17)