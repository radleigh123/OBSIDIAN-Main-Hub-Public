#C #Cswitch

```C
#include<stdio.h>
#include<stdlib.h>

int main(){
    int num1, num2, result;
    char operator;

    printf("Enter 1st number: ");
    scanf("%d", &num1);
    printf("Enter 2nd number: ");
    scanf("%d", &num2);
    // input specifiec char to execute codes on switch
    printf("Enter an operator: ");
    scanf(" %c", &operator);

    system("cls");

    // executes a certain code depending on the input char
    switch (operator){
    case '+':
        result = num1 + num2;
        printf("%d + %d = %d", num1, num2, result);
        break;
    case '-':
        result = num1 + num2;
        printf("%d - %d = %d", num1, num2, result);
        break;
    case '*':
        result = num1 * num2;
        printf("%d * %d = %d", num1, num2, result);
        break;
    case '/':
        result = num1 / num2;
        printf("%d / %d = %d", num1, num2, result);
        break;
    default:
        printf("Error! Please enter a valid operator SEARCH GOOGLE PLEASE");
    }

    return 0;
}
```