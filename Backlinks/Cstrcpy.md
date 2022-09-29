#C #Cstrings #Cputs 
# String Copy function
> is used to copy a string pointed by <mark class="hltr-lightred">source</mark> (including NULL character) to the <mark class="hltr-lightgreen">destination</mark> (character array)
> >**Prototype**: `char* strcpy(char* destination, const char* source)`
> >**Note:** It isn't modified, that's why the <mark class="hltr-lightred"> source is constant</mark>
```C
#include<string.h>

    char str1[10] = "Hello";
    char str2[10];
    char str3[10];

    // copying str1 to str2, and then to str3
    strcpy(str3, strcpy(str2, str1));
    
    printf("%s %s", str2, str3); // Hello Hello
```

> **strcpy()** returns the pointer to the first character of the string which is copied in the destination.
> Hence if we use **%s**, then whole string will be printed on the screen

<br>

### Caution
- In the call to `strcpy(str, str2)`, there is no way the strcpy will check whether the string by str2 will fit in str1
- If the length of the string pointed by str2 is greater than the length of the character array str2 then it will be an undefined behavior.
- To avoid this we can call **[strncpy() function](Cstrncpy.md)**

# 
---
**[[C]]**
**[[Cstringh]]**

<br>

**Link:**
[C String Library and String Copy Function - strcpy() - YouTube](https://www.youtube.com/watch?v=DOPs6c0f4Ek&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=138)
