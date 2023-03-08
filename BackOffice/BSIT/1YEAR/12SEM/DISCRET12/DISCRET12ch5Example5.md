---
cssclass:
aliases:
tags:
---
**[[DISCRET12ch5|BACK]]**

---
## Example 5.5: Inequalities and De Morgan’s Laws
Use De Morgan’s laws to write the negation of $−1 <\\ x\\ ≤\ 4$.

**Solution:**
The given statement is equivalent to
$$-1 \lt x\qquad\text{and}\qquad x \le 4$$
By De Morgan's laws, the negation is
$$-1 \not\lt x\qquad\text{and}\qquad x \not\le 4$$
which is equivalent to
$$-1 \ge x\qquad\text{and}\qquad x \gt 4$$

Pictorially, if $−1 ≥ x$ or $x > 4$, then $x$ lies in the shaded region of the number line, as shown below.
![[DISCRET12ch5Example5image.png|center]]

De Morgan’s laws are frequently used in writing computer programs. For instance, suppose you want your program to delete all files modified outside a certain range of dates, say from date 1 through date 2 inclusive. You would use the fact that.
<center>∼(<em>date</em>1&nbsp;&nbsp; ≤&nbsp;&nbsp; <em>file_modification_date</em>&nbsp;&nbsp; ≤&nbsp;&nbsp; <em>date</em>2)</center>

is equivalent to
<center>(<em>file_modification_date</em>&nbsp;&nbsp; <&nbsp;&nbsp; <em>date</em>1)&nbsp;&nbsp;&nbsp;&nbsp; or&nbsp;&nbsp;&nbsp;&nbsp; (<em>date</em>2&nbsp;&nbsp; <&nbsp;&nbsp; <em>file_modification_date</em>)</center>