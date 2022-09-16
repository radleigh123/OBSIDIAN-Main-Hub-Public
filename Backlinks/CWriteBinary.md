#C #CFileHandling #Cloop 

```C
#include<stdio.h>
#include<stdlib.h>

struct threeNum{
    int num1, num2, num3;
};

int main(){
    struct threeNum number;
    FILE *ptr;

    if ((ptr = fopen("D:\\Users\\For WEBTOON\\COLLEGE\\PROGRAMMING\\C-LANG\\C Course\\C Learn\\File Handling\\Binary File\\Program.bin", "wb")) == NULL){
        printf("Error! Can't open file.");
        exit(1);
    }
    
    for (int i = 1; i <= 5; i++){
        number.num1 = i;
        number.num2 = 5 * i;
        number.num3 = 5 * i + 1;
        fwrite(&number, sizeof(struct threeNum), 1, ptr);
    }
    fclose(ptr);

    return 0;
}
```