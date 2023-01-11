---
aliases:
tags:
- C/Lecture
---
**[[C|HOME [C]]]**

---
## Call: Value & Reference
>[!column|flex no-t]
>>[!INFO|clean no-i] Call by value
>> ```C
>> #include<stdio.h>
>> void change(int num) {
>> 	printf("Before adding value inside function num=%d \n",num);
>> 	num=num+100;
>> 	printf("After adding value inside function num=%d \n", num);
>> }
>> 
>> int main() {
>> 	int x=100;
>> 	
>> 	printf("Before function call x=%d \n", x);
>> 	change(x);//passing value in function
>> 	printf("After function call x=%d \n", x);
>> 	
>> 	return 0;
>> }
>> ```
>
>>[!INFO|clean no-i] Call by reference
>> ```C
>> #include<stdio.h>
>> void change(int *num) {
>> 	printf("Before adding value inside function num=%d \n", *num);
>> 	*num += 100;
>> 	printf("After adding value inside function num=%d \n", *num);
>> }
>> 
>> int main() {
>> 	int x=100;
>> 	
>> 	printf("Before function call x=%d \n", x);
>> 	change(&x); //passing reference in function
>> 	printf("After function call x=%d \n", x);
>> 	
>> 	return 0;
>> }
>> ```

<br>

# 
---
**Sources:**
- [Call by Value and Call by Reference in C - javatpoint](https://www.javatpoint.com/call-by-value-and-call-by-reference-in-c)