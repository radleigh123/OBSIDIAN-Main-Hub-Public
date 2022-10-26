---
aliases:
---
**tags:** #C/File_Handling 
**[[0File Handling|BACK]]**

---
```C
#include<stdio.h>
#include<stdlib.h>

int main(){
    int num;
    FILE *fptr;

    if ((fptr = fopen("D:\\Users\\For WEBTOON\\COLLEGE\\PROGRAMMING\\C-LANG\\C Course\\C Learn\\File Handling\\Write.txt", "r")) == NULL){
        printf("Error! File does not exist.");

        // Program exits if the file pointer returns NULL
        exit(1);
    }
    
    // a function is used to read set of characters from file. 
    // It reads a word from the file and returns EOF at the end of file.
    fscanf(fptr,"%d", &num);

    printf("Value of n= %d", num);
    fclose(fptr);

    return 0;
}
```