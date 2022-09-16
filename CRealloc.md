## Realloc
#C #Cmemoryallocation #Crealloc #Cconversion #Cpointers 

```C
#include<stdio.h>
#include<stdlib.h>

int main(){
    int *pointer, num1, num2;
    
    printf("Enter a size: ");
    scanf("%d", &num1);

    // allocating memory of num1 value times 4bytes of INT
    pointer = (int*) malloc(num1 * sizeof(int));

    printf("Addresses of previously allocated memory:\n");
    for (int i = 0; i < num1; i++){
        printf("%pc\n", pointer + i);
    }

    printf("\nEnter the new size: ");
    scanf("%d", &num2);

    // reallocating the memory
    // of NEW num2 value times 4bytes of INT
    pointer = (int*) realloc(pointer, num2 * sizeof(int));

    printf("Addresses of newly allocated memory:\n");
    for (int i = 0; i < num2; i++){
        printf("%pc\n", pointer + i);
    }
    
    free(pointer);
    
    return 0;
}
```