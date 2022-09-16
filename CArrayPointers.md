#C #Cpointers #Carrays 

```C
#include<stdio.h>
int main(){
    int data[5] = {1, 2, 3, 4, 5};
    printf("Address of array data: %p\n\n", data);

    // FOR ADDRESS
    // &data[0] = data;        &data[1] = data + 1;

    // FOR VALUE
    // data[0] = *data;        data[1] = *(data + 1);

    for (int i = 0; i < 5; i++){
        printf("Address of data[%d]: %p\t", i, &data[i]);
        printf("Value of data[%d]: %d\n", i, data[i]);
    }
    
    printf("\nADDRESS\t\t\t\tVALUE\n");

    printf("&data[0]: %p\t", &data[0]); // ADDRESS
    printf("data[0]: %d\n", data[0]); // VALUE

    printf("&data[1]: %p\t", &data[1]); // ADDRESS
    printf("data[1]: %d\n", data[1]); // VALUE

    printf("\n--------------------OR-----------------------\n\n");

    printf("data:\t  %p\t", data); // ADDRESS
    printf("*data:\t     %d\n", *data); // VALUE

    printf("data + 1: %p\t", data + 1); // ADDRESS
    printf("*(data + 1): %d", *(data +1)); // VALUE

    return 0;
}
```