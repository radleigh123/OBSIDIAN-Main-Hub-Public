---
cssclass: no-m
aliases:
tags:
- C/File_Handling
- C/stdio/fgets
---
**[[Cfilehandling#Operators/Functions for file handling|BACK]]**

---
## `fgets()` function
reads a line of characters from file. It gets string from a stream.
>[!EXAMPLE|alt-co no-i] **Syntax:** `char* fgets(char *s, int n, FILE *stream)`

>[!aside|show-title right] File Text
> hello c programming
```C
#include<stdio.h>  
#include<conio.h>  
void main(){  
	FILE *fp;  
	char text[300];  
	clrscr();  
	  
	fp=fopen("myfile2.txt","r");  
	printf("%s",fgets(text,200,fp));  
	  
	fclose(fp);  
	getch();  
}
```
# 

<br>

---
**Sources:**
- [fputs() and fgets() in C - javatpoint](https://www.javatpoint.com/fputs-fgets-in-c)