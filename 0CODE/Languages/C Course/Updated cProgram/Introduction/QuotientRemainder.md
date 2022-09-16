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