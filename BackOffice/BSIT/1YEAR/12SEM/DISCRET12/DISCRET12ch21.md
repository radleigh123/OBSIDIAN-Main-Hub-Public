---
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Subsets
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