---
aliases:
---
**tags:** #C/File_Handling 
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `fprintf()`

>[!EXAMPLE] Syntax: `fprintf(FILE * stream, const char *format, ...);`

```C
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *fptr;
    fptr = fopen("proto.txt", "w");
    
    fprintf(fptr, "%s", "Hello World");
    fprintf(fptr, "%.2lf\n", 5.22);
    fprintf(fptr, "%d\n", 52);

    fclose(fptr);
    return 0;
}
```
