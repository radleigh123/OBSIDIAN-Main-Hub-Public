---
cssclass:
aliases:
tags:
---
**[[DISCRET12ch5|BACK]]**

---
## Example 5.6: A Cautionary Example
According to De Morgan’s laws, the negation of
<center><em>p</em>: Jim is tall and Jim is thin</center>
is <center><em>∼p</em>: Jim is not tall or Jim is not thin</center>

because the negation of an **and** statement is the **or** statement in which the two components are negated. 

Unfortunately, a potentially confusing aspect of the English language can arise when you are taking negations of this kind. Note that statement $p$ can be written more compactly as

![[DISCRET12ch5Example6image.png|center]]

When it is so written, another way to negate it is

![[DISCRET12ch5Example6image1.png|center]]

But in this form the negation looks like an and statement. Doesn’t that violate De Morgan’s laws?

Actually no violation occurs. The reason is that in formal logic the words **and** and **or** are allowed only between complete statements, not between sentence fragments. One lesson to be learned from this example is that when you apply De Morgan’s laws, you must have complete statements on either side of each and and on either side of each or.

>[!WARNING|alt-co ttl-c]
> Although the laws of logic are extremely useful, they should be used as an aid to thinking, not as a mechanical substitute for it.