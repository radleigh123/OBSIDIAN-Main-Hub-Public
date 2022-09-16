#C #Cstructures #Cfunctions 

```C
#include<stdio.h>
struct student{
    char name[50];
    int age;
};

// function prototype
struct student getInformation();

int main(){
    struct student s;

    s = getInformation();

    printf("\nDisplaying Information\n");
    printf("Name: %s\t\t", s.name);
    printf("Age: %d", s.age);

    return 0;
}

struct student getInformation(){
    struct student s1;

    printf("Enter name: ");
    scanf("%[^\n]%*c", s1.name);

    printf("Enter age: ");
    scanf("%d", &s1.age);

    return s1;
};
```