---
aliases:
---
**tags:** #C/File_Handling #C/Structures/File_Handling #C/stdio/putchar  
**[[CCODES|BACK]]**

---
## C FileExample1
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

## C FileExample2
```C
// C program to write all the members of an array of structures to a file using fwrite(). Read the array from the file and display on the screen.
#include<stdio.h>
#include<stdlib.h>
struct student{
    char name[50];
    int height;
};

int main(){
    struct student stud1[5], stud2[5];
    FILE *ptr;
    
    // wb - Open for writing in Binary mode
    ptr = fopen("D:\\Users\\For WEBTOON\\COLLEGE\\PROGRAMMING\\C-LANG\\C Course\\Updated cProgram\\C Files\\file.txt", "wb");

    for (int i = 0; i < 5; i++){
        fflush(stdin);
        printf("Enter name: ");
        gets(stud1[i].name);

        printf("Enter height: ");
        scanf("%d", &stud1[i].height);
    }
    
    fwrite(stud1, sizeof(stud1), 1, ptr);
    fclose(ptr);

    // rb - Open for reading in Binary mode
    ptr = fopen("D:\\Users\\For WEBTOON\\COLLEGE\\PROGRAMMING\\C-LANG\\C Course\\Updated cProgram\\C Files\\file.txt", "rb");

    fread(stud2, sizeof(stud2), 1, ptr);
    for (int i = 0; i < 5; i++){
        printf("Name: %s\tHeight: %d\n", stud2[i].name, stud2[i].height);
    }
    fclose(ptr);

    return 0;
}
```

## C FileExample3
```C
#include<stdio.h>
int main(){
    FILE *ptr;
    int c;

    // open the current input file
    ptr = fopen(__FILE__, "r");

    do
    {
        c = getc(ptr); // read character
        putchar(c); // display character
    } while (c != EOF); // loop until the end of file is reached
    
    fclose(ptr);
    return 0;
}
```