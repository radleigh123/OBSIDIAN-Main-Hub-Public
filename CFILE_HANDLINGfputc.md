---
cssclass: 
aliases:
---
**tags:** #C/File_Handling #C/stdio/fputc 
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `fputc()` function
writes a character (*an unsigned char*) specified by the argument **char** to the specified stream and advances the position indicator for the stream
**Declaration:** `int fputc(int char, FILE *stream)`
**Parameters:**
- [F]  **<u>char</u>** 
	- the character to be written
- [O]  **<u>stream</u>**
	- the pointer to a FILE object

>[!aside|show-title]+ File text
> Hello World
```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    char str[10];
    FILE *fptr;
    if ((fptr = fopen("proto.txt", "w")) == NULL) {
        printf("Error!");
        exit(1);
    }
    
    printf("Enter name: ");
    scanf("%[^\n]s", &str); // Hello World
    // until newline (ENTER) is used, scanf will stop reading
    for (int i = 0; str[i] != '\0'; i++) {
        fputc(str[i], fptr);
    }

    fclose(fptr);
    return 0;
}
```

# 

<br>

---
**Sources:**
- [How to store characters using fputc( ) function into files in c programming | by Sanjay Gupta - YouTube](https://www.youtube.com/watch?v=QBiWy0txd08&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=20)