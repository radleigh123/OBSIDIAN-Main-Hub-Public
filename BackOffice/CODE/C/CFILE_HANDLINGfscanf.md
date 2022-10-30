---
aliases:
---
**tags:** #C/File_Handling 
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `fscanf()`
>[!EXAMPLE]- Syntax: `fscanf(FILE * stream, const char *format, ...);`
>- **stream** - This is the pointer to a FILE object that identifies the stream.
>- **format** - This is the C string that contains one or more of the following items
>	- A format specifier will be as **[=%[*][width][modifiers]type=]**
>	- Learn more about the [parameters](https://www.tutorialspoint.com/c_standard_library/c_function_fscanf.htm#:~:text=format%2C%20...\)-,Parameters,-stream%20%E2%88%92%20This%20is)

```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int num;
    char num1;
    FILE *fptr;
	fptr = fopen("proto.txt", "r")

    fscanf(fptr, "%d", &num);
    printf("Number: %d", num);

    fclose(fptr);
    return 0;
}
```