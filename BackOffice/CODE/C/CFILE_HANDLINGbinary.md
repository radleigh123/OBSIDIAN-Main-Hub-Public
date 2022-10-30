---
aliases:
---
**tags:** #C/File_Handling/Binary_Files 
**[[Cfilehandling|BACK]]**

---
## Binary Files
- are mostly the **.bin** files in your computer
- instead of storing data in *plain text*, they store it in binary form.
	- not easily readable
	- provides better security
	- holds higher amount of data

### Reading and Writing
Functions **`fread()`** and **`fwrite`** are used for reading from and writing to a file on the disk respectively in case of binary files. The functions take four arguments:
1. address of data to be written in the disk
2. size of data to be written in the disk
3. number of such type of data
4. pointer to the file where you want to write

>[!EXAMPLE] **Syntax:** `fwrite(addressData, sizeData, numbersData, pointerToFile);`

```C
#include <stdio.h>
#include <stdlib.h>

struct threeNum
{
    int num1, num2, num3;
};

int main()
{
    struct threeNum num;
    FILE *fptr;

    if ((fptr = fopen("students.bin", "wb")) == NULL)
    {
        printf("Error!");
        exit(1);
    }

    for (int n = 1; n < 5; ++n)
    {
        num.num1 = n;
        num.num2 = 5 * n;
        num.num3 = 5 * n + 1;
        fwrite(&num, sizeof(struct threeNum), 1, fptr);
    }
    fclose(fptr);
    fptr = fopen("students.bin", "rb");
    for (int n = 1; n < 5; ++n)
    {
        fread(&num, sizeof(struct threeNum), 1, fptr);
        printf("num1: %d\tnum2: %d\tnum3: %d\n", num.num1, num.num2, num.num3);
    }

    fclose(fptr);
    return 0;
}
```

# 

<br>

---
**Sources: **
- [Programiz](https://www.programiz.com/c-programming/c-file-input-output#:~:text=Reading%20and%20writing%20to%20a%20binary%20file)