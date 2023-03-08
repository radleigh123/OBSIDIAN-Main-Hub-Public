---
cssclass:
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Logical Equivalence
The statements

<center>6 is greater than 2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; and &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2 is less than 6</center>

are two different ways of saying the same thing. Why? Because of the definition of the phrases greater than and less than. By contrast, although the statements

<center>(1) Dogs bark and cats meow&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; and &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(2) Cats meow and dogs bark</center>

are also two different ways of saying the same thing, the reason has nothing to do with the definition of the words. It has to do with the logical form of the statements. Any two statements whose logical forms are related in the same way as (1) and (2) would either both be true or both be false. You can see this by examining the following truth table, where the statement variables p and q are substituted for the component statements “*Dogs bark*” and “*Cats meow,*” respectively.

The table shows that for each combination of truth values for $p$ and $q$, $p ∧ q$ is true when, and only when, $q ∧ p$ is true. In such a case, the statement forms are called logically equivalent, and we say that (1) and (2) are logically equivalent statements.

![[DISCRET12ch5image.png|center ws-med]]

>[!INFO|collapse alt-co] DEFINITION
> Two statement forms are called **logically equivalent** if, and only if, they have identical truth values for each possible substitution of statements for their statement variables. The logical equivalence of statement forms $P$ and $Q$ is denoted by writing $P\ \ ≡\ \ Q$.
> &nbsp;
> Two statements are called <u>logically equivalent</u> if, and only if, they have logically equivalent forms when identical component statement variables are used to replace identical component statements.

[[DISCRET12ch5Example1|Example 5.1]]: **Double Negative Property: ∼(∼p) ≡ p**
[[DISCRET12ch5Example2|Example 5.2]]: **Showing Nonequivalence**


[[DISCRET12ch5Example3|Example 5.3]]: **Negations of And and Or: De Morgan’s Laws**
[[DISCRET12ch5Example4|Example 5.4]]: **Applying De Morgan’s Laws**
[[DISCRET12ch5Example5|Example 5.5]]: **Inequalities and De Morgan’s Laws**
[[DISCRET12ch5Example6|Example 5.6]]: **A Cautionary Example**