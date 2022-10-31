---
cssclass: no-m
aliases:
---
**tags:** #C/File_Handling 
**[[Cfilehandling#^a6b496|BACK]]**

---
>[!recite|no-i] Print table of a number on output screen as well as in file using file handling in C programming

>[!aside|show-title bg-purple]+ Text File
> 8
> 16
> 24
> 32
> 40
> 48
> 56
> 64
> 72
> 80

<br>

```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    FILE *fptr;
    int num1;
    if ((fptr = fopen("proto.txt", "w")) == NULL)
    {
        printf("Error!");
        exit(1);
    }
    printf("Enter a number: ");
    scanf("%d", &num1);
    for (int i = 1; i <= 10; i++)
    {
        printf("%d ", num1 * i);
        fprintf(fptr, "%d ", num1 * i);
    }

    fclose(fptr);
    return 0;
}
```