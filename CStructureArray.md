#C #Cstructures 

```C
// Arrays of Structures(AOS) and Pointers
#include<stdio.h>
struct Employee{
    int age, salary;
} person[3];

int main(){
    // take age and salary input of 3 persons
    for (int i = 0; i < 3; i++){
        printf("For employee %d:\n", i + 1);
        
        printf("Enter age: ");
        scanf("%d", &(person + i)->age);
        printf("Enter salary: ");
        scanf("%d", &(person + i)->salary);
    }
    
    // print age and salary of 3persons
    for (int i = 0; i < 3; i++){
        printf("\nEmployee %d:\n", i + 1);
        printf("Age = %d\t", (person + i)->age);
        printf("Salary = %d", (person + i)->salary);
    }

    return 0;
}
```