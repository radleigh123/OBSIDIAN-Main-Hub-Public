---
cssclass:
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Summary of Logical Equivalences
Knowledge of logically equivalent statements is very useful for constructing arguments. It often happens that it is difficult to see how a conclusion follows from one form of a statement, whereas it is easy to see how it follows from a logically equivalent form of the statement. A number of logical equivalences are summarized in Theorem 2.1.1 for future reference. It is below:

![[DISCRET12ch52image.png|wtall center]]

The proofs of laws **4** and **6**, the first parts of laws **1** and **5**, and the second part of law **9** have already been given as examples in the text. Proofs of the other parts of the theorem are left as exercises. In fact, it can be shown that the first five laws of *Theorem 2.1.1* form a core from which the other laws can be derived. The first five laws are the axioms for a mathematical structure known as a **[[DISCRET12BooleanAlgebra|Boolean algebra]]**. The equivalences of *Theorem 2.1.1* are general laws of thought that occur in all areas of human endeavor. They can also be used in a formal way to rewrite complicated statement forms more simply.

Example 52.1: **Simplifying Statement Forms**
Use Theorem 2.1.1 to verify the logical equivalence
$$\lnot(\lnot p\ \land\ q)\ \land\ (p\ \lor\ q) \equiv p$$

**Solution:**
Use the laws of *Theorem 2.1.1* to replace sections of the statement form on the left by logically equivalent expressions. Each time you do this, you obtain a logically equivalent statement form. Continue making replacements until you obtain the statement form on the right.

![[DISCRET12ch52image1.png|center]]

Skill in simplifying statement forms is useful in constructing logically efficient computer programs and in designing digital logic circuits. Although the properties in *Theorem 2.1.1* can be used to prove the logical equivalence of two statement forms, they cannot be used to prove that statement forms are not logically equivalent.

On the other hand, truth tables can always be used to determine both equivalence and nonequivalence, and truth tables are easy to program on a computer. When truth tables are used, however, checking for equivalence always requires $2^{\text{n}}$ steps, where $n$ is the number of variables. Sometimes you can quickly see that two statement forms are equivalent by *Theorem 2.1.1*, whereas it would take quite a bit of calculating to show their equivalence using truth tables. For instance, it follows immediately from the associative law for $∧$ that $p ∧ (∼q\ \ ∧ ∼r) ≡ (p ∧\ \ ∼q)\ \ ∧ ∼r$, whereas a truth table verification requires constructing a table with eight rows.