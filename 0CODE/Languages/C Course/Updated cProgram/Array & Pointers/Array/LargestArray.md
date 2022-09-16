#C #Carrays 

```C
// Program to find the largest element in an Array
#include<stdio.h>
int main(){
    int num1, data[10];
    printf("Enter number of elements(1 - 10): ");
    scanf("%d", &num1);

    for (int i = 0; i < num1; i++){
        printf("%d. Enter number: ", i + 1);
        scanf("%d", &data[i]);
    }

    // storing the largest number to data[0]
    for (int i = 0; i < num1; i++){
        if (data[0] < data[i]){
            data[0] = data[i];
        }
    }
    
    printf("Largest element: %d", data[0]);

    return 0;
}
```