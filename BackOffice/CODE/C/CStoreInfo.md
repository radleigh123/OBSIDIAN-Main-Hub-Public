---
aliases:
---
**tags:** #C/Structures 
**[[1Structure|BACK]]**

---
```C
// Store information of a student using structure
#include<stdio.h>
struct student{
    char name[50];
    int roll, marks;
};

int main(){
    struct student s1;
    
    printf("Enter information\n");
    printf("Enter name: ");
    scanf("%[^\n]%*c", s1.name);

    printf("Enter roll number: ");
    scanf("%d", &s1.roll);
    printf("Enter marks: ");
    scanf("%d", &s1.marks);

    printf("\nDisplaying Information\n");
    printf("Name: %s\n", s1.name);
    printf("Roll number: %d\t\t", s1.roll);
    printf("Marks: %d", s1.marks);
    
    return 0;
}
```