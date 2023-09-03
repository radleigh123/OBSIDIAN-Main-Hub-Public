---
cssclass:
- hide-header-underline-1
aliases:
tags:
---
**[[DSA|HOME [DSA]]]**

---
## Omega Notation (Ω)
represents the <mark class="hltr-lightblue">**lower bound** of the running time of an algorithm</mark>. Thus, it provides the best case complexity of an algorithm.

>[!caption|center]
> ![[DSAOmega.png|center hs-med]]
> Omega gives the lower bound of a function

```
Ω(g(n)) = {
	f(n): there exist positive constants c and n0 
	such that 0 ≤ cg(n) ≤ f(n) for all n ≥ n0
}
```
The above expression can be described as a function `f(n)` belongs to the set `Ω(g(n))` if there exists a positive constant `c` such that it lies above `cg(n)`, for sufficiently large `n`.

For any value of `n`, the minimum time required by the algorithm is given by Omega `Ω(g(n))`.

<br>

# 
---
- [Big-O Notation, Omega Notation and Big-O Notation (Asymptotic Analysis)](https://www.programiz.com/dsa/asymptotic-notations#google_vignette)