---
cssclass: no-m
aliases:
tags:
- C/File_Handling
- C/stdio/fread
---
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `fread()` function
reads data from the given **stream** into the array pointed to, by **pointer**.
>[!EXAMPLE|alt-co collapse no-i] **Declaration:**
> size_t `fread(void *fptr, size_t size, size_t nmemb, FILE *stream)`

>[!EXAMPLE|no-i alt-co collapse] **Parameters:**
>- `ptr` - the pointer to the array of elements
>- `size` - size in bytes of each element
>- `nmemb` - number of elements, each one with a size of **size** bytes
>- `stream` - the pointer to a FILE object that specifies an output stream

>[!aside|show-title bg-purple]+ File Text
> Hello World
```C
#include <stdio.h>
#include <string.h>

int main () {
   FILE *fp;
   char c[] = "Hello World";
   char buffer[100];

   /* Open file for both reading and writing */
   fp = fopen("file.txt", "w+");

   /* Write data to the file */
   fwrite(c, strlen(c) + 1, 1, fp);

   /* Seek to the beginning of the file */
   fseek(fp, 0, SEEK_SET); //to reset writing pointer to the beginning of the file

   /* Read and display data */
   fread(buffer, strlen(c)+1, 1, fp);
   printf("%s\n", buffer);
   fclose(fp);
   
   return(0);
}
```

# 

<br>

---
**Sources:**
- [C library function - fread() (tutorialspoint.com)](https://www.tutorialspoint.com/c_standard_library/c_function_fread.htm)
- [fwrite( ) and fread( ) to write and read array from file using file handling in c programming - YouTube](https://www.youtube.com/watch?v=6mCBmRRwt7k&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=32)