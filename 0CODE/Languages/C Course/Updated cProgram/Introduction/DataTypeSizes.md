```C
// Program to print Size of variables
#include<stdio.h>
int main(){
    int intType;
    float floatType;
    double doubleType;
    char charType;

    printf("Size of int: %lu bytes\n", sizeof(intType));
    printf("Size of float: %lu bytes\n", sizeof(floatType));
    printf("Size of double: %lu bytes\n", sizeof(doubleType));
    printf("Size of character: %lu bytes", sizeof(charType));

    return 0;
}
```