---
aliases:
---
**tags:** #C/File_Handling 
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `fseek()` function
- If you have many records inside a file and <mark class="hltr-blue">need to access a record at a specific position</mark>, you need to loop through all the records before it to get the record.
	- This will waste a lot of memory and operation time. An easier way to get to the required data can be achieved using **`fseek()`**.

>[!EXAMPLE] Syntax: `fseek(FILE * stream, long int offset, int whence);`
>- First parameter stream is the pointer to the file
>- Second parameter is the position of the record to be found
>- Third parameter specifies the location where the offset starts.

**<center>Different `whence` in fseek()</center>**

| **<center>Whence</center>** | **<center>Meaning</center>**                      |
| --------------------------- | ------------------------------------------------- |
| **`SEEK_SET`**              | Starts the offset from the beginning of the file. |
| **`SEEK_END`**              | Starts the offset from the end of the file.       |
| **`SEEK_CUR`**              | Starts the offset from the current location of the cursor in the file.                                                  |

>[!EXAMPLE]-
>```C
>#include <stdio.h>
>#include <stdlib.h>
>
> struct threeNum {
>    int num1, num2, num3;
> };
>
> int main() {
>    struct threeNum num;
>    FILE *fptr;
>
>    if ((fptr = fopen("students.bin", "rb")) == NULL) {
>        printf("Error!");
>        exit(1);
>    }
>
>    fseek(fptr, -sizeof(struct threeNum), SEEK_END);
>
>    for (int i = 1; i < 5; ++i)
>    {
>        fread(&num, sizeof(struct threeNum), 1, fptr);
>        printf("num1: %d\tnum2: %d\tnum3: %d\n", num.num1, num.num2, num.num3);
>        fseek(fptr, -2 * sizeof(struct threeNum), SEEK_CUR);
>   }
> 
>    fclose(fptr);
>    return 0;
> }
>```

# 

<br>

---
**Sources:**
- [Programiz](https://www.programiz.com/c-programming/c-file-input-output#:~:text=Example%205%3A-,fseek(),-%23include%20%3Cstdio)