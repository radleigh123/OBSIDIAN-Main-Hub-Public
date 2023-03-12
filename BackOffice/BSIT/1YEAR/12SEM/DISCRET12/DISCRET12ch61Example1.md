---
cssclass:
aliases:
tags:
---
**[[DISCRET12ch61|BACK]]**

---
## Example 61.1: Division into Cases: Showing that p ∨ q → r ≡ ( p → r) ∧ (q → r)
Use truth tables to show the logical equivalence of the statement forms $p\ \ ∨ q → r$ and $(p → r)\ \ ∧ (q → r)$. Annotate the table with a sentence of explanation.

**Solution:**
First fill in the eight possible combinations of truth values for $p$, $q$, and $r$. Then fill in the columns for $p\ ∨ q$, $p → r$, and $q → r$ using the definitions of **or** and **if-then**. For instance, the $p → r$ column has **F**’s in the second and fourth rows because these are the rows in which $p$ is **true** and $q$ is **false**. Next fill in the $p ∨ q → r$ column using the definition of **if-then**. The rows in which the hypothesis $p ∨ q$ is **true** and the conclusion $r$ is **false** are the second, fourth, and sixth. So **F**’s go in these rows and **T**’s in all the others. The complete table shows that $p\ ∨ q → r\quad \text{and}\quad (p → r)\ ∧ (q → r)$ have the same truth values for each combination of truth values of $p$, $q$, and $r$. Hence the two statement forms are logically equivalent.

![[DISCRET12ch61Example1image.png|center wtall]]