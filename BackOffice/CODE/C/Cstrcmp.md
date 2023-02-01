---
title: string comparison function
creation-date: 2022-10-26
aliases: [string comparison]
---
**tags:** #C/Strings/strcmp #C/Lecture  
**[[Cstrings|BACK]]** | **[[Cstringh|<string.h>]]**

---
#  `strcmp()` String Comparison function
 > **Prototype:** `int strcmp(const char* s1, const char* s2);`
> ![[Pasted image 20221001172546.png|300]]
```C
#include<stdio.h>
#include<string.h>
int main(){
    char str1[] = "abcd", str2[] = "abCd", str3[] = "abcd";
    int result;

    // comparing strings str1 and str2\
    // str1 and str2 are not equal. Hence, the result is a non-zero integer.
    result = strcmp(str1, str2);
    printf("strcmp(str1, str2) = %d\n", result);

    // comparing strings str1 and str3
    // str1 and str3 are equal. Hence, the result is 0.
    result = strcmp(str1, str3);
    printf("strcmp(str1, str3) = %d", result);

    return 0;
}
```
>[!WARNING] **Attention:** [ASCII Character set](ASCII%20codes.md)

### Caution
`strcmp()` considers s1 < s2 if either one of the following conditions is satisfied:
- When the first i characters in s1 and s2 are some and (i + 1)st characters of s1 is less than that of s2.
	- **[Example 1](CSTRCMPex1.md)**
	- **[Example 2](CSTRCMPex2.md)**
	- **[Example 3](CSTRCMPex3.md)**
	- **[Example 4](CSTRCMPex4.md)**
- [All characters of s1 match s2. is shorter than s2](CSTRCMPex5.md)