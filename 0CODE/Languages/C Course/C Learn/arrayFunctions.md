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