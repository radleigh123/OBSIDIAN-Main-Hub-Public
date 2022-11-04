---
aliases:
tags:
- C/File_Handling
- C/stdio/fwrite
---
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `fwrite()` function
writes data from the array pointed to, by **pointer** to the given **stream**.
>[!EXAMPLE|no-i alt-co collapse] **Declaration:**
> size_t `fwrite(const void *ptr, size_t size, size_t nmemb, FILE *stream)`

>[!EXAMPLE|no-i alt-co collapse] **Parameters:**
>- `ptr` - the pointer to the array of elements
>- `size` - size in bytes of each element
>- `nmemb` - number of elements, each one with a size of **size** bytes
>- `stream` - the pointer to a FILE object that specifies an output stream

>[!aside|show-title bg-purple]+ File Text
> Hello World
```C
#include<stdio.h>

int main () {
   FILE *fp;
   char str[] = "Hello World";

   fp = fopen( "file.txt" , "w" );
   fwrite(str , 1 , sizeof(str) , fp );

   fclose(fp);
  
   return(0);
}
```

# 

<br>

---
**Sources:**
- [C library function - fwrite() (tutorialspoint.com)](https://www.tutorialspoint.com/c_standard_library/c_function_fwrite.htm)
- [fwrite( ) and fread( ) to write and read array from file using file handling in c programming - YouTube](https://www.youtube.com/watch?v=6mCBmRRwt7k&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=32)