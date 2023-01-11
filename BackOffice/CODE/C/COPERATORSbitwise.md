---
aliases:
tags:
- C/Operators
- C/Lecture
---
**[[Coperators|BACK]]**

---
## Bitwise Operator
- it does bitwise manipulation

>[!recite|no-i collapse clean] &, |, ~, <<, >>, ^

---
**AND operator  `&`**
>[!column|flex no-t txt-c]
>>[!NOTE|no-t collapse clean]
>> take 2bits at a time and perform AND
>
>>[!NOTE|no-t collapse clean]
>> is binary operator takes 2 numbers and perform AND
>
>>[!NOTE|no-t collapse clean]
>> result of AND is 1 when both bits are 1

**e.g.**
![[CBITWISEsample1.svg|cover left hsmall]]

| A   | B   | A&B |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 1   | 

---
**OR operator `|`**
>[!column|flex no-t txt-c]
>>[!NOTE|no-t collapse clean]
>> take 2bits at a time and perform OR
>
>>[!NOTE|no-t collapse clean]
>> is binary operator takes 2 numbers and perform OR
>
>>[!NOTE|no-t collapse clean]
>> result of OR is 0 when both bits are 0

**e.g.**
![[CBITWISEsample2.svg|cover left hsmall]]

| A   | B   | A&B |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 1   |

---
**NOT operator `~`**
>[!column|flex no-t txt-c]
>>[!NOTE|no-t collapse clean]
>> job is to complement each bit one by one
>
>>[!NOTE|no-t collapse clean]
>> is a [[COPERATORSunary|unary operator]]
>
>>[!NOTE|no-t collapse clean]
>> result of NOT is 0 when both bit is 1, and 1 when bit is 0

**e.g.**
![[CBITWISEsample3.svg|cover left hsmall]]

| A   | ~A   |
| --- | --- |
| 0   | 1   |
| 1   | 0   |

<br>

---
**XOR operator `^`**
[[COPERATORSbinary|binary operator]], result of XOR is 1 when two bits are different
>[!column|flex no-t]
>>[!NOTE|clean no-i ttl-c] Inclusive OR
>> Either A is 1 or B is 1 or Both are 1, then the output is 1
>> 
>> | A | B | A OR B |
>> | -- | -- | -- |
>> | 0 | 0 | 0 |
>> | 0 | 1 | 1 |
>> | 1 | 0 | 1 |
>> | **1** | **1** | **1** |
>
>>[!NOTE|clean no-i ttl-c] Exclusive OR
>> Either A is 1 or B is 1 then the output is 1 but when both A and B are 1 then output is 0
>> 
>> | A | B | A XOR B |
>> | -- | -- | -- |
>> | 0 | 0 | 0 |
>> | 0 | 1 | 1 |
>> | 1 | 0 | 1 |
>> | **1** | **1** | **0** |

<br>

# 
---
**Sources:**
- [Bitwise Operator in C - javatpoint](https://www.javatpoint.com/bitwise-operator-in-c)

**To learn more:**
- [2s complement in C - javatpoint](https://www.javatpoint.com/2s-complement-in-c)