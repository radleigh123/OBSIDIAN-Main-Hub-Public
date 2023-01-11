---
aliases:
tags:
- C/Lecture
- C/Pointers
---
**[[C|HOME [C]]]**

---
## Dangling Pointers
occurs at the time of the object destruction when the object is deleted or de-allocated from memory without modifying the value of the pointer.
**e.g.**
>[!column|clean no-t]
>>[!INFO|clean no-t collapse]
>> ![[Pasted image 20230104192404.png|center]]
>
>>[!INFO|clean no-t collapse]
>> ```C
>> #include <stdio.h>
>> 
>> int *fun() {
>> 	int y=10;
>> 	return &y;
>> }
>> 
>> int main() {
>> 	int *p=fun();
>> 
>> 	// dangling pointer
>> 	// address of y is already terminated
>> 	printf("%d", *p);
>> 	return 0;
>> }
>> ```

**Using static variables**
>[!column|clean no-t]
>>[!INFO|clean no-t collapse txt-c]
>> ![[Pasted image 20230104193901.png]]
>
>>[!INFO|clean no-t collapse]
>> ```C
>> #include <stdio.h>
>> 
>> int *fun() {
>> 	static int y=10;
>> 	return &y;
>> }
>> 
>> int main() {
>> 	int *p=fun();
>> 
>> 	printf("%d", *p); // 10
>> 	return 0;
>> }
>> ```

The above code is similar to the previous one but the only difference is that the variable `y` is **static**. We know that **[[CVARIABLEstatic|static variable]]** stores in the global memory.

>[!WARNING|alt-co]+ &nbsp Avoid dangling pointer errors
> The dangling pointer errors can be avoided by initializing the pointer to the `NULL` value. If we assign the `NULL` value to the pointer, then the pointer will not point to the de-allocated memory. Assigning `NULL` value to the pointer means that the pointer is not pointing to any memory location.

<br>

# 
---
**Sources:**
- [Dangling Pointers in C - javatpoint](https://www.javatpoint.com/dangling-pointers-in-c)