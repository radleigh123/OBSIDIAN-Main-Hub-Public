---
aliases:
---
**tags:** #C/Miscellaneous/Data_Type #C/Character 
**[[CCODES|BACK]]**

---
## Datatype Sizes
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

## Long Int
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

# Quotient Remainder
```C
// Program to compute Quotient and Remainder
#include<stdio.h>
int main(){
    int dividend, divisor, quotient, remainder;
    printf("Enter dividend: ");
    scanf("%d", &dividend);
    printf("Enter divisor: ");
    scanf("%d", &divisor);

    // Computes quotient
    quotient = dividend / divisor;

    // Computes remainder
    remainder = dividend % divisor;

    printf("Quotient: %d\tRemainder: %d", quotient, remainder);
    
    return 0;
}
```

# ASCII Values
```C
// Program to print ASCII value
#include<stdio.h>
int main(){
    char char1;
    printf("Enter a character: ");
    scanf("%c", &char1);

    // %c displays the actual character
    // %d displays the integer value of a character
    printf("\nASCII value of '%c': %d", char1, char1);

    return 0;
}
```