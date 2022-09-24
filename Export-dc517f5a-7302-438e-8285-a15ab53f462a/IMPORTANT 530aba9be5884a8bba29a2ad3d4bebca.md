 **C standard** is the language specification which is adopted by all C compilers across the globe.
    
![Untitled](IMPORTANT%20530aba9be5884a8bba29a2ad3d4bebca/Untitled%201.png)
    
- Therefore, `**i++`** inside `sizeof` is not evaluated.

```c
int = 5;
int var = sizeof(i++);
printf("%d %d", i, var); // 5 4
```

---

- **Logical short circuit notes**.
    - if a condition anywhere in the expression is TRUE, then all conditions after that will not be evaluated.
- **Post-increment Operators.**
    - after completion of the expression, then post-increment is implemented.
    - [C Operators](https://www.notion.so/C-Operators-1b6bd32aff444b0db8fec19cc70a4fd4)
    
    ![Untitled](IMPORTANT%20530aba9be5884a8bba29a2ad3d4bebca/Untitled%202.png)
    
    ---
    
- **For loop().** It’s okay to not include or declare again both the initialization and condition. Simply declare only the ‘`;`’ to let the compiler know.
    
    ```c
    int i = 1024;
    for(; i; i >>= 1) {
    	printf("Hello World\n");
    }
    // prints 11 times
    ```
    
    ![Untitled](IMPORTANT%20530aba9be5884a8bba29a2ad3d4bebca/Untitled%203.png)
    
    [C Loops](https://www.notion.so/C-Loops-7d8335dad2434e5fbecf81e7e2a80874) 
    
    ---
    
- **printf.** returns the amount of letters printed.
    - `printf ("")` is considered to be 0. As nothing is printed.
        
        ```c
        int i = 0;
            for (printf("one\n"); i < 3 && printf(""); i++){
                printf("Hi!\n");
            }
        		// output: one
        ```
        
    
    [C Output Function](https://www.notion.so/C-Output-Function-286954d54de34ab985d9762165c07918) 
    
    ---
    
- Half adder logic is implemented
    
    ![Untitled](IMPORTANT%20530aba9be5884a8bba29a2ad3d4bebca/Untitled%204.png)
    

---

- Count **array elements** using sizeof() operator:
    
    ### `**sizeof(name_array) / sizeof(name_array[0])**`
    
    [C Arrays](https://www.notion.so/C-Arrays-f9e712229ff8471cb698a7f972e97dac) 
    
    ---