## Calloc
#Cmemoryallocation #Cpointers #Cconversion #Ccalloc

```C
#include<stdio.h>
#include<stdlib.h>

int main(){
    int num1 = 50;
    float *pointer;

    printf("Size of Float: %lu", sizeof(float));

    // allocates contiguous space in memory for 50 elements of type FLOAT
    // 200 bytes of memory allocated
    pointer = (float*) calloc(num1, sizeof(float));

    return 0;
}
```

## CallocFree
#Cmemoryallocation #Cfree

```C
// Program to calculate the sum of n numbers entered by the user
#include<stdio.h>
#include<stdlib.h>

int main(){
    int *pointer, num1, sum = 0;
    int i;
    printf("Enter number of elements: ");
    scanf("%d", &num1);

    // allocating memory of number of num1 times 4bytes of INT
    pointer = (int*) calloc(num1, sizeof(int));
    if (pointer == NULL){
        printf("ERROR! memory not allocated.");
    }

    printf("Enter elements: ");
    for (i = 0; i < num1; i++){
        scanf("%d", &pointer[i]);
        sum += *(pointer + i);
    }
    
    printf("Sum = %d", sum);
    free(pointer);
    
    return 0;
}
```