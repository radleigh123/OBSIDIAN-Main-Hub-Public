```C
#include<stdio.h>
int sum(int number);

int main(){
    int num1, result;
    printf("Enter a positive integer: ");
    scanf("%d", &num1);

    result = sum(num1);

    printf("Sum = %d", result);

    return 0;
}

int sum(int number){
    if (number != 0){
         // sum() function calls itself
         return number + sum(number - 1);
     } else{
        return number;
     }    
}
```