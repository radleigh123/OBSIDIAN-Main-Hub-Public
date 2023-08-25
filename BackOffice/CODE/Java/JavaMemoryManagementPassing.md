---
cssclass:
aliases:
tags:
- Java
- 
---
**[[Java#Java Memory Management|HOME [Java]]]**

---
![[JavaMemoryManagementPassingImage1.png|center wm-tl]]
1. First, a `String` will be created on the **heap**
2. The `Customer` object is created with the property that references the `String` object (since `String` is also an object).
3. Then, the `c` variable will be created on the **stack**, pointing to the `Customer` object.

<br>

![[JavaMemoryManagementPassingImage2.png|center wm-tl]]
1. When calling the `renameCustomer(c);`, passes the value `c`, creating a copy or a new variable `cust` is created on the stack.

<br>

![[JavaMemoryManagementPassingImage3.png|wm-tl center]]
The original `String` object, `Sally`, is no longer referenced from anywhere. 

>[!BUG] `String` objects are immutable.
> You can't change the value of `Strings`, if so, it will create a new `String` object on the **heap**. Resulting in the original `String` not having a reference to.