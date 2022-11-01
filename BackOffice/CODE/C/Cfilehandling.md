---
title: File Handling
creation-date: 2022-10-29
aliases: [fprintf, fscanf, fwrite, fclose, fread]
cssclass: no-m, t-c, t-w
---
**tags:** #C/File_Handling #C/Pointers/File_Handling  
**[[C|HOME [C]]]**

---
# File Handling
A file is a container in computer storage devices used for storing data.

>[!INFO|ttl-c no-i]- Why do we need File Handling in C?
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

>[!aside|bg-purple right]+ 
>- [[CFILE_HANDLINGexample1|Getting the Factorial number]]
>- [[CFILE_HANDLINGexample2|Compare console & text]]
>- [[CFILE_HANDLINGexample3|Print table of numbers]]
>- [[CFILE_HANDLINGexample4|Read multiple numbers]]
>- [[CFILE_HANDLINGexample5|Count number of characters using fgetc]]
>- [[CFILE_HANDLINGexample6|Count characters and words from file]]
>- [[CFILE_HANDLINGexample7|Copy contents of file to another]]
>- [[CFILE_HANDLINGexample8|Display source code as output on screen]]
^a6b496

**Types of Files**
- [[CFILE_HANDLINGtext|Text Files]]
- [[CFILE_HANDLINGbinary|Binary Files]]

<br>

## Prerequisites of file handling
### 1. Declaration of file pointer
When working with files, you need to declare a <mark class="hltr-blue">pointer of type file</mark>. This declaration is needed for communication between the file and the program.
>[!EXAMPLE|alt-co no-i] **Syntax:** `FILE *fptr;`

---
### 2. Opening a file
Using the **`fopen()`** function defined in the **`<stdio.h>`** header file.
>[!EXAMPLE|alt-co no-i] **Syntax** `fptr = fopen("filename", "mode");`

---
### 3. Closing a File
Closing a file is performed using the `fclose()` function
>[!EXAMPLE|alt-co no-i] **Syntax:** `fclose(fptr);`

---
## Opening Modes in `standard I/O`

| **<center>Mode</center>**      | **<center>Meaning of Mode</center>**   |                   |
| --------- | ----------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| **`r`**   | Open for reading                                      | If the file does not exist, `fopen()` returns NULL                                               |
| **`rb`**  | Open for reading in binary mode                       | If the file does not exist, `fopen()` returns NULL                                               |
| **`w`**   | Open for writing                                      | IF the file exists, its contents are overwritten. If the file does not exist, it will be created |
| **`wb`**  | Open for writing in binary mode                       | IF the file exists, its contents are overwritten. If the file does not exist, it will be created |
| **`a`**   | Open for append, Data is added to the end of the file | IF the does not exist, it will be created                                                        |
| **`ab`**  | Open for append, Data is added to the end of the file | IF the does not exist, it will be created                                                        |
|           |                                                       |                                                                                                  |
| **`r+`**  | Open for both reading and writing                     | If the file does not exist, `fopen()` returns NULL                                               |
| **`rb+`** | Open for both reading and writing in binary mode      | If the file does not exist, `fopen()` returns NULL                                               |
| **`w+`**  | Open for both reading and writing                     | IF the file exists, its contents are overwritten. If the file does not exist, it will be created |
| **`wb+`** | Open for both reading and writing in binary mode      | IF the file exists, its contents are overwritten. If the file does not exist, it will be created |
| **`a+`**  | Open for both reading and appending                   | IF the does not exist, it will be created                                                        |
| **`ab+`** | Open for both reading and appending in binary mode.   | If the file does not exist, it will be created.                                                  |

## Operators/Functions for file handling

| **<center>Function in Use</center>**     | **<center>Description of Function</center>**                 |
| ---------------------------------------- | ------------------------------------------------------------ |
| **`fopen()`**                            | used to open an existing file or a new file                  |
| **[[CFILE_HANDLINGfprintf\|fprintf()]]** | writing data into an available file                          |
| **[[CFILE_HANDLINGfscanf\|fscanf()]]**   | reading the data available in a file                         |
| **[[CFILE_HANDLINGfputc\|fputc()]]**     | writing any character into the program file                  |
| **[[CFILE_HANDLINGfgetc\|fgetc()]]**     | reading the character from an available file                 |
| **`fclose()`**                           | used to close the program file                               |
| **[[CFILE_HANDLINGfseek\|fseek()]]**     | used to set the file pointer to the intended file position   |
| **`fputw()`**                            | writing an integer into an available file                    |
| **`fgetw()`**                            | used to read an integer from the given file                  |
| **`ftell()`**                            | used for reading the current position of a file              |
| **`rewind()`**                           | sets an intended file pointer to the file’s beginning itself |
| **fgets()**                                         |                                                              |

# 

<br>

---
**Sources:**
- [Youtube - Sanjay Gupta](https://www.youtube.com/watch?v=lJPFWdVkPfk&list=PL-gW8Fj5TGrpVCun29h8HqtysUq6OPq3X)
- [GeeksforGeeks](https://www.geeksforgeeks.org/basics-file-handling-c/)
- [Programiz](https://www.programiz.com/c-programming/c-file-input-output)
- [C | GATE Notes](https://byjus.com/gate/file-handling-in-c/#what-is-file-handling-in-c)