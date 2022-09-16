#C #Cstrings 

```C
#include<stdio.h>
#include<string.h>
int main(){
    char data1[20] = "Program";
    char data2[20] = {'P', 'r', 'o', 'g', 'r', 'a', 'm', '\0'};

    // using the %zu format specifier to print size_t
    printf("Length of string data1: %zu\n", strlen(data1));
    printf("Length of string data2: %zu", strlen(data2));

    return 0;
}
```