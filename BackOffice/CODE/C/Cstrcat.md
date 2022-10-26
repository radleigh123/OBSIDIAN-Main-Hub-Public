---
title: string concatenation function
creation-date: 2022-10-26
aliases: [concatenation]
---
**tags:** #C/Strings/strcat #C/Lecture #C/Loop #C/stdio/puts   
**[[Cstrings|BACK]]** | **[[Cstringh|<string.h>]]**

---
# `strcat()` string concatenation function
> <mark class="hltr-lightgreen">appends the content</mark> of string str2 at the end of the string str1, then it <mark class="hltr-lightgreen">returns the pointer</mark> to the resulting string str1
> > **Prototype:** `char* str1, const char* str2);`

```C
#include<stdio.h>
#include<string.h>
int main(){
	char str1[100], str2[100];
	strcpy(str1, "Welcome to ");
	strcpy(str2, "our Academy");

	strcat(str1, str2);
	printf("%s\n", str1); // Welcome to our Academy
	puts(str2);           // our Academy
	
	return 0;
}
```
### Concatenating strings without `strcat()`

```C
#include<stdio.h>
#include<string.h>
int main(){
    char str1[100] = "Programming ", str2[100] = "is awesome";
    int length;

    // store length of str1 in the length variable
    length = 0;
    while (str1[length] != '\0'){
        length++;
    }
    
    // concatenates str2 to str1
    for (int i = 0; str2[i] != '\0'; i++, length++){
        str1[length] = str2[i];
    }
    
    // terminating the str1 string
    str1[length] = '\0';

    puts(str1); // Programming is awesome

	return 0;
}
```
> **[strncat()](Cstrncat.md)** is the safer version of [[Cstrcat#`strcat()` string concatenation function|strcat]]
>>[!WARNING] #### Caution
>>- If size of str1 isn't long enough to accommodate the additional characters of str2, it will result in an **undefined behavior**. Ex.
>>	- **char str1[10], str2[20];**

# 

<br>

---
**Source:**
[String Concatenate Functions - strcat() & strncat() - YouTube](https://www.youtube.com/watch?v=beq14396XMk&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=141)