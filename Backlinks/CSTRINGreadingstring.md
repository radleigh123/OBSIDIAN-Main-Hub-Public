#C #Clecture #Cstrings #Cscanf #Cgets
## Reading Strings using scanf and gets functions
### [scanf()](Cscanf.md)
- Using **scanf()** function, we can read a string into a string variable (character array).

![[Pasted image 20220924225049.png|450]]
### [gets()](Cgets)
- <mark class="hltr-lightred">gets() is still unsafe</mark>, it will try to write the characters beyond the memory allocated to the character array which is unsafe because it will simply overwrite the memory beyond the memory allocated to the character array.
- Hence, it is <mark class="hltr-lightred">not advisable to use the gets() function</mark>

<br>

# 
---
| TAKE NOTE            |
| -------------------- |
| [[Cscanf&getslimit]] |

**[BACK](Cstrings)**