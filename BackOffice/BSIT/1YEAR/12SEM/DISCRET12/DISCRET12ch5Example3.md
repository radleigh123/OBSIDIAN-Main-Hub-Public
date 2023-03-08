---
cssclass:
aliases:
tags:
---
**[[DISCRET12ch5|BACK]]**

---
## Example 5.3: Negations of And and Or: De Morgan’s Laws
For the statement “*John is tall and Jim is redheaded*” to be true, both components must be true. So for the statement to be false, one or both components must be false. Thus the negation can be written as “*John is not tall or Jim is not redheaded*.” In general, the negation of the conjunction of two statements is logically equivalent to the disjunction of their negations. That is, statements of the forms $∼(p ∧ q)$ and $∼p\ \ ∨ ∼q$ are logically equivalent. Check this using truth tables.

**Solution:**
![[DISCRET12ch5Example3image.png|center wm-tl]]

Symbolically,
$$\lnot(p \land q)\ \equiv\ \lnot p \lor \lnot q$$

In the exercises at the end of this section you are asked to show the analogous law that the negation of the disjunction of two statements is logically equivalent to the conjunction of their negations:
$$\lnot(p \land q)\ \equiv\ \lnot p \land \lnot q$$
The two logical equivalences of *Example 5.3* are known as **De Morgan’s laws of logic** in honor of Augustus De Morgan, who was the first to state them in formal mathematical terms.

<br>

>[!DONE|alt-co] De Morgan's Laws
> The negation of an **and** statement is logically equivalent to the **or** statement in which each component is negated.
> The negation of an **or** statement is logically equivalent to the **and** statement in which each component is negated

<br>

# 
---
- [[DISCRET12ch5Example4|Example 5.4: Applying De Morgan's Laws]]
- [[DISCRET12ch5Example5|Example 5.5: Inequalities and De Morgan’s Laws]]