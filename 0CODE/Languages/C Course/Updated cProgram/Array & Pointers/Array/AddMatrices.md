#C #Carrays #Carray2D

```C
// Program to add two matrices
#include<stdio.h>
int main(){
    int row, column, a[10][10], b[10][10], sum[10][10];
    printf("Enter the number of rows(1 - 10): ");
    scanf("%d", &row);
    printf("Enter the number of columns(1 - 10): ");
    scanf("%d", &column);

    printf("\nEnter elements of 1st matrix:\n");
    for (int i = 0; i < row; i++){
        for (int j = 0; j < column; j++){
            printf("Enter element A%d%d: ", i, j);
            scanf("%d", &a[i][j]);
        }
    }
    
    printf("Enter elements of 2nd matrix:\n");
    for (int i = 0; i < row; i++){
        for (int j = 0; j < column; j++){
            printf("Enter element B%d%d: ", i, j);
            scanf("%d", &b[i][j]);
        }
    }
    
    // adding two matrices
    for (int i = 0; i < row; i++){
        for (int j = 0; j < column; j++){
            sum[i][j] = a[i][j] + b[i][j];
        }
    }
    
    // printing the results
    for (int i = 0; i < row; i++){
        for (int j = 0; j < column; j++){
            printf("%d  ", sum[i][j]);
            if (j == column - 1){
                printf("\n\n");
            }   
        }
        
    }

    return 0;
}
```