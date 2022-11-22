---
aliases:
tags:
- C/Operators
- C/Lecture
---
**[[Coperators|BACK]]**

---
## Logical Operator
- used to combine 2 conditions

>[!recite|no-i collapse clean] &&, ||, !

**Short circuit case**

![[CLOGICALsample.svg|center cover wm-tl]]
>[!column|flex no-t]
>>[!NOTE|clean no-i collapse ttl-c] <u>case of `&&`</u>
>> if there is a condition anywhere in the expression that returns **FALSE**, then all conditions after that will not be evaluated.
>
>>[!NOTE|clean no-i collapse ttl-c] <u>case of `||`</u>
>> if there is a condition that is **TRUE**, then all conditions after that will not be evaluated.