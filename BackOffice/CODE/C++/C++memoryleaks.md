---
title: C++memoryleaks
creation-date: 2023-01-10
aliases:
tags:
- CPP/Lecture
- CPP/Memory
- CPP/Pointers
---
**[[C++|HOME [C++]]]**

---
# Memory leaks
when we loose access to memory that is dynamically allocated

>[!FAIL]+ Reassignment of stack address to active dynamic address pointer
> ```cpp
> #include <iostream>
> 
> int main()
> {
>     int *ptr_var{new int{65}}; // points to address1
>     int var1{45}; // lives at address2
>     
>     // Should delete and reset here
> 
>     // now ptr_var points to address2, but address1 is still in use. Our program has lost access to that memory location
>     ptr_var = &var1;
> 
>     return 0;
> }
> ```

>[!FAIL]+ Double allocation
> ```cpp
> #include <iostream>
> 
> int main()
> {
>     int *ptr_var1{new int{55}};
>     
>     // Use the pointer. Should delete and reset here
>     
>     ptr_var1 = new int{44}; // memory w/ int{55} leaked
>     
>     return 0;
> }
> ```