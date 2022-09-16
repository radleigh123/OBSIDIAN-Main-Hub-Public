#C #Carrays 

```C
// Program to store numbers and calculate average using arrays
#include<stdio.h>
int main(){
    int num1;
    double num[100], sum = 0.0, avg;

    printf("Enter the numbers of elements: ");
    scanf("%d", &num1);

    while (num1 > 100 || num1 < 1){
        printf("Error! number should be in range of (1 - 100).\n");
        printf("Enter the number again: ");
        scanf("%d", &num1);
    }
    
    for (int i = 0; i < num1; i++){
        printf("%d. Enter number: ", i + 1);
        scanf("%lf", &num[i]);
        sum += num[i];
    }
    
    avg = sum / num1;
    printf("Sum: %.2lf\tAverage: %.2lf", sum, avg);

    return 0;
}
```