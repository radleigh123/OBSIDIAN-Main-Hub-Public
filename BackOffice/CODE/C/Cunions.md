---
title: Unions
creation-date: 2022-10-26
aliases:
---
**tags:** #C/Unions #C/Lecture 
**[[C|BACK]]**

---
# Unions
is a user defined data type but unlike structures, union members share same memory location.

![[Pasted image 20221012203927.png]]

>[!BUG]- Memory Allocation
>![[Pasted image 20221012204029.png]]

>[!BUG]- Fact
>In union, members will share same memory location. If we make changes in one member then it will be reflected to other member as well.
>
>>[!EXAMPLE]
>>![[Pasted image 20221012204911.png]]

>[!BUG]- Deciding the SIZE of Union
>Size of the union is taken according to the size of the largest member of the union.
>
>>[!EXAMPLE]
>>![[Pasted image 20221012205637.png]]

>[!BUG]- Accessing members using Pointers
>We can access members of union through [pointers](Cpointers.md) by using the arrow (->) operator.
>>[!EXAMPLE]
>>![[Pasted image 20221012210138.png]]

>[!CITE] **See also**
>1. [Application of Unions](CUNIONSapplications.md)
>2. [Application of Unions 2](CUNIONSapplications2.md)