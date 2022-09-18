#C #Cstructures #Cpointers #Cmalloc #Cfree #C #Cloop #Cstructures #Cstdlib 

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

```C
// Demonstrate the Dynamic Memory Allocation for Structure
#include<stdio.h>
#include<stdlib.h>
struct Course{
    char subject[30];
    int marks;
};

int main(){
    struct Course *ptr;
    int noOfRecords;
    printf("Enter the number of records: ");
    scanf("%d", &noOfRecords);

    // Memory allocation for noOfRecords structures
    ptr = (struct Course*) malloc(noOfRecords * sizeof(struct Course));
    for (int i = 0; i < noOfRecords; i++){
        printf("Enter subject and marks:\n");
        scanf("%s %d", (ptr + i)->subject, &(ptr + i)->marks);
    }
    
    printf("Displaying Information\n");
    for (int i = 0; i < noOfRecords; i++){
        printf("%s\t%d\n", (ptr + i)->subject, (ptr + i)->marks);
    }
    
    free(ptr);

    return 0;
}
```