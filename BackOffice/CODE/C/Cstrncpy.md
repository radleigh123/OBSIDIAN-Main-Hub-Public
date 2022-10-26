---
title: strncpy() function
creation-date: 2022-10-26
aliases:
---
**tags:** #C/Strings #C/Lecture #C/Strings/strncpy  
**[[Cstrings|BACK]]** | **[[Cstringh|<string.h>]]**

---
# `strncpy()` function
**Prototype:** `strncpy(destination, soruce, sizeof(destination))`
```C
#include<string.h>

char str1[] = "Hello";
char str2[4];

strncpy(str2, str1, sizeof(str2));
printf("%s", str2); // Hell
```
<br>

### Caution:
![[Pasted image 20220930000325.png|450]]

# 

<br>

---
**Relations:**
**[[Cstrcpy]]**