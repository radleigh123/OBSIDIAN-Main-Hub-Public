#C #Cloop

```C
#include<stdio.h>

int main(){
    int index = 0;

    // WHILE loop checks expression before executing the code
    while (!(index == 5)){
        index++;
        printf("Index %d\n", index);
    }
    
    index = 6;
    // DO WHILE loop executes the code and then checks the expression
    do
    {
        printf("Index %d\n", index);
        index++;
    } while (index <= 5);

    return 0;
}
```