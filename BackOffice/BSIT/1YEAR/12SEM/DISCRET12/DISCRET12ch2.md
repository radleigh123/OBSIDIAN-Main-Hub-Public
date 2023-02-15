---
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## The Language of Sets
> **Notation**
>- if $S$ is a set, 
>	- the notation $x \in S$ means that $x$ is an element of $S$
>	- the notation $x \notin S$ means that $x$ is not an element of $S$

a **set** may be specified using the **set-roster notation** by writing all of its elements between braces{} e.g.:
>[!aside|right]+
> The **cardinality**(size) of set $\{1, 2, 3\}$ is 3
> $$|{1, 2, 3}|\ = 3$$

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