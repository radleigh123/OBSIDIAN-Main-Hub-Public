---
cssclass: no-m
aliases:
tags:
- C/File_Handling
- C/stdio/rewind
---
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `rewind()` function
sets the file position to the beginning of the file of the given **stream**.
>[!EXAMPLE|alt-co no-i collapse] **Syntax:** `void rewind (FILE *stream)`

>[!aside|show-title bg-purple]+ File Text
> Hello World
```C
#include <stdio.h>

int main () {
   char str[] = "Hello World";
   FILE *fp;
   int ch;

   /* First let's write some content in the file */
   fp = fopen( "file.txt" , "w" );
   fwrite(str , 1 , sizeof(str) , fp );
   fclose(fp);

   fp = fopen( "file.txt" , "r" );
   while(1) {
      ch = fgetc(fp);
      if( feof(fp) ) {
         break ;
      }
      printf("%c", ch);
   }
   rewind(fp);
   printf("\n");
   while(1) {
      ch = fgetc(fp);
      if( feof(fp) ) {
         break ;
      }
      printf("%c", ch);
     
   }
   fclose(fp);

   return(0);
}
```
# 

<br>

---
**Sources:**
- [C library function - rewind() (tutorialspoint.com)](https://www.tutorialspoint.com/c_standard_library/c_function_rewind.htm)
- [Use of rewind( ) function using w+ mode in file handling in c programming | by Sanjay Gupta - YouTube](https://www.youtube.com/watch?v=RPxeqg6MGno&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=32)