---
cssclass:
- t-c
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Speaking Mathematically
**Variables** - used as a placeholder when you want to talk about something but either:
(1) you imagine that it has one or more values but you don't know what they are;
(2) you want whatever you say about it to be equally true for all elements in a given set **e.g.**
> <center>Is there a  number with the following property: doubling it and adding 3 gives the same result as squaring it</center>
> 
> Is there a number $x$ with the property that $2x + 3 = x^2$?

**More examples** (Use variables to rewrite the following sentences more formally)

Are there numbers with with the property that the sum of their squares equals the square of their sum?
>[!CHECK|alt-co collapse ttl-c]
> Are there numbers $a$ and $b$ with the property that $a^2 + b^2 = (a + b)^2$?
> Are there numbers $a$ and $b$ such that $a^2 + b^2 = (a + b)^2$?
> Do there exist any numbers $a$ and $b$ that $a^2 + b^2 = (a + b)^2$?

Given any real number, its square is nonnegative.
>[!CHECK|alt-co collapse ttl-c]
> Given any real number $r$, $r^2$ is nonnegative
> For any real number $r$, $r^2 \ge 0$
> For all real number $r$, $r^2 \ge 0$

<br>

**Universal statement** - says that a certain property is true for all elements in a set e.g., *All positive numbers are greater than zero*
- [[DISCRET12ch1universalconditional|Universal conditional]]
- [[DISCRET12ch1universalexistential|Universal existential]]

**Conditional statement** - says that if one thing is true then some other thing also has to be true e.g., *If 378 is divisible by 18. then 378 is divisible by 6*

**Existential statement** - says that there is at least one thing for which the property is true e.g., *There is a prime number that is even*
- [[DISCRET12ch1existentialuniversal|Existential universal]]

<br>

---
### The Language of Sets
> **Notation**
>- if $S$ is a set, 
>	- the notation $x \in S$ means that $x$ is an element of $S$
>	- the notation $x \notin S$ means that $x$ is not an element of $S$

a **set** may be specified using the **set-roster notation** by writing all of its elements between braces{} e.g.:
- $\{1,2,3\}$ - denotes the set whose elements are 1, 2, and 3
- $\{1,2,3,\dots,100\}$ - set of all integers from 1 to 100
- $\{1,2,3,\dots\}$ - infinite set, set of all positive integers

**<center>Ellipsis (...)</center>**<center>is read "and so forth"</center>

**More examples**

Let $A = \{1 ,2 ,3\}$, $B = \{3 ,1 ,2\}$, and $C = \{1, 1, 2, 3, 3, 3\}$. What are the elements of A, B, and C? How are A, B, and C related?
>[!CHECK|collapse ttl-c]
> ◾ A, B, and C have exactly the same three elements 1, 2, and 3. Therefore, A, B, and C are simply different ways to represent the same set

<br>

Is $\{0\} = 0$?
>[!CHECK|collapse ttl-c]
> ◾ $\{0\} \neq 0$ because $\{0\}$ is a set with one element, namely 0, whereas 0 is just the symbol that represents the number zero

<br>

How many elements are in the set $\{1, \{1\}\}$?
>[!CHECK|collapse ttl-c]
> ◾ The set $\{1, \{1\}\}$ has two elements: 1 and the set whose only element is 1

<br>

For each nonnegative integer $n$, let $U_n = \{n, -n\}$. Find $U_1$, $U_2$, and $U_0$
>[!CHECK|collapse ttl-c]
> ◾ $U_1 = \{1, -1\}$**,** $U_2 = \{2, -2\}$**,** $U_0 = \{0, -0\} = \{0, 0\} = \{0\}$

<br>

---
>[!aside|left collapse]+
> Certain sets of numbers are so frequently referred to that they are given special symbolic names

| <center>Symbol</center> | <center>Set</center>                      |
| ----------------------- | ----------------------------------------- |
| <center>$R$</center>    | set of all real numbers                   |
| <center>$Z$</center>    | set of all integers                       |
| <center>$Q$</center>    | set of all rational numbers, or quotients |

Another way to specify a set uses what is called the:
> **Set-Builder Notation**
>- Let $S$ denote a set and let $P(x)$ be a property that elements of $S$ may or may not satisfy.
>- The set of all elements $x$ in $S$ such that $P(x)$ is true
>
> ![[DISCRET12ch1image0.png|center ws-med]]

**More examples**
Given that $R$ denotes the set of all real numbers, $Z$ the set of all integers, and $Z^+$ the set of all positive integers
>[!CHECK|collapse ttl-c]
> ◾ $\{x\ \in\ R\  |\  -2\ \lt\ x\ \lt\ 5\ \}$, is the open interval of real numbers (strictly) between $-2$ and $5$. It is pictures as follows:
> ![[DISCRET12ch1image1.png|center]]

<br>

Given that $R$ denotes the set of all real numbers, $Z$ the set of all integers, and $Z^+$ the set of all positive integers
>[!CHECK|collapse ttl-c]
> ◾ $\{x\ \in\ Z\  |\  -2\ \lt\ x\ \lt\ 5\ \}$, is the set of all integers (strictly) between $-2$ and $5$. It is equal to the set $\{-1, 0, 1, 2, 3, 4\}$.
> <br>
> ◾ Since all the integers in $Z^+$ are positive, $\{x\ \in\ Z^+\  |\  -2\ \lt\ x\ \lt\ 5\ \}\ =\ \{1, 2, 3, 4\}$.

<br>

---
### Subsets
a basic relation between sets is that of **subset**
>- If $A$ and $B$ are sets
>	- then $A$ is a **subset** of $B$ ($A\ \subseteq\ B$)
>		- if, and only if, every element of $A$ is also an element of $B$
>
>- $A\ \subseteq\ B$ means, *For all elements of $x$, if $x \in A$ then $x \in B$*
>- $A\ \subsetneq\ B$ means, *There is at least one element $x$ such that $x \in A$ and $x \notin B$*

**More examples**
Let $A = Z^+$, $B = \{n \in Z\ |\ 0 \le\ n\ \le\ 100\}$, and $C = \{100,200,300,400,500\}$.
>[!CHECK|collapse ttl-c]
> ◾ $B\ \subseteq\ A$
> **FALSE**. Zero is not a positive integer. Thus zero is in $B$ but zero is not in $A$, and so $B\ \not\subseteq\ A$
> <br>
> ◾ $C$ is a proper subset of $A$
> **TRUE**. Each element in $C$ is a positive integer and hence, is in $A$, but there are elements in $A$ that re not in $C$. For instance, 1 is in $A$ and not in $C$
> <br>
> ◾ $C$ and $B$ have at least one element in common
> **TRUE**. For example, 100 is in both $C$ and $B$
> <br>
> ◾ $C\ \subseteq\ B$
> **FALSE**. For example, 200 is in $C$ but not in $B$
> <br>
> ◾ $C\ \subseteq\ C$
> **TRUE**. Every element in $C$ is in $C$. In general, the definition of subset implies that all sets are subsets of themselves

<br>

---
### Cartesian Products
>- Given sets $A$ and $B$, the **Cartesian product of $A$ and $B$**
>	- $A \times B$ read "A cross B"
>	- is the set of all ordered pairs (a, b)
>		-  where $a$ is in $A$ and $b$ is in $B$
>
> $$A \times B = \{(a, b)\ |\ a \in A\ \ and\ \ b \in B \}$$

**More examples**
Let $A = \{1, 2, 3\}\ \ and\ \ B = \{u, v\}$.
>[!CHECK|collapse ttl-c]
> ◾ $A \times B = \{(1,u), (2,u), (3,u), (1,v), (2,v), (3,v)\}$
> ◾ $B \times A = \{(u,1), (u,2), (u,3), (v,1), (v,2), (v,3)\}$
> ◾ $B \times B = \{(u,u), (u,v), (v,u), (v,v)\}$
> <br>
> ◾ How many elements are in $A \times B$, $B \times A$, and $B \times B$?
> $A \times B$ has six elements. Note that this is the number of elements in $A$ times the number of elements in $B$. $B \times A$ has six elements, the number of elements in $B$ times the number of elements in $A$. $B \times B$ has four elements, the number of elements in $B$ times the number of elements in $B$
> <br>
> ◾ Let $R$ denote the set of all real numbers. Describe $R \times R$
> $R \times R$ is the set of all ordered pairs (x, y) where both $x$ and $y$ are real numbers. If horizontal and vertical axes are drawn on a plane and a unit length is marked off, then each ordered pair in $R \times R$ corresponds to a unique point in the plane, with the first and second elements of the pair indicating, respectively, the horizontal and vertical positions of the point.  The term **Cartesian plane** is often used to refer to a plane with this coordinate system, as illustrated below
> 
> ![[Pasted image 20230207233706.png|center wm-sm]]

<br>

---
### The Language of Relations and Functions
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