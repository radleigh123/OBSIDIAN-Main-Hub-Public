---
cssclass:
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Valid and Invalid Arguments
> "Contrariwise,” continued Tweedledee, “if it was so, it might be; and if it were so, it would be; but as it isn’t, it ain’t. That’s logic."
> \- Lewis Carroll, Through the Looking Glass

In mathematics and logic an argument is not a dispute. It is a sequence of statements ending in a conclusion. In this section we show how to determine whether an argument is valid—that is, whether the conclusion follows *necessarily* from the preceding statements. We will show that this determination depends only on the form of an argument, not on its content.

It was shown in Section 2.1 that the logical form of an argument can be abstracted from its content. For example, the argument

$\qquad\qquad\qquad$ If Socrates is a man, then Socrates is mortal
$\qquad\qquad\qquad$ Socrates is a man.
$\qquad\qquad\quad\; \therefore$ Socrates is mortal.

has the abstract form

$\qquad\qquad\qquad$ If $p$ then $q$
$\qquad\qquad\qquad$ $p$
$\qquad\qquad\quad\; \therefore$ $q$

When considering the abstract form of an argument, think of $p$ and $q$ as variables for which statements may be substituted. An argument form is called **valid** if, and only if, whenever statements are substituted that make all the premises true, the conclusion is also true.

>[!NOTE] Definition
> An **argument** is a sequence of statements, and an **argument form** is a sequence of statement forms. All statements in an argument and all statement forms in an argument form, except for the final one, are called **premises** (or **assumptions** or **hypotheses**). The final statement or statement form is called the **conclusion**. The symbol **$∴$**, which is read “therefore,” is normally placed just before the conclusion. To say that an *argument form* is **valid** means that no matter what particular statements are substituted for the statement variables in its premises, if the resulting premises are all true, then the conclusion is also true. To say that an argument is **valid** means that its form is valid.

The crucial fact about a valid argument is that the truth of its conclusion follows *necessarily* or *inescapably* or *by logical form alone* from the truth of its premises. It is impossible to have a valid argument with true premises and a false conclusion. When an argument is valid and its premises are true, the truth of the conclusion is said to be inferred or deduced from the truth of the premises. If a conclusion “ain’t necessarily so,” then it isn’t a valid deduction.

>[!EXAMPLE|ttl-c]+ Testing an Argument Form for Validity
>1. Identify the premises and conclusion of the argument form.
>2. Construct a truth table showing the truth values of all the premises and the conclusion.
>3. A row of the truth table in which all the premises are true is called a critical row. If there is a critical row in which the conclusion is false, then it is possible for an argument of the given form to have true premises and a false conclusion, and so the argument form is invalid. If the conclusion in every critical row is true, then the argument form is valid.

**Example: Determining Validity or Invalidity**
Determine whether the following argument form is valid or invalid by drawing a truth table, indicating which columns represent the premises and which represent the conclusion, and annotating the table with a sentence of explanation. When you fill in the table, you only need to indicate the truth values for the conclusion in the rows where all the premises are true (the critical rows) because the truth values of the conclusion in the other rows are irrelevant to the validity or invalidity of the argument.
$$\displaylines{p\ \to\ q\ \lor\ \lnot r \\ q\ \to\ p\ \land\ r \\ p\ \to\ r}$$
**Solution:** The truth table shows that even though there are several situations in which the premises and the conclusion are all true (rows 1, 7, and 8), there is one situation (row 4) where the premises are true and the conclusion is false.

![[DISCRET12FINALch1image0.png|center wfull]]