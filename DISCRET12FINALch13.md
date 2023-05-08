---
cssclass:
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Fallacies
A **fallacy** is an error in reasoning that results in an invalid argument. Three common fallacies are **using ambiguous premises**, and treating them as if they were unambiguous, **circular reasoning** (assuming what is to be proved without having derived it from the premises), and **jumping to a conclusion** (without adequate grounds). In this section we discuss two other fallacies, called *converse error* and *inverse error*, which give rise to arguments that superficially resemble those that are valid by modus ponens and modus tollens but are not, in fact, valid.
$\quad$As in previous examples, you can show that an argument is invalid by constructing a truth table for the argument form and finding at least one critical row in which all the premises are true but the conclusion is false. Another way is to find an argument of the same form with true premises and a false conclusion.

>[!NOTE|no-t alt-co]
> $\quad$For an argument to be valid, every argument of the same form whose premises are all true must have a true conclusion. It follows that for an argument to be invalid means that there is an argument of that form whose premises are all true and whose conclusion is false.

**Example: Converse Error**
Show that the following argument is invalid:

$\qquad\qquad\qquad$ If Zeke is a cheater, then Zeke sits in the back row.
$\qquad\qquad\qquad$ Zeke sits in the back row.
$\qquad\qquad\quad\; \therefore$ Zeke is a cheater.

**Solution:** Many people recognize the invalidity of the above argument intuitively, reasoning something like this: The first premise gives information about Zeke if it is known he is a cheater. It doesn’t give any information about him if it is not already known that he is a cheater. One can certainly imagine a person who is not a cheater but happens to sit in the back row. Then if that person’s name is substituted for Zeke, the first premise is true by default and the second premise is also true but the conclusion is false.
$\quad$The general form of the previous argument is as follows:
$$\displaylines{p\ \to\ q \\ q \\ \therefore p}$$
$\quad$The fallacy underlying this invalid argument form is called the **converse error** because the conclusion of the argument would follow from the premises if the premise $p\ \to\ q$ were replaced by its converse. Such a replacement is not allowed, however, because a conditional statement is not logically equivalent to its converse. Converse error is also known as the *fallacy of affirming the consequent*.
Another common error in reasoning is called the *inverse error*.

**Example: Inverse Error**
Consider the following argument:
$\qquad\qquad\qquad$ If interest rates are going up, stock market prices will go down.
$\qquad\qquad\qquad$ Interest rates are not going up.
$\qquad\qquad\quad\; \therefore$ Stock market prices will not go down.
Note that this argument has the following form:
$$\displaylines{p\ \to\ q \\ \lnot\,p \\ \therefore \lnot\,q}$$
$\quad$The fallacy underlying this invalid argument form is called the **inverse error** because the conclusion of the argument would follow from the premises if the premise $p\ \to\ q$ were replaced by its inverse. Such a replacement is not allowed, however, because a conditional statement is not logically equivalent to its inverse. Inverse error is also known as the *fallacy of denying the antecedent*.

$\quad$Sometimes people lump together the ideas of validity and truth. If an argument seems valid, they accept the conclusion as true. And if an argument seems fishy (really a slang expression for invalid), they think the conclusion must be false. This is not correct!

>[!WARNING]
> In logic, the words true and valid have very different meanings. A valid argument may have a false conclusion, and an invalid argument may have a true conclusion.

**Example: A Valid Argument with a False Premise and a False Conclusion**
The argument below is valid by modus ponens. But its major premise is false, and so is its conclusion.

$\qquad\qquad\qquad$ If John Lennon was a rock star, then John Lennon had red hair.
$\qquad\qquad\qquad$ John Lennon was a rock star.
$\qquad\qquad\quad\; \therefore$ John Lennon had red hair.

**Example: An Invalid Argument with True Premises and a True Conclusion**
The argument below is invalid by the converse error, but it has a true conclusion.

$\qquad\qquad\qquad$ If New York is a big city, then New York has tall buildings.
$\qquad\qquad\qquad$ New York has tall buildings.
$\qquad\qquad\quad\; \therefore$ New York is a big city.

>[!NOTE] Definition
> An argument is called **sound** if, and only if, it is valid and all its premises are true. An argument that is not sound is called **unsound**.

$\quad$The important thing to note is that validity is a property of argument *forms*: If an argument is valid, then so is every other argument that has the same form. Similarly, if an argument is invalid, then so is every other argument that has the same form. What characterizes a valid argument is that no argument whose form is valid can have all true premises and a false conclusion. For each valid argument, there are arguments of that form with all true premises and a true conclusion, with at least one false premise and a true conclusion, and with at least one false premise and a false conclusion. On the other hand, for each invalid argument, there are arguments of that form with every combination of truth values for the premises and conclusion, including all true premises and a false conclusion. The bottom line is that we can only be sure that the conclusion of an argument is true when we know that the argument is sound, that is, when we know both that the argument is valid and that it has all true premises.