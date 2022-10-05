#C #Cstrings #Cstrlen
# String Length function
> - is used to <mark class="hltr-lightblue">determine the length</mark> of the given string.
>> **Prototype:** `size_t strlen(const char* str);`
>> **Note:** we should pass the pointer to the first character of the string whose length we want to determine. And as a <mark class="hltr-lightgreen">result, it returns the length of the string</mark>
```C
#include <string.h>
    char data1[100] = {'H', 'e', 'l', 'l', 'o', '\0'};
    char *ptr = "Hello";
    
    // using the %zu format specifier to print size_t
    printf("%zu\n", strlen(data1)); // 5
    // it calculates the LENGTH of the string and not the length of the array

    printf("%d", (int)strlen(ptr)); // 5
```
> `size_t` is an unsigned integer type of at least 16 bits.


# 
---
**[[C]]**
**[[Cstringh]]**