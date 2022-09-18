#C #Cstructures #Cloop 

```C
// Program to store information of 5 students using structure
#include<stdio.h>
struct student{
    char firstName[50];
    int roll, marks;
};

int main(){
    struct student s1[5];

    printf("Enter information of students\n");

    // storing information
    for (int i = 0; i < 5; i++){
        s1[i].roll = i + 1;
        printf("\nFor roll number%d,\n", s1[i].roll);
        printf("Enter first name: ");
        scanf("%s", s1[i].firstName);
        printf("Enter marks: ");
        scanf("%d", &s1[i].marks);
    }
    printf("Displaying Information\n");

    // displaying information
    for (int i = 0; i < 5; i++){
        printf("\nRoll number: %d\n", i + 1);
        printf("First name: ");
        puts(s1[i].firstName);
        printf("Marks: %d", s1[i].marks);
        printf("\n");
    }

    return 0;
}
```