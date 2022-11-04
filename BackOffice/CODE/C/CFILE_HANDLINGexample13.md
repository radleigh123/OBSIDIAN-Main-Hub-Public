---
cssclass: no-m
aliases:
tags:
- C/File_Handling
- C/Structures/File_Handling
---
**[[Cfilehandling|BACK]]**

---
>[!recite|no-i alt-co collapse] Reading and Writing [[Cstructures|`Structure`]] into File

<br>

>[!INFO|ttl-c clean collapse ngm no-i]- **Writing into the file**
>```C
>#include <stdio.h>
>#include <stdlib.h>
>
>struct student
>{
>    int num;
>    char name[10];
>};
>
>int main()
>{
>    FILE *fptr;
>    if ((fptr = fopen("proto.bin", "wb")) == NULL)
>    {
>        printf("Error!");
>        exit(1);
>    }
>    struct student s1;
>    
>    fread(&s1, sizeof(struct student), 1, fptr);
>
>    fclose(fptr);
>    return 0;
>}
>```

>[!INFO|collapse clean ttl-c ngm no-i]+ **Reading from a file**
>```C
>#include <stdio.h>
>#include <stdlib.h>
>
>struct student
>{
>    int num;
>    char name[10];
>};
>
>int main()
>{
>    FILE *fptr;
>    if ((fptr = fopen("proto.bin", "wb")) == NULL)
>    {
>        printf("Error!");
>        exit(1);
>    }
>    struct student s1;
>    
>    printf("Enter roll number: ");
>    scanf("%d", &s1.num);
>	while((getchar()) != '\n'); // clears the input buffer
>
>    printf("Enter name: ");
>    gets(s1.name);
>
>    fwrite(&s1, sizeof(struct student), 1, fptr);
>    printf("%d. %s", s1.num, s1.name);
>
>    fclose(fptr);
>    return 0;
>}
>```
# 

<br>

---
**Sources:**
- [Reading and Writing structure into File in C language | C programming video tutorials series - YouTube](https://www.youtube.com/watch?v=bLAv0MY68HA&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X&index=33)
- [Clearing The Input Buffer In C/C++ - GeeksforGeeks](https://www.geeksforgeeks.org/clearing-the-input-buffer-in-cc/)