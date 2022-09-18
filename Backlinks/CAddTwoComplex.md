#C #Cstructures #Cfunctions 

```C
// Program to add two complex numbers by passing structure to a function
#include<stdio.h>
typedef struct Complex{
    double real, imag;
} complex;

complex add(complex n1, complex n2);

int main(){
    complex n1, n2, result;

    printf("For 1st complex\n");
    printf("Enter the real and imaginary parts: ");
    scanf("%lf%lf", &n1.real, &n1.imag);
    printf("For 2nd complex\n");
    printf("Enter the real and imaginary parts: ");
    scanf("%lf%lf", &n2.real, &n2.imag);

    result = add(n1, n2);

    printf("Sum = %.1lf + %.1lf", result.real, result.imag);
    return 0;
}

complex add(complex n1, complex n2){
    complex temp;
    temp.real = n1.real + n2.real;
    temp.imag = n1.imag + n2.imag;

    return temp;
}
```