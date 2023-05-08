---
cssclass:
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Additional Valid Argument Forms: Rules of Inference
A **rule of inference** is a form of argument that is valid. Thus modus ponens and modus tollens are both rules of inference. The following are additional examples of rules of inference that are frequently used in deductive reasoning.

**Example: Generalization**
The following argument forms are valid:
>[!column|clean no-t collapse]
>>[!INFO|clean no-t]
>> a. $\quad\ p$
>> $\quad \therefore\ p\ \lor\ q$
>
>>[!INFO|clean no-t]
>> b. $\quad\ q$
>> $\quad \therefore\ p\ \lor\ q$

$\quad$These argument forms are used for making generalizations. For instance, according to the first, if $p$ is true, then, more generally, “p or q” is true for any other statement $q$. As an example, suppose you are given the job of counting the upperclassmen at your school. You ask what class Anton is in and are told he is a junior.

You reason as follows:
$\qquad\quad$ Anton is a junior
$\qquad\therefore$ (more generally) Anton is a junior or Anton is a senior.

Knowing that upperclassman means junior or senior, you add Anton to your list.

**Example: Specialization**
The following argument forms are valid:
>[!column|clean no-t collapse]
>>[!INFO|clean no-t]
>> a. $\quad\ p\ \land\ q$
>> $\quad \therefore\ p$
>
>>[!INFO|clean no-t]
>> b. $\quad\ p\ \land\ q$
>> $\quad \therefore\ q$

These argument forms are used for specializing. When classifying objects according to some property, you often know much more about them than whether they do or do not have that property. When this happens, you discard extraneous information as you concentrate on the particular property of interest.
$\quad$For instance, suppose you are looking for a person who knows graph algorithms to work with you on a project. You discover that Ana knows both numerical analysis and graph algorithms. You reason as follows:

$\qquad$ Ana knows numerical analysis and Ana knows graph algorithms.
$\quad \therefore$ (in particular) Ana knows graph algorithms.

Accordingly, you invite her to work with you on your project.

$\quad$Both generalization and specialization are used frequently in mathematics to tailor facts to fit into hypotheses of known theorems in order to draw further conclusions. Elimination, transitivity, and proof by division into cases are also widely used tools

**Example: Elimination**
The following argument forms are valid:
>[!column|clean no-t collapse]
>>[!INFO|clean no-t]
>> a. $\quad\ p\ \lor\ q$
>> $\quad\ \ \ \lnot\, q$
>> $\quad \therefore\; p$
>
>>[!INFO|clean no-t]
>> b. $\quad\ p\ \lor\ q$
>> $\quad\ \ \ \lnot\, p$
>> $\quad \therefore\; q$

These argument forms say that when you have only two possibilities and you can rule one out, the other must be the case. For instance, suppose you know that for a particular number $x$,
$$x - 3 = 0\quad \mathsf{or}\quad x + 2 = 0$$
If you also know that x is not negative, then $x = −2$, so
$$x + 2 \neq 0$$
By elimination, you can then conclude that
$$\therefore x - 3 = 0$$

**Example: Transitivity**
The following argument form is valid:
$$\displaylines{p\ \to\ q \\ q\ \to\ r \\ \therefore\ p\ \to\ r}$$
Many arguments in mathematics contain chains of if-then statements. From the fact that one statement implies a second and the second implies a third, you can conclude that the first statement implies the third. Here is an example:
$\quad$ If 18,486 is divisible by 18, then 18,486 is divisible by 9.
$\quad$ If 18,486 is divisible by 9, then the sum of the digits of 18,486 is divisible by 9.
$\; \therefore$ If 18,486 is divisible by 18, then the sum of the digits of 18,486 is divisible by 9.

**Example: Proof by Division into Cases**
The following argument form is valid:
$$\displaylines{p\ \lor\ q \\ p\ \to\ r \\ q\ \to\ r \\ \therefore r}$$

It often happens that you know one thing or another is true. If you can show that in either case a certain conclusion follows, then this conclusion must also be true. For instance, suppose you know that x is a particular nonzero real number. The trichotomy property of the real numbers says that any number is positive, negative, or zero. Thus (by elimination) you know that x is positive or x is negative. You can deduce that $x^2 \gt 0$ by arguing as follows:

$\qquad$ $x$ is positive or x is negative.
$\qquad$ If $x$ is positive, then $x^2 \gt 0$.
$\qquad$ If $x$ is negative, then $x^2 \gt 0$.
$\qquad$ $x^2 \gt 0$

The rules of valid inference are used constantly in problem solving. Here is an example from everyday life.

**Example: Application: A More Complex Deduction**
You are about to leave for school in the morning and discover that you don’t have your glasses. You know the following statements are true:
a. If I was reading the newspaper in the kitchen, then my glasses are on the kitchen table.
b. If my glasses are on the kitchen table, then I saw them at breakfast.
c. I did not see my glasses at breakfast.
d. I was reading the newspaper in the living room or I was reading the newspaper in the kitchen.
e. If I was reading the newspaper in the living room then my glasses are on the coffee table.

Where are the glasses?
**Solution:** Let $\mathit{RK}\ =$ I was reading the newspaper in the kitchen.
$\qquad\qquad\ \ \,$ $\mathit{GK}\ =$ My glasses are on the kitchen table.
$\qquad\qquad\ \ \,$ $\mathit{SB}\ =$ I saw my glasses at breakfast.
$\qquad\qquad\ \ \,$ $\mathit{RL}\ =$ I was reading the newspaper in the living room.
$\qquad\qquad\ \ \,$ $\mathit{GC}\ =$ My glasses are on the coffee table.

Here is a sequence of steps you might use to reach the answer, together with the rules of inference that allow you to draw the conclusion of each step:
![[DISCRET12FINALch12image0.png|center wm-sm]]