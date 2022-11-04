---
cssclass: 
aliases:
---
**tags:** #C/File_Handling #C/stdio/fgetc 
**[[Cfilehandling|BACK]]**

---
>[!recite|no-i collapse] Count number of characters in a file using fgetc()

```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    char ch;
    int count = 0;
    FILE *fptr;
    if ((fptr = fopen("proto.txt", "r")) == NULL) {
        printf("Error!");
        exit(1);
    }
    
    while (1) {
        ch = fgetc(fptr);
        if (ch == EOF) {
            break;
        }
        ++count;
        printf("%c", ch);
    }
    
    printf("Total Characters: %d", count);
    fclose(fptr);
    return 0;
}
```

# 

<br>

---
**Sources:**
- [How to count number of characters in a file using fgetc( ) in c programming | by Sanjay Gupta - YouTube](https://www.youtube.com/watch?v=2Qr2-erTmfQ&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=16)