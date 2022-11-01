---
cssclass: no-m
aliases:
---
**tags:** #C/File_Handling #C/stdio/fscanf 
**[[Cfilehandling|BACK]]**

---
>[!recite|no-i] Read a number from user and another number from file, Now compare them using file handling in c programming

<br>

>[!aside|show-title right] File text
> 12
```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    FILE *fptr;
    int num1, num2;
    if ((fptr = fopen("proto.txt", "r")) == NULL) {
        printf("Error!");
        exit(1);
    }
    printf("Enter a number: ");
    scanf("%d", &num1);
    fscanf(fptr, "%d", &num2);
    if (num1 == num2) {
        printf("Numbers are equal");
    } else{
        printf("Not equal");
    }

    fclose(fptr);
    return 0;
}
```