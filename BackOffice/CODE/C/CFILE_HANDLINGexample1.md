---
cssclass: no-m, co-ttl-ctr
aliases:
---
**tags:** #C/File_Handling 
**[[Cfilehandling#^a6b496|BACK]]**

---
>[!recite|no-i] Read a number, Calculate its factorial and store the result into a file using a file handling in C programming

<br>

>[!aside|show-title]+ Text file
> Factorial number: 120
> Factorial number: 24
```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    FILE *fptr;
    int num1;

    if ((fptr = fopen("proto.txt", "a")) == NULL) {
        printf("Error! Cannot find the file");
        exit(1);
    }
    printf("Enter a number: ");
    scanf("%d", &num1);
    
    for (int i = num1 - 1; i > 1; i--) {
        num1 *= i;
    }
    printf("\nFactorial number: %d", num1);
    fprintf(fptr, "Factorial number: %d\n", num1);

    fclose(fptr);
    return 0;
}
```