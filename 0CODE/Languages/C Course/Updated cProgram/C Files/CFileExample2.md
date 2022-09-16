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