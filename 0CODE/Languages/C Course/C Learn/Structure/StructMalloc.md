```C
// Sometimes, the number of struct variables you declared may be insufficient. You may need to allocate memory 
// during run-time. Here's how you can achieve this in C programming.
#include<stdio.h>
#include<stdlib.h>
struct person{
    int age;
    char name[50];
};

int main(){
    struct person *ptr;
    int n;

    printf("Enter number of persons: ");
    scanf("%d", &n);

    // allocating memory of n numbers of struct person
    ptr = (struct person*) malloc(n * sizeof(struct person));

    for (int i = 0; i < n; i++){
        printf("Enter first name and age respectively: ");

        // To access members of 1st struct person, ptr->name and ptr->age is used.
        // To access members of 2nd struct person, (ptr + 1)->name and (ptr + 1)->age is used.
        scanf("%s%d", (ptr + i)->name, &(ptr + i)->age);
    }
    
    for (int i = 0; i < n; i++){
        printf("Name: %s\tAge: %d\n", (ptr + i)->name, (ptr + i)->age);
    }

    free(ptr);

    return 0;
}
```