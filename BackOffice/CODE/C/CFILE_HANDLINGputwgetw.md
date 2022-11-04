---
cssclass: no-m
aliases:
tags:
- C/File_Handling
- C/stdio/putw
- C/stdio/getw
---
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `putw()` function
is used for writing a number into file.
>[!EXAMPLE|no-i alt-co collapse] **Syntax:** `putw(int num, FILE *stream);`

---
## `getw()` function
is used for reading a number into file.
>[!EXAMPLE|no-i alt-co collapse] **Syntax:** `getw(FILE *stream);`

>[!aside|right show-title]+ File Title
> file content is 12345678910
```C
#include <stdio.h>
int main() {
    FILE *fp;
    int i;
    fp = fopen("proto.txt", "w");
    for (i = 1; i <= 10; i++) {
        putw(i, fp);
    }
    fclose(fp);
    
    fp = fopen("proto.txt", "r");
    printf("file content is ");
    for (i = 1; i <= 10; i++) {
        i = getw(fp);
        printf("%d", i);
        printf("");
    }
    fclose(fp);
    return 0;
}
```

# 

<br>

---
**Sources:**
- [Explain the functions putw() and getw() in C language (tutorialspoint.com)](https://www.tutorialspoint.com/explain-the-functions-putw-and-getw-in-c-language)