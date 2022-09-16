#C #Carrays #Carrayfunctions 

```C
// Basic Array syntax
#include<stdio.h>
int main(){
    // initializing array data
    int data[] = {45, 26, 89, 333, 78};

    // modifying array elements
    data[3] = 444;

    for (int i = 0; i <= 5; i++){
        printf("Index %d item: %d\n", i, data[i]);
    }
    
    return 0;
}
```

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

### Array Function
```C
#include<stdio.h>
void printAge(int age1, int age2);
void printAge1(int age[]);

int main(){
    int ageArray[] = {5, 6, 7, 8, 9};

    // passing the 1st & 4th elements
    printAge(ageArray[0], ageArray[3]);

    // notice we do not use [] during the function call 
    printAge1(ageArray);
    
    return 0;
}

// Pass an Array Element
void printAge(int age1, int age2){
    printf("Array element1: %d\n", age1);
    printf("Array element4: %d\n", age2);
}

// Pass an Entire Array
// notice the use of [] here
void printAge1(int age[]){
    // print elements of the array
    printf("Entire array element1: %d\n", age[0]);
    printf("Entire array element4: %d", age[3]);
}
```