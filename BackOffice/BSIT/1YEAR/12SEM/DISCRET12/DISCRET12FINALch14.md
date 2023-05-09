---
cssclass:
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Contradictions and Valid Arguments
The concept of logical contradiction can be used to make inferences through a technique of reasoning called the *contradiction rule*. Suppose $p$ is some statement whose truth you wish to deduce.
>[!CHECK|no-i ttl-c alt-co] Contradiction Rule
> If you can show that the supposition that statement $p$ is false leads logically to a contradiction, then you can conclude that $p$ is true.

**Example: Contradiction Rule**
Show that the following argument form is valid:

$\qquad\qquad\qquad$ $\lnot\,p\ \to\ \mathbb{c}$., where $\mathbb{c}$ is a contradiction
$\qquad\qquad\quad\; \therefore$ $p$

**Solution:** Construct a truth table for the premise and the conclusion of this argument.
![[DISCRET12FINALch14image0.png|center wtall]]

$\quad$The contradiction rule is the logical heart of the method of proof by contradiction. A slight variation also provides the basis for solving many logical puzzles by eliminating contradictory answers: *If an assumption leads to a contradiction, then that assumption must be false.*

**Example: Knights and Knaves**
The logician *Raymond Smullyan* describes an island containing two types of people: knights who always tell the truth and knaves who always lie.∗ You visit the island and are approached by two natives who speak to you as follows:

$\qquad\qquad\qquad$ $\mathit{A}$ says: $\mathit{B}$ is a knight.
$\qquad\qquad\qquad$ $\mathit{B}$ says: $\mathit{A}$ and I are of opposite type.

What are $\mathit{A}$ and $\mathit{B}$ ?

**Solution:** $\mathit{A}$ and $\mathit{B}$ are both knaves. To see this, reason as follows:

$\quad$ Suppose $\mathit{A}$ is a knight.

![[DISCRET12FINALch14image1.png]]

This reasoning shows that if the problem has a solution at all, then $\mathit{A}$ and $\mathit{B}$ must both be knaves. It is conceivable, however, that the problem has no solution. The problem statement could be inherently contradictory. If you look back at the solution, though, you can see that it does work out for both $\mathit{A}$ and $\mathit{B}$ to be knaves