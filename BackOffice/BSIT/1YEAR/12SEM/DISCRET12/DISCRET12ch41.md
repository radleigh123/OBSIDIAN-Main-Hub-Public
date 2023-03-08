---
cssclass:
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Statements (or Proposition)
Most of the definitions of formal logic have been developed so that they agree with the natural or intuitive logic used by people who have been educated to think clearly and use language carefully. The differences that exist between formal and intuitive logic are necessary to avoid ambiguity and obtain consistency.

In any mathematical theory, new terms are defined by using those that have been previously defined. However, this process has to start somewhere. A few initial terms necessarily remain undefined. In logic, the words ***sentence***, ***true***, and ***false*** are the initial undefined terms.

>[!INFO|alt-co clean no-i ttl-c txt-c] statement (or <u>proposition</u>) 
> \- a sentence that is true or false but not both.

>[!EXAMPLE|alt-co] EXAMPLE
> “*Two plus two equals four*” and “*Two plus two equals five*” are both statements, the first because it is true and the second because it is false. 

On the other hand, the truth or falsity of “*He is a college student*” depends on the reference for the pronoun *he*. For some values of he the sentence is true; for others it is false. If the sentence were preceded by other sentences that made the pronoun’s reference clear, then the sentence would be a statement. Considered on its own, however, the sentence is neither true nor false, and so it is not a statement (Learn more, [[DISCRET12ch9|Quantified Statements]]).

Similarly, “$x + y\ >\ 0$” is not a statement because for some values of x and y the sentence is true, whereas for others it is false. For instance, if $x = 1\ \ \text{and}\ \ y = 2$, the sentence is $true$; if $x = −1\ \ \text{and}\ \ y = 0$, the sentence is $false$.

<br>

### Compound Statements
The symbol $\boldsymbol{\sim}$ (or $\boldsymbol{\lnot}$ ) denotes ***not***
>[!INFO|clean no-t collapse alt-co]
> Given a statement $p$, the sentence “$\lnot p$” is read “**not p**” or “**It is not the case that p**” and is called **the negation of p**.

The symbol $\boldsymbol{\land}$ denotes ***and***
>[!INFO|clean no-t collapse alt-co]
> Given another statement $q$, the sentence "$p\ \land\  q$" is read “**p and q**” and is called **the conjunction of p and q**.

The symbol $\boldsymbol{\lor}$ denotes ***or***
>[!INFO|clean no-t collapse alt-co]
> The sentence “$p\ \lor\ q$” is read “**p or q**” and is called **the disjunction of p and q**.

<br>

>[!WARNING|ttl-c no-i] In expressions that include the symbol $\boldsymbol{\sim}$ as well as $\boldsymbol{\land}$ or $\boldsymbol{\lor}$, the order of operations specifies that <u>$\boldsymbol{\sim}$ is performed first</u>.

<br>

For instance, $\lnot p \land q\ =\ (\lnot p) \land q$. In logical expressions, as in ordinary algebraic expressions, the order of operations can be overridden through the use of parentheses. Thus $\lnot (p \land q)$ represents the negation of the conjunction of $p$ and $q$. In this, as in most treatments of logic, the symbols $\boldsymbol{\land}$ and $\boldsymbol{\lor}$ are considered coequal in order of operation, and an expression such as $p ∧ q ∨ r$ is considered ambiguous. This expression must be written as either $(p ∧ q) ∨ r\;$ or $\ p ∧ (q ∨ r)$ to have meaning.

A variety of English words translate into logic as $\boldsymbol{∧}$, $\boldsymbol{∨}$, or $\boldsymbol{∼}$. For instance, the word but translates the same as and when it links two independent clauses, as in “*Jim is tall but he is not heavy*.” Generally, the word **but** is used in place of and <mark class="hltr-lightgreen">when the part of the sentence that follows is, in some way, unexpected</mark>. Another example involves the words **neither-nor**. When Shakespeare wrote, “*Neither a borrower nor a lender be*,” he meant, “*Do not be a borrower and do not be a lender*.” So if $p$ and $q$ are statements, then
$$p\ \text{but}\ q\quad \quad \quad \quad \text{means}\quad p\ \text{and}\ q$$
$$\text{neither}\ p\ \text{nor}\ q\quad \quad \text{means}\quad \lnot p\ \text{and}\ \lnot q$$

Examples: Write each of the following sentences symbolically, letting $h$ = “It is hot” and $s$ = “It is sunny.”
**a.** It is not hot but it is sunny.
The given sentence is equivalent to “<mark class="hltr-lightgreen">It is not hot and it is sunny,</mark>”. $\lnot h ∧ s$. ^c09ed1

**b.** It is neither hot nor sunny.
To say it is neither hot nor sunny means that <mark class="hltr-lightgreen">it is not hot and it is not sunny</mark>. $\lnot h\ ∧ \lnot s$

<br>

The notation for inequalities involves **and** and **or** statements. For instance, if $x$, $a$, and $b$ are particular $\mathsf{real\ numbers}$, then:
$$\displaylines{x \le a\qquad \qquad \text{means}\quad x \lt a\quad \text{or}\quad x = a\\a \le x \le b\qquad \text{means}\quad a \le x\quad \text{and}\quad x \le b}$$
Note that the inequality $2 ≤ x ≤ 1$ is not satisfied by any real numbers because
$$2 \le x \le 1\qquad \text{means}\quad 2 \le x\quad \text{and}\quad x \le 1$$
and this is false no matter what number $x$ happens to be. By the way, the point of specifying $x$, $a$, and $b$ to be particular $\mathsf{real\ numbers}$ is to ensure that sentences such as “$x < a$” and “$x ≥ b$” are either **true** or **false** and hence that they are statements.

Example: [[DISCRET12ch41sample0|And, Or, and Inequalities]] ^05fa3c

<br>

# 
---
**[[DISCRET12ch42|Truth Values]]**