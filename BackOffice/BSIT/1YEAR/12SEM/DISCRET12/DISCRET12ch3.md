---
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## The Language of Relations & Functions
>- Let $A$ and $B$ be sets
>- A **relation R from A to B** is a subset of $A \times B$
>- Given an ordered pair (x, y) in $A \times B$, **x is related to y by R**, written $x\ R\ y$
>	- if, and only if, (x, y) is in $R$
>	- The set $A$ is called  the domain of $R$ and set $B$ is called its co-domain

>[!INFO|clean no-t txt-c]
> The notation for a relation $R$ may be written symbolically as follows:
> $x\ R\ y$ means that $(x, y) \in R$
> <br>
> The notation $x\ R\ y$ means that $x$ is not related to $y$ by $R$
> $x\ R\ y$ means that $(x, y) \notin R$

**More examples**
Let $A = \{1, 2\}\ and\ B = \{1, 2, 3\}$ and define a relation $R$ from $A$ to $B$ as follows: Given any $(x, y)\ \in\ A \times B$

>[!INFO|clean no-t txt-c]
$(x, y) \in R$ means that $\frac{x - y}{2}$ is an integer

>[!CHECK|collapse ttl-c]
> ◾ State explicitly which ordered pairs are in $A \times B$ and which are in $R$
> **A x B = {(1, 1), (1, 2). (1, 3), (2, 1), (2, 2), (2, 3)}** To determine explicitly the composition of $R$, examine each ordered pair in $A \times B$ to see whether its elements satisfy the defining condition for $R$
> &nbsp;
>>[!INFO|clean no-t collapse txt-c]
>> $(1, 1)\ \in\ R$ because $\frac{1-1}{2}\ =\ \frac{0}{2}\ =\ 0$, which is an integer
>> $(1, 2)\ \notin\ R$ because $\frac{1-2}{2}\ =\ \frac{-1}{2}$, which is not an integer
>> $(1, 3)\ \in\ R$ because $\frac{1-3}{2}\ =\ \frac{-2}{2}\ =\ -1$, which is an integer
>> $(2, 1)\ \notin\ R$ because $\frac{2-1}{2}\ =\ \frac{1}{2}$, which is not an integer
>> $(2, 2)\ \in\ R$ because $\frac{2-2}{2}\ =\ \frac{0}{2}\ =\ 0$, which is an integer
>> $(2, 3)\ \notin\ R$ because $\frac{2-3}{2}\ =\ \frac{-1}{2}$, which is an integer
>> <br>
>> $R = \{(1, 1), (1, 3), (2, 2)\}$

<br>

Let $A = \{1, 2\}$ and $B = \{1, 2, 3\}$ and define a relation $R$ from $A$ to $B$ as follows: Given any $(x, y)\ \in\ A \times B$
>[!INFO|clean no-t txt-c collapse]
> $(x, y)\ \in\ R$ means  that $\frac{x\ -\ y}{2}$ is an integer

>[!CHECK|collapse ttl-c]
> ◾ Is 1 $R$ 3? Is 2 $R$ 3? Is 2 $R$ 2?
> Yes, 1 $R$ 3 because $(1, 3)\ \in\ R$
> No, 2 $\not\\R$ 3 because $(2, 3)\ \notin\ R$
> Yes, 2 $R$ 2 because $(2, 2)\ \notin\ R$
> <br>
> ◾ What are the domain and co-domain of $R$?
> The domain of $R$ is $\{1, 2\}$ and the co-domain is $\{1, 2, 3\}$

<br>

---
### Functions
- **function** $F$ **from a set A to a set B**
	- is a relation with domain A and co-domain B that satisfies the following two properties
		1. For every element $x$ in $A$, there is an element $y$ in $B$ such that $(x, y)\ \in\ F$
		2. For all elements $x$ in $A$ and $y$ and $z$ in $B$
			- if $(x, y)\ \in\ F$ and $(x, z)\ \in\ F$, then $y\ =\ z$

- **Notation**
- If A and B are sets and F is a function
	- from A to B the given any element x in A, the unique element in B that is related to x by F is denoted $F(x)$, which is read "**F of x**"

>[!INFO|alt-co] Function
> a relation in which every input has exactly one output

**More examples**
Let $A = \{2, 4, 6\}$ and $B = \{1, 3, 5\}$. Which of the relations $R$, $S$, and $T$ defined below are function from A to B
>[!CHECK|collapse ttl-c]
> ◾ $R = \{(2, 5), (4, 1), (4, 3), (6, 5)\}$
> <br>
> ◾ For all $(x, y)\ \in\ A \times B$, $(x, y)\ \in\ S$ means that $y\ =\ x\ +\ 1$
> <br>
> ◾ $T$ is defined by the arrow diagram