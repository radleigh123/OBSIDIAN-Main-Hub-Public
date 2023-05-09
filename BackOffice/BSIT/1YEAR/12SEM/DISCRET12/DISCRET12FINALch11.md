---
cssclass:
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Modus Ponens & Modus Tollens
An argument form consisting of two premises and a conclusion is called a **[[syllogism]]**. The first and second premises are called the **major premise** and **minor premise**, respectively.

The most famous form of syllogism in logic is called **modus ponens**. It has the following form:

$\qquad\qquad\qquad$ If $p$ then $q$.
$\qquad\qquad\qquad$ $p$
$\qquad\qquad\quad\; \therefore$ $q$

Here is an argument of this form:

$\qquad\qquad\qquad$ If the sum of the digits of 371,487 is divisible by 3, then 371,487 is divisible by 3.
$\qquad\qquad\qquad$ The sum of the digits of 371,487 is divisible by 3.
$\qquad\qquad\quad\; \therefore$ 371,487 is divisible by 3.

The term *modus ponens* is Latin meaning “method of affirming” (the conclusion is an affirmation). Long before you saw your first truth table, you were undoubtedly being convinced by arguments of this form. Nevertheless, it is instructive to prove that modus ponens is a valid form of argument, if for no other reason than to confirm the agreement between the formal definition of validity and the intuitive concept. To do so, we construct a truth table for the premises and conclusion.

![[DISCRET12FINALch11image0.png|center wm-tl]]

The first row is the only one in which both premises are true, and the conclusion in that row is also true. Hence the argument form is valid.
$\quad$Now consider another valid argument form called modus tollens. It has the following form:

$\qquad\qquad\qquad$ If $p$ then $q$.
$\qquad\qquad\qquad$ $\lnot q$
$\qquad\qquad\quad\; \therefore$ $\lnot p$

Here is an example of modus tollens:

$\qquad\qquad\qquad$ If Zeus is human, then Zeus is mortal.
$\qquad\qquad\qquad$ Zeus is not mortal.
$\qquad\qquad\quad\; \therefore$ Zeus is not human.

$\quad$An intuitive explanation for the validity of modus tollens uses proof by contradiction. It goes like this:
$\quad$Suppose:

$\qquad\qquad\qquad$ (1) If Zeus is human, then Zeus is mortal; and
$\qquad\qquad\qquad$ (2) Zeus is not mortal.
$\qquad\qquad\qquad$ Must Zeus necessarily be nonhuman?

$\qquad\qquad\qquad$ Yes!
$\qquad\qquad\qquad$ Because, if Zeus were human, then by (1) he would be mortal.
$\qquad\qquad\qquad$ But by (2) he is not mortal.
$\qquad\qquad\qquad$ Hence, Zeus cannot be human.

$\quad$*Modus tollens* is Latin meaning “method of denying” (the conclusion is a denial). The validity of modus tollens can be shown to follow from modus ponens together with the fact that a conditional statement is logically equivalent to its contrapositive. Or it can be established formally by using a truth table. (See exercise 13.)

$\quad$Studies by cognitive psychologists have shown that although nearly 100% of college students have a solid, intuitive understanding of modus ponens, less than 60% are able to apply modus tollens correctly.∗ Yet in mathematical reasoning, modus tollens is used almost as often as modus ponens. Thus it is important to study the form of modus tollens carefully to learn to use it effectively.

**Example: Recognizing Modus Ponens and Modus Tollens**
Use modus ponens or modus tollens to fill in the blanks of the following arguments so that they become valid inferences.
a. If there are more pigeons than there are pigeonholes, then at least two pigeons roost in the same hole.
$\quad$There are more pigeons than there are pigeonholes.
$\quad\therefore$ <u>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</u>
b. If 870,232 is divisible by 6, then it is divisible by 3.
$\quad$ 870,232 is not divisible by 3.
$\quad\therefore$ <u>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</u>

**Solution:**
a. At least two pigeons roost in the same hole. `by modus ponens`
b. 870,232 is not divisible by 6. `by modus ponens`