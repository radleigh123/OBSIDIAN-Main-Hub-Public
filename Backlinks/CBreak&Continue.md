#C #Cbreak #Ccontinue #Cloop 

```C
#include<stdio.h>

int main(){
    int number, sum;
    sum = 0;

    for (int i = 1; i <= 10; ++i){
        printf("Enter a number: ");
        scanf("%d", &number);

        if (number == 1){
            // code goes back to top if input value is 1
            continue;
        } else if (number < 0){
            // code stops if input value is negative
            break;
        }
           
        sum += number;
        printf("You entered: %d\n", sum);
    }

    return 0;
}
```