---
aliases:
---
**tags:** #C/Structures/Functions 
**[[0Structure|BACK]]**

---
```C
#include<stdio.h>
struct student{
    char name[50];
    int age;
};

//function prototype
void display(struct student s);

int main(){
    struct student s1;

    printf("Enter name: ");

    // read string input from the user until \n is entered
    // \n is discarded
    scanf("%[^\n]%*c", s1.name);

    printf("Enter age: ");
    scanf("%d", &s1.age);

    // passing struct as an argument
    display(s1); 

    return 0;
}

void display(struct student s){
    printf("\nDisplaying Information\n");
    printf("Name: %s\t", s.name);
    printf("Age: %d", s.age);
}
```