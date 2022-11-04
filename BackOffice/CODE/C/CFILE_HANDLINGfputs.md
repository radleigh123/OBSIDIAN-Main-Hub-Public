---
cssclass: no-m
aliases:
tags:
- C/File_Handling
- C/stdio/fputs
---
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## C `fputs()` function
writes a line of characters into file. It outputs string to a stream.
>[!EXAMPLE|no-i alt-co] **Syntax:** `int fputs(const char *s, FILE *stream)`

>[!aside|show-title right]+ File Text
> hello c programming
```C
#include<stdio.h>  
#include<conio.h>  
void main(){  
	FILE *fp;  
	clrscr();  
	  
	fp=fopen("myfile2.txt","w");  
	fputs("hello c programming",fp);  
	  
	fclose(fp);  
	getch();  
}  
```

# 

<br>

---
**Sources:**
- [fputs() and fgets() in C - javatpoint](https://www.javatpoint.com/fputs-fgets-in-c)