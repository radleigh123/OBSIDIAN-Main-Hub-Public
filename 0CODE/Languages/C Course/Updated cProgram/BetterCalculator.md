```C
#include<stdio.h>
#include<string.h>
double calcFunction(double NUMBER_DATA[], char OPER);

int main(){
    double numberData[5];
    char oper;
    for (int i = 0; i < 5; i++){
        printf("-> ");
        scanf("%lf", &numberData[i]);
    }
    printf("\nChoose an operand(+,-,x,÷): ");
    scanf(" %c", &oper);

    // the variables here are passed unto the calcFunction
    printf("\nResults: %.lf", calcFunction(numberData, oper));

    return 0;
}

// ALL CAPS initializing variables in order to be recognized
double calcFunction(double NUMBER_DATA[], char OPER){
    double result = 0.0;

    // switch is used to perform the specific function user wanted to do
    switch (OPER){
    case '+':
        for (int i = 0; i < 5; i++){
            result += NUMBER_DATA[i];
        }
        break;
    case '-':
        result = NUMBER_DATA[0];
        for (int i = 1; i < 5; i++){
            result -= NUMBER_DATA[i];
        }
        break;
    case '*':
        result = 1.0;
        for (int i = 0; i < 5; i++){
            result *= NUMBER_DATA[i];
        }
        break;
    case '/':
        result = NUMBER_DATA[0];
        for (int i = 1; i < 5; i++){
            result /= NUMBER_DATA[i];
        }
        break;
    default:
        printf("Error! Not quite the correct operand.");
        exit(1);
    }

    return result;
}
```