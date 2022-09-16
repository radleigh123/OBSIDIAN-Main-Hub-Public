```C
#include<stdio.h>
int main(){
    int data[3][3] = {
        {2, 3, 5}, 
        {8, 7, 9},
        {11, 22, 33}
        };

    // prints from data[0][0] to data[2][2]
    for (int i = 0; i < 3; i++){
        for (int j = 0; j < 3; j++){
            printf("%d ", data[i][j]);
        }
        printf("\n");
    }
    return 0;
}  
```