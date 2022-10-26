---
title: Cfilehandling
creation-date: 2022-10-26
aliases:
---
**tags:** #C/File_Handling  
**[[C#^c4be75|HOME [C]]]**

---
# File Handling
- refers to the method of storing data in the C program.
	- **Text Files**
	- **Binary Files**

>[!INFO]- What is a File in C?
>- a file refers to a source in which a program stores the information/data in the form of bytes of sequence on a disk(permanently).

>[!INFO]- Why do we need File Handling in C?
>- There are times when the output generated out of a program after its compilation and running do not serve our intended purpose.
>-  In such cases, we might want to check the program’s output various times. Now, compiling and running the very same program multiple times becomes a tedious task for any programmer.
>
>>[!EXAMPLE] Reusability
>>- File handling allows us to preserve the information/data generated after we run the program.
>
>>[!EXAMPLE] Saves Time
>>- Some programs might require a large amount of input from their users. In such cases, file handling allows you to easily access a part of a code using individual commands.
>
>>[!EXAMPLE] Commendable storage capacity
>>- When storing data in files, you can leave behind the worry of storing all the info in bulk in any program.
>
>>[!EXAMPLE] Portability
>>- The contents available in any file can be transferred to another one without any data loss in the computer system. This saves a lot of effort and minimizes the risk of flawed coding.

## Operators/Functions used for File Handling in C

| **Function in Use** | **Description of Function**                                  |
| ------------------- | ------------------------------------------------------------ |
| fopen()             | used to open an existing file or a new file                  |
| fprintf()           | writing data into an available file                          |
| fscanf()            | reading the data available in a file                         |
| fputc()             | writing any character into the program file                  |
| fgetc()             | reading the character from an available file                 |
| fclose()            | used to close the program file                               |
| fseek()             | used to set the file pointer to the intended file position   |
| fputw()             | writing an integer into an available file                    |
| fgetw()             | used to read an integer from the given file                  |
| ftell()             | used for reading the current position of a file              |
| rewind()            | sets an intended file pointer to the file’s beginning itself |

# 

<br>

---
**Sources:**
- [File Handling in C | GATE Notes (byjus.com)](https://byjus.com/gate/file-handling-in-c/#what-is-file-handling-in-c)
- [Basics of File Handling in C - GeeksforGeeks](https://www.geeksforgeeks.org/basics-file-handling-c/?id=discuss)