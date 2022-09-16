#C #Cstructures 

```C
#include<stdio.h>

struct person{
    int age;
    double weight;
};

int main(){
    struct person *personPtr, person1;
    personPtr = &person1;

    printf("Enter age: ");
    scanf("%d", &personPtr->age);

    printf("Enter weight: ");
    scanf("%lf", &personPtr->weight);

    printf("Displaying:\n");

    // personPtr->age = (*personPtr).age
    printf("Age: %d\t\t", personPtr->age);
    printf("Weight: %.2lf", (*personPtr).weight);

    return 0;
}
```