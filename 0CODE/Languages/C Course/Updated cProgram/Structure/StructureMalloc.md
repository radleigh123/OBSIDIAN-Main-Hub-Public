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