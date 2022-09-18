#C #Cstructures #Cloop 

```C
// Program to add two distances(in Inch-Feet system) using structures
#include<stdio.h>
struct Distance{
    int feet;
    double inch;
};

int main(){
    struct Distance d1, d2, result;

    // take first distance input
    printf("Enter 1st distance\n");
    printf("Enter feet: ");
    scanf("%d", &d1.feet);
    printf("Enter inch: ");
    scanf("%lf", &d1.inch);

    // take second distance input
    printf("Enter 2nd distance\n");
    printf("Enter feet: ");
    scanf("%d", &d2.feet);
    printf("Enter inch: ");
    scanf("%lf", &d2.inch);

    // adding distances
    result.feet = d1.feet + d2.feet;
    result.inch = d1.inch + d2.feet;

    // convert inches to feet if greater than 12
    while (result.inch >= 12.0){
        result.inch = result.inch - 12.0;
        result.feet++;
    }
    printf("\nSum of distances = %d\'-%.1lf\"", result.feet, result.inch);

    return 0;
}
```