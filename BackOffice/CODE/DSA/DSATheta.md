---
cssclass:
- hide-header-underline-1
aliases:
tags:
---
**[[DSA|HOME [DSA]]]**

---
## Theta Notation (θ)
Theta notation encloses the function from above and below. Since it represents the <mark class="hltr-lightblue">**upper and the lower bound** of the running time of an algorithm</mark>, it is used for analyzing the average-case complexity of an algorithm.
>[!caption|center]
> ![[DSATheta.png|center hs-med]]
> Theta bounds the function within constants factors

```
For a function g(n), Θ(g(n)) is given by the relation:
	Θ(g(n)) = {
		f(n): there exist positive constants c1, c2 and n0
		such that 0 ≤ c1g(n) ≤ f(n) ≤ c2g(n) for all n ≥ n0
	}
```
The above expression can be described as a function `f(n)` belongs to the set `Θ(g(n))` if there exist positive constants `c1` and `c2` such that it can be sandwiched between `c1g(n)` and `c2g(n)`, for sufficiently large n.

If a function `f(n)` lies anywhere in between `c1g(n)` and `c2g(n)` for all `n ≥ n0`, then `f(n)` is said to be asymptotically tight bound.

<br>

# 
---
- [Big-O Notation, Omega Notation and Big-O Notation (Asymptotic Analysis)](https://www.programiz.com/dsa/asymptotic-notations#google_vignette)