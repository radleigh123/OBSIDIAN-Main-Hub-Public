---
aliases:
tags:
- C/File_Handling 
- C/stdio/feof
---
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `feof()` function
tests the end-of-file indicator for the given stream.
>[!EXAMPLE|alt-co collapse no-i] **Declaration:** `int feof(FILE *stream)`
>**Parameters:** `stream` - this is the pointer to a FILE

>[!aside|right show-title]+ File Text
> Hello World
```C
#include <stdio.h>

int main () {
   FILE *fp;
   fp = fopen("file.txt","r");
   if(fp == NULL) {
      perror("Error in opening file");
      return(-1);
   }

   char ch;
   while(1) {
      c = fgetc(fp);
      if( feof(fp) ) { 
         break ;
      }
      printf("%c", c);
   }
   fclose(fp);
   
   return(0);
}
```
# 

<br>

---
**Sources:**
- [C library function - feof() (tutorialspoint.com)](https://www.tutorialspoint.com/c_standard_library/c_function_feof.htm)