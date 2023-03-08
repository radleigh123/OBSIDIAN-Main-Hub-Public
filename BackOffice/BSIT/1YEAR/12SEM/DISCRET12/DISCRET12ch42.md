---
cssclass:
- t-c
- tbl-nalt
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Truth Values
In [[DISCRET12ch41#^c09ed1|Examples 4.1]] and [[DISCRET12ch41sample0|4.2]] we built compound sentences out of component statements and the terms **not**, **and**, and **or**. If such sentences are to be statements, however, they must have well-defined ***truth values*** — they must be either true or false. We now define such compound sentences as statements by specifying their truth values in terms of the statements that compose them.

> The negation of a statement is a statement that exactly expresses what it would mean for the statement to be false.

>[!NOTE|collapse alt-co] NOTE
> If $p$ is a statement variable, the **negation** of $p$ is “not p” or “It is not the case that p” and is denoted $\lnot p$. It has opposite truth value from $p$: if $p$ is true, $\lnot p$ is false; if $p$ is false, $\lnot p$ is true.

The truth values for negation are summarized in a truth table:

| **p**          | **~p**    |
| ------------ | ------------ |
| $\mathrm{T}$ | $\mathrm{F}$ |
| $\mathrm{F}$ | $\mathrm{T}$ | 

In ordinary language the sentence “It is hot and it is sunny” is understood to be true when both conditions — *being hot and being sunny* — are satisfied. If it is hot but not sunny, or sunny but not hot, or neither hot nor sunny, the sentence is understood to be false. The formal definition of truth values for an **and** statement agrees with this general understanding.

>[!NOTE|collapse alt-co] NOTE
> If $p$ and $q$ are statement variables, the **conjunction** of $p$ and $q$ is “p and q,” denoted $p ∧ q$. It is true when, and only when, both $p$ and $q$ are true. If either $p$ or $q$ is **false**, or if both are false, $p ∧ q$ is **false**.

The truth values for conjunction can also be summarized in a truth table. The table is obtained by considering the four possible combinations of truth values for $p$ and $q$. Each combination is displayed in one row of the table; the corresponding truth value for the whole statement is placed in the right-most column of that row. Note that the only row containing a $\mathrm{T}$ is the first one since the only way for an and statement to be true is for both component statements to be true.

| **p&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;q** | **p ∧ q**    |
| ------------------------------------------------------------------------------------------------------ | ------------ |
| $\mathrm{T}$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\mathrm{T}$       | $\mathrm{T}$ |
| $\mathrm{T}$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\mathrm{F}$       | $\mathrm{F}$ |
| $\mathrm{F}$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\mathrm{T}$       | $\mathrm{F}$ |
| $\mathrm{F}$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\mathrm{F}$       | $\mathrm{F}$ |

By the way, the order of truth values for p and q in the table above is **TT**, **TF**, **FT**, **FF**. It is not absolutely necessary to write the truth values in this order, although it is customary to do so. We will use this order for all truth tables involving two statement variables. In [[DISCRET12ch42sample1|Example 42.2]] we will show the standard order for truth tables that involve three statement variables.

In the case of disjunction—statements of the form “p or q”—intuitive logic offers two alternative interpretations. In ordinary language **or** is sometimes used in an exclusive sense ($p\ \mathit{or}\ q\ \mathit{but\ not\ both}$) and sometimes in an inclusive sense ($p\ \mathit{or}\ q\ \mathit{or\ both}$). A waiter who says you may have “*coffee, tea, or milk*” uses the word **or** in an exclusive sense: Extra payment is generally required if you want more than one beverage. On the other hand, a waiter who offers “*cream or sugar*” uses the word **or** in an inclusive sense: You are entitled to both cream and sugar if you wish to have them.

Mathematicians and logicians avoid possible ambiguity about the meaning of the word **or** by understanding it to mean the inclusive “**and/or**.” The symbol $\boldsymbol{∨}$ comes from the Latin word *vel*, which means **or** in its inclusive sense. To express the exclusive **or**, the phrase $p\ \mathit{or}\ q\ \mathit{but\ not\ both}$ is used.

>[!NOTE|collapse alt-co] NOTE
> If $p$ and $q$ are statement variables, the **disjunction** of $p$ and $q$ is “p or q,” denoted $p ∨ q$. It is true when either $p$ is **true**, or $q$ is **true**, or both $p$ and $q$ are **true**; it is **false** only when both $p$ and $q$ are **false**.

>[!aside|show-title left c-green]+ LIL NOTE
> The statement "$2 \le 2$" means that 2 is less than 2 or 2 equals 2. It is **true** because $2 = 2$

Here is the truth table for disjunction:

| **p&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;q** | **p ∧ q**    |
| ------------------------------------------------------------------------------------------------------ | ------------ |
| $\mathrm{T}$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\mathrm{T}$       | $\mathrm{T}$ |
| $\mathrm{T}$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\mathrm{F}$       | $\mathrm{T}$ |
| $\mathrm{F}$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\mathrm{T}$       | $\mathrm{T}$ |
| $\mathrm{F}$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\mathrm{F}$       | $\mathrm{F}$ |

<br>

#### Evaluating the Truth of More General Compound Statements
Now that truth values have been assigned to $∼p$, $p ∧ q$, and $p ∨ q$, consider the question of assigning truth values to more complicated expressions such as $∼p ∨ q$, $(p ∨ q) ∧ ∼(p ∧ q)$, and $(p ∧ q) ∨ r$. Such expressions are called **statement forms** (or **propositional forms**). The close relationship between statement forms and **[[DISCRET12ch45|Boolean expressions]]**.

>[!NOTE|alt-co] DEFINITION
> A **statement form** (or **propositional form**) is an expression made up of statement variables (such as $p$, $q$, and $r$) and logical connectives (such as $∼,$ $∧,$ and $∨)$ that becomes a statement when actual statements are substituted for the component statement variables. The **truth table** for a given statement form displays the truth values that correspond to all possible combinations of truth values for its component statement variables.

To compute the truth values for a statement form, follow rules similar to those used to evaluate algebraic expressions. For each combination of truth values for the statement variables, first evaluate the expressions within the innermost parentheses, then evaluate the expressions within the next innermost set of parentheses, and so forth until you have the truth values for the complete expression.

<br>

---
**Truth Table for *Exclusive Or* Examples:**
- [[DISCRET12ch42sample|Example 42.1]]

**Truth Table for ( p ∧ q) ∨ ∼r**
- [[DISCRET12ch42sample1|Example 42.2]]