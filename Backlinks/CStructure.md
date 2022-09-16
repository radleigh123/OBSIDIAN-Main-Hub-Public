#C #Cstructures 

```C
// A structure - a collection of variables (can be different types) under a single name
#include<stdio.h>
#include<string.h>

typedef struct Person{
    int age;
    double height;
} person;

int main(){
    person p1, p2;

    // assign values to p1 and p2 variables
    p1.age = 10, p1.height = 5.55;
    p2.age = 15, p2.height = 6.00;

    printf("Age: %d\t", p1.age);
    printf("Height: %.2lf\n\n", p1.height);
    printf("Age: %d\t", p2.age);
    printf("Height: %.2lf", p2.height);

    return 0;
}
```