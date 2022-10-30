---
title: strncat() function
creation-date: 2022-10-26
aliases:
---
**tags:** #C/Strings/strncat #C/Lecture  
**[[Cstrings|BACK]]** | **[[Cstringh|<string.h>]]**

---
# `strncat()` function
> is the<mark class="hltr-lightgreen"> safer version</mark> of strcat
> it appends the limited number of characters specified by the third argument passed to it.
> > **Note:** `strncat()` automatically adds NULL character at the end of the resultant string

```C
#include <stdio.h>
#include <string.h>
int main(){
    char str1[5], str2[100];
    strcpy(str1, "He");
    strcpy(str2, "llo!");

    // 
    strncat(str1, str2, sizeof(str1) - strlen(str1) - 1);
    printf("%s", str1); // Hell

    return 0;
}
```
![[Pasted image 20221001171917.png|450]]