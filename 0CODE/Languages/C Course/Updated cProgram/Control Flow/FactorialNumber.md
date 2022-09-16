```C
// Program to find the factorial of a number
#include<stdio.h>
int main(){
    int num1;
    unsigned long long fact = 1;
    printf("Enter an integer: ");
    scanf("%d", &num1);

    // shows error if the user enters a negative integer
    if (num1 < 0){
        printf("Error! Factorial of a negative number doesn't exist");
    } else
    {
        for (int i = 1; i <= num1; i++){
            fact *= i;
        }
        printf("Factorial of %d: %llu", num1, fact);
    }
    
    return 0;
}
```