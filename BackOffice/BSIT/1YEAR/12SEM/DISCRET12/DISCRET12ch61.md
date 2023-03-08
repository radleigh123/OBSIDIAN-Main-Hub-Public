---
cssclass:
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Logical Equivalences Involving →
Imagine that you are trying to solve a problem involving three statements: $p$, $q$, and $r$. Suppose you know that the truth of $r$ follows from the truth of $p$ and also that the truth of $r$ follows from the truth of $q$. Then no matter whether $p$ or $q$ is the case, the truth of $r$ must follow. The division-into-cases method of analysis is based on this idea.

[[DISCRET12ch61Example1|Example 61.1]]: **Division into Cases: Showing that p ∨ q → r ≡ ( p → r) ∧ (q → r)**

#### Representation of If-Then As Or
In [[exercise13(a)image.png|exercise13(a)]] at the end of this section you are asked to use truth tables to show that
<center>p → q ≡ ∼p ∨ q.</center>

The logical equivalence of “if p then q” and “not p or q” is occasionally used in everyday speech. Here is one instance.

[[DISCRET12ch61Example2|Example 61.2]]: **Application of the Equivalence between ∼p ∨ q and p → q**

#### The Negation of a Conditional Statement
By definition, $p → q$ is **false if**, and only if, its hypothesis, $p$, is **true** and its conclusion,
$q$, is **false**. It follows that

![[Pasted image 20230308191855.png|center wm-tl]]

This can be restated symbolically as follows:
![[Pasted image 20230308191935.png|center]]

You can also obtain this result by starting from the logical equivalence $p → q ≡ ∼ p ∨ q$. Take the negation of both sides to obtain

![[Pasted image 20230308192032.png|center]]

Yet another way to derive this result is to construct truth tables for $∼(p → q)$ and for $p ∧ ∼q$ and to check that they have the same truth values. (See [[exercise13(a)image.png|exercise13(b)]] at the end of this section.)

[[DISCRET12ch61Example3|Example 61.3]]: **Negations of If-Then Statements**