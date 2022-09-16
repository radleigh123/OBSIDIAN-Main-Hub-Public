```C
// Program using the Long keyword
#include<stdio.h>
int main(){
    int intType;
    long longintType; // equivalent to long int longintType;
    long long long2intType; // equivalent to long long int long2intType;
    float floatType;
    double doubleType;

    printf("Size of int: %lu bytes\n", sizeof(intType));
    printf("Size of long int: %lu bytes\n", sizeof(longintType));
    printf("Size of long long int: %lu bytes\n\n", sizeof(long2intType));
    printf("Size of float: %lu bytes\n", sizeof(floatType));
    printf("Size of double: %lu bytes\n", sizeof(doubleType));
    
    return 0;
}
```