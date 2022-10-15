**[C](C#^ENUM)**

#C #Clecture #Cenumeration 
>[!TIP] # Enumeration
> is a user defined type which is <u>used to assign names</u> to integral constans because names are easier to handle in program
>>[!EXAMPLE]-
>> ![[Pasted image 20221016010643.png]]![[Pasted image 20221016010658.png]]
>
>>[!WARNING]- Why **enum** instead of **\#define** to assign [integral constants](Cconstants.md)
>>- enums can be declared in the local scope
>> ![[Pasted image 20221016011206.png]]
>>
>>- enum names are automatically initialized by the compiler
>>  ![[Pasted image 20221016011316.png]]

## Important Facts
>[!INFO]- Two or more names can have some value.
> ![[Pasted image 20221016011946.png]]

>[!INFO]- We can assign values in any order.
> All unassigned names will get value as value of previous name + 1
> ![[Pasted image 20221016012506.png]]

>[!INFO]- Only integral values are allowed
> ![[Pasted image 20221016012624.png]]

>[!INFO]- All enum constant must be unique in their scope
> ![[Pasted image 20221016012718.png]]

### 

<br>

# 
---
**Sources:**
- [Enumerations in C - YouTube](https://www.youtube.com/watch?v=9QdJExC2AVg&list=PLBlnK6fEyqRhX6r2uhhlubuF5QextdCSM&index=167)