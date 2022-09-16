#C #Carrays #Carraypointer 

```C
#include<stdio.h>
int main(){
    int data[5];
    printf("Enter elements:\n");
    for (int i = 0; i < 5; i++){
        printf("%d. ", i + 1);
        scanf("%d", data + i);
    }

    printf("\nEntered elements:\n");
    for (int i = 0; i < 5; i++){
        printf("%d. %d\n", i + 1, *(data + i));
    }
    
    return 0;
}
```