---
aliases:
---
**tags:** #C/File_Handling/Text_Files 
**[[Cfilehandling|BACK]]**

---
## Text Files
>[!column|flex no-t]
>>[!TODO|no-t]+ 
>> \- are normal **.txt** files
>> \- takes minimum effort to maintain
>
>>[!DONE|no-t]
>> \- easily readable
>> \- provides less security
>> \- takes bigger storage space

### Reading and Writing
>[!aside|show-title bg-purple]- example
>```C
> #include <stdio.h>
> #include <stdlib.h>
>
> int main() {
> 	int num;
> 	FILE *fptr;
> 	if ((fptr = fopen("students.txt", "w+")) == NULL) {
> 		printf("Error!");
> 		exit(1);
> 	}
>	
> 	printf("Enter number: ");
> 	scanf("%d", &num);
> 	fprintf(fptr, "%d\n", num); // stores the data into the file
>	
> 	fscanf(fptr, "%d", &num); // reads the data inside the file
> 	printf("Number inside the file is %d\n\n", num);
> 	fclose(fptr);
>	
> 	printf("Successfully closed the file");
> 	return 0;
> }
> ```

The only difference is that [[CFILE_HANDLINGfprintf|`fprintf()`]] and [[CFILE_HANDLINGfscanf|`fscanf()`]] expects a pointer to the structure [[Cfilehandling#1. Declaration of file pointer|FILE]].

>[!aside|show-title center no-i]+ *Other functions like **`fgetchar()`**, **`fputc()`**, etc. can be used in a similar way.*

# 

<br>

---
**Sources:**
- [Programiz](https://www.programiz.com/c-programming/c-file-input-output#:~:text=to%20be%20closed.-,Reading%20and%20writing%20to%20a%20text%20file,-For%20reading%20and)