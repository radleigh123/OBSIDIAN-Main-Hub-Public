---
aliases:
cssclass: 
---
**tags:** #C/File_Handling 
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `fscanf()`
>[!EXAMPLE|no-i]- Syntax: `fscanf(FILE * stream, const char *format, ...);`
>- **stream** - This is the pointer to a FILE object that identifies the stream.
>- **format** - This is the C string that contains one or more of the following items
>	- A format specifier will be as **[=%[*][width][modifiers]type=]**
>	- Learn more about the [parameters](https://www.tutorialspoint.com/c_standard_library/c_function_fscanf.htm#:~:text=format%2C%20...\)-,Parameters,-stream%20%E2%88%92%20This%20is)

>[!aside|show-title]+ Text file
> K
> 25
> 5.26
> Keane

```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    char var1;
    int var2;
    double var3;
    char var4[10];
    FILE *fptr;
	fptr = fopen("proto.txt", "r");

    fscanf(fptr, "%c", &var1);
    fscanf(fptr, "%d", &var2);
    fscanf(fptr, "%lf", &var3);
    fscanf(fptr, "%s", var4);
    
    printf("Character: %c\n", var1);
    printf("Number: %d\n", var2);
    printf("Floating Number: %.3lf\n", var3);
    printf("String: %s", var4);

    fclose(fptr);
    return 0;
}
```
