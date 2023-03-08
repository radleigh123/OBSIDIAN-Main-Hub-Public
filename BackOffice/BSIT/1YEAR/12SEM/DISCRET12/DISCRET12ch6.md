---
cssclass:
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Conditional Statements
>[!CITE] ... hypothetical reasoning implies the subordination of the real to the realm of the possible ... — Jean Piaget, 1972

When you make a logical inference or deduction, you reason from a hypothesis to a conclusion. Your aim is to be able to say, “*If such and such is known, then something or other must be the case*.”

Let $p$ and $q$ be statements. A sentence of the form “***If $\ p\;$ then $\ q$***” is denoted symbolically by “**$p → q$**”; $p$ is called the hypothesis and $q$ is called the conclusion. For instance, consider the following statement:
![[DISCRET12ch6image.png|center]]

Such a sentence is called conditional because the truth of statement $q$ is conditioned on the truth of statement $p$.

The notation $p → q$ indicates that $→$ is a connective, like $∧$ or $∨$, that can be used to join statements to create new statements. To define $p → q$ as a statement, therefore, we must specify the truth values for $p → q$ as we specified truth values for $p\ ∧ q$ and for $p\ ∨ q$. As is the case with the other connectives, the formal definition of truth values for $→$ (**if-then**) is based on its everyday, intuitive meaning. Consider an example.
>[!INFO|clean alt-co collapse no-t]
> Suppose you go to interview for a job at a store and the owner of the store makes you the following promise:
> &nbsp;
> &nbsp;
> <center>If you show up for work Monday morning, then you will get the job.</center>
> &nbsp;
> 
> Under what circumstances are you justified in saying the owner spoke falsely? That is, under what circumstances is the above sentence false? The answer is: You **do** show up for work Monday morning and you do **not** get the job.
> After all, the owner’s promise only says you will get the job **if** a certain condition (showing up for work Monday morning) is met; it says nothing about what will happen if the condition is **not** met. So if the condition is not met, you cannot in fairness say the promise is false regardless of whether or not you get the job.

The above example was intended to convince you that *the only combination of circumstances in which you would call a conditional sentence false occurs when the hypothesis is true and the conclusion is false*. In all other cases, you would not call the sentence false. This implies that the only row of the truth table for $p → q$ that should be filled in with an F is the row where $p$ is T and $q$ is F. No other row should contain an F. But each row of a truth table must be filled in with either a T or an F. Thus all other rows of the truth table for $p → q$ must be filled in with T’s.

![[DISCRET12ch6image1.png|center]]

>[!INFO|alt-co collapse] DEFINITION
> If $p$ and $q$ are statement variables, the **conditional** of $q$ by $p$ is “*If p then q” or “p implies q*” and is denoted $p → q$. It is false when $p$ is true and $q$ is false; otherwise it is true. We call $p$ the **hypothesis** (or **antecedent**) of the conditional and $q$ the **conclusion** (or **consequent**)

A conditional statement that is true by virtue of the fact that its hypothesis is false is often called **vacuously true** or **true by default**. Thus the statement “*If you show up for work Monday morning, then you will get the job*” is vacuously true if you do not show up for work Monday morning. In general, when the “*if*” part of an if-then statement is false, the statement as a whole is said to be true, regardless of whether the conclusion is true or false.

[[DISCRET12ch6Example1|Example 6.1]]: **A Conditional Statement with a False Hypothesis**
[[DISCRET12ch6Example2|Example 6.2]]:  **Truth Table for p ∨ ∼q → ∼p**