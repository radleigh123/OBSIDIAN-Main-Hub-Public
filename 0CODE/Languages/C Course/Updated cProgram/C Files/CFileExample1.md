#C #CFileHandling 

```C
// C program to read name and marks of n number of students and store them in a file.
#include<stdio.h>
#include<stdlib.h>

int main(){
    char name[50];
    int marks, num;

    printf("Enter number of students: ");
    scanf("%d", &num);

    FILE *ptr;
    ptr = (fopen("D:\\Users\\For WEBTOON\\COLLEGE\\PROGRAMMING\\C-LANG\\C Course\\Updated cProgram\\C Files\\students.txt", "w"));
    if (ptr == NULL){
        printf("Error!");

        exit(1);
    }
    
    for (int i = 0; i < num; i++){
        printf("For student%d\nEnter name: ", i + 1);
        scanf("%s", name);

        printf("Enter marks: ");
        scanf("%d", &marks);

        fprintf(ptr, "Name: %s\nMarks: %d\n", name, marks);
    }
    
    fclose(ptr);
    return 0;
}
```