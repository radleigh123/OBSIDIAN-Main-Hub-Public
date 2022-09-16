#C #Cstrings

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