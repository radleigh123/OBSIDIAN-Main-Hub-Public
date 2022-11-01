---
cssclass: no-m
aliases:
---
**tags:** #C/File_Handling #C/stdio/fscanf 
**[[Cfilehandling|BACK]]**

---
>[!recite|no-i] How to read multiple numbers from file

<br>

>[!aside|show-title bg-purple]- Text file
> 1
> 2
> 3
> 4
> 5
> 6
> 7
> 8
> 9
> 10
```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    FILE *fptr;
    int num1;

    if ((fptr = fopen("proto.txt", "r")) == NULL) {
        printf("Error!");
        exit(1);
    }
    for (int i = 1; i <= 10; i++) {
        fscanf(fptr, "%d", &num1);
        printf("%d ", num1);
    }

    fclose(fptr);
    return 0;
}
```
