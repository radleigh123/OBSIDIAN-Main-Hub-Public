---
aliases:
tags:
---
**[[BackOffice/BSIT/1YEAR/12SEM/DISCRET12/DISCRET12ch3|BACK]]**

---
## Functions and Relations on Sets of Real Numbers
a. In Example 1.3.2 the circle relation C was defined as follows:

Is $C$ a function? If it is, find $C(0)$ and $C(1)$.
$$\text{For all}\ (x,\ y) \in R \times R,\ \ (x,\ y) \in C\ \ \text{means that}\ x^2 + y^2 = 1$$
The graph of $C$, shown on the next page, indicates that $C$ does not satisfy either function property. To see why $C$ does not satisfy property (1), observe that there are many real numbers $x$ such that $(x, y) \in C$ for any $y$.
![[DISCRET12ch3sample0image1.png|center]]
For instance, when $x = 2$, there is no real number $y$ so that
$$x^2 + y^2 = 2^2 + y^2 = 4 + y^2 = 1$$
because if there were, then it would have to be true that
$$y^2 = −3$$
which is not the case for any real number y. To see why $C$ does not satisfy property (2), note that for some values of $x$ there are two distinct values of $y$ so that $(x, y) \in C$. One way to see this graphically is to observe that there are vertical lines, such as $\frac{1}{2}$ , that intersect the graph of $C$ at two separate points: $(\frac{1}{2},\ \frac{\sqrt{3}}{2})$ and $(\frac{1}{2},\ -\frac{\sqrt{3}}{2})$.

<br>

---
b. Define a relation from $R$ to $R$ as follows:

Is $L$ a function? If it is, find $L(0)$ and $L(1)$.
$$\text{For all}\ (x,\ y) \in R \times R,\ \ (x,\ y) \in L\ \ \text{means that}\ y = x - 1$$
$L$ is a function. For each real number $x$, $y = x − 1$ is a real number, and so there is a real number $y$ with $(x, y) \in L$. Also if $(x, y) \in L$ and $(x, z) \in L$, then $y = x − 1$ and $z = x − 1$, and so $y = z$. In particular, $L(0) = 0 − 1 = −1$ and $L(1) = 1 − 1 = 0$. You can also check these results by inspecting the graph of $L$, shown below. Note that for every real number $x$, the vertical line through $(x, 0)$ passes through the graph of $L$ exactly once. This indicates both that every real number $x$ is the first element of an ordered pair in $L$ and also that no two distinct ordered pairs in $L$ have the same first element.
![[DISCRET12ch3sample0image0.png|center]]