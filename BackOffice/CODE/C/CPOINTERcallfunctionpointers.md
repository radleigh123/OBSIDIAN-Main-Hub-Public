---
aliases:
---
**tags:** #C/Pointers/Functions #C/Arrays #C/Functions  
**[[Cpointerfunction2#^2500ed|BACK]]**

---
## Designing a calculator program using function pointers
```C
// https://www.youtube.com/watch?v=wQ-gWwKKeP4&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=150


#include <stdio.h>
#define ops 4

double sum(double num1, double num2){
    return num1 + num2;
}

double diff(double num1, double num2){
    return num1 - num2;
}

double prod(double num1, double num2){
    return num1 * num2;
}

double quo(double num1, double num2){
    return num1 / num2;
}


int main(){
    double (*ptrfunc[ops])(double, double) = {sum, diff, prod, quo};
    int choice;
    double num1, num2;
  
    printf("[0] for Addition, [1] for Subtraction, [2] for Multiplication, [3] for Division\n");

    do{
        printf("Enter your choice: ");
        scanf("%d", &choice);
    } while ((choice < 0 || choice > 3) && (choice > 3 || choice < 0));

    printf("Enter two numbers: ");
    scanf("%lf %lf", &num1, &num2);

    printf("\n%.2lf", ptrfunc[choice](num1, num2));
    return 0;
}
```