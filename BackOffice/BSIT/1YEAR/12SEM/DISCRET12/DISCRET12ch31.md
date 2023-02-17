---
aliases:
tags:
---
**[[DISCRET12|MAINHUB]]**

---
## Function Machines
> Another useful way to think of a function is as a machine

Suppose $f$ is a function from $X$ to $Y$ and an input $x$ of $X$ is given. Imagine $f$ to be a machine that processes $x$ in a certain way to produce the output $f(x)$.

![[DISCRET12ch31image0.png|center]]

<br>

The **squaring function** $f$ from $R$ to $R$ is defined by the formula $f(x) = x^2$ for all real numbers $x$. This means that no matter what real number input is substituted for $x$, the output of $f$ will be the square of that number. This idea can be represented by writing $f(\fbox{}) = \fbox{}^2$. In other words, $f$ sends each real number $x$ to $x^2$, or, symbolically, $f:x \to x^2$. Note that the variable $x$ is a dummy variable; any other symbol could replace it, as long as the replacement is made everywhere the $x$ appears.

![[DISCRET12ch31image1.png|center]]

The **successor function** $g$ from $Z$ to $Z$ is defined by the formula $g(n) = n + 1$. Thus, no matter what integer is substituted for $n$, the output of $g$ will be that number plus one: $g(\fbox{}) = \fbox{} + 1$. In other words, $g$ sends each integer $n$ to $n + 1$, or, symbolically, $g:n \to n + 1$.

![[DISCRET12ch31image2.png|center]]

An example of a **constant function** is the function $h$ from $Q$ to $Z$ defined by the formula $h(r) = 2$ for all rational numbers $r$. This function sends each rational number $r$ to $2$. In other words, no matter what the input, the output is always $2:h(\fbox{}) = 2$ or $h:r \to 2$.

![[DISCRET12ch31image3.png|center]]

<br>

---
A function is an entity in its own right. It can be thought of as a certain relationship between sets or as an input/output machine that operates according to a certain rule. This is the reason why a function is generally denoted by a single symbol or string of symbols, such as $f$, $G$, of $\log$, or $\sin$.

A relation is a subset of a Cartesian product and a function is a special kind of relation. Specifically, if $f$ and $g$ are functions from a set $A$ to a set $B$, then
$$f = \{(x, y) \in A \times B\ |\ y = f(x)\}\quad \text{and}\quad g = \{(x, y) \in A \times B\ |\ y = g(x)\}$$
It follows that
$$\fbox{f equals g,\quad written f = g,\quad if, and only if,\quad f(x) = g(x) for all x in A}
$$

Define $f:R \to R$ and $g:R \to R$ by the following formulas:
$$f(x) = |x|\quad \text{for all}\ x \in R$$
$$g(x) = \sqrt{x^2}\quad \text{for all}\ x \in R$$

Does $f = g$?
Yes. Because the absolute value of any real number equals the square root of its square, $|x| = \sqrt{x^2}\quad \text{for all}\ \ x \in R$. Hence $f = g$.