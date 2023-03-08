**[[DISCRET12ch42|BACK]]**

---
Construct the truth table for the statement form $(p ∨ q) ∧ ∼(p ∧ q)$. Note that when **or** is used in its exclusive sense, the statement “*p or q*” means “*p or q but not both*” or “*p or q and not both p and q*,” which translates into symbols as $(p ∨ q) ∧ ∼(p ∧ q)$. This is sometimes abbreviated $p ⊕ q$ or $p\ \mathit{XOR}\ q$.

**Solution:**
Set up columns labeled $p$, $q$, $p ∨ q$, $p ∧ q$, $∼(p ∧ q)$, and $(p ∨ q) ∧ ∼(p ∧ q)$. Fill in the p and q columns with all the logically possible combinations of **T’s** and **F’s**. Then use the truth tables for $∨$ and $∧$ to fill in the $p ∨ q$ and $p ∧ q$ columns with the appropriate truth values. Next fill in the $∼(p ∧ q)$ column by taking the opposites of the truth values for $p ∧ q$. For example, the entry for $∼(p ∧ q)$ in the first row is **F** because in the first row the truth value of $p ∧ q$ is **T**. Finally, fill in the $(p ∨ q) ∧ ∼(p ∧ q)$ column by considering the truth table for an and statement together with the computed truth values for $p ∨ q and ∼(p ∧ q)$. For example, the entry in the first row is **F** because the entry for $p ∨ q$ is **T**, the entry for $∼(p ∧ q)$ is **F**, and an **and** statement is **false** unless both components are **true**. The entry in the second row is **T** because both components are **true** in this row.

![[DISCRET12ch42sampleimage.png|center]]