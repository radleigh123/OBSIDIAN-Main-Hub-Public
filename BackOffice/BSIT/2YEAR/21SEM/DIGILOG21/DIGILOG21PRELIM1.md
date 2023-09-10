---
cssclasses: []
aliases: []
tags: []
---
**[[DIGILOG21|HOME]]**

---
## Logic Gates
A logic gate is a device that acts as a <mark class="hltr-lightgreen">building block for digital circuits</mark>. They perform basic logical functions that are fundamental to digital circuits. Most electronic devices we use today will have some form of logic gates in them. For example, logic gates can be used in technologies such as smartphones, tablets or within memory devices.

In a circuit, logic gates will make decisions based on a combination of digital signals coming from its inputs. Most logic gates have two inputs and one output. Logic gates are based on Boolean algebra. At any given moment, every terminal is in one of the two binary conditions, `false` or `true`. False represents `0`, and true represents `1`. Depending on the type of logic gate being used and the combination of inputs, the binary output will differ. A logic gate can be thought of like a light switch, wherein one position the output is off -- `0`, and in another, it is on -- `1`. Logic gates are commonly used in **integrated circuits** (**IC**).

**[[DIGILOG21PRELIM1AND|AND]]** gate
if 0 is called "false" and 1 is called "true," the gate acts in the same way as the logical "and" operator. The following illustration and table show the circuit symbol and logic combinations for an AND gate. (In the symbol, the input terminals are at left and the output terminal is at right.) The output is "true" when both inputs are "true." Otherwise, the output is "false." In other words, the output is 1 only when both inputs one AND two are 1.
![[DIGILOG21PRELIM11.png|center]]

**[[DIGILOG21PRELIM1OR|OR]]** gate
gets its name from the fact that it behaves after the fashion of the logical inclusive "or." The output is "true" if either or both of the inputs are "true." If both inputs are "false," then the output is "false." In other words, for the output to be 1, at least input one OR two must be 1.
![[DIGILOG21PRELIM12.png|center]]

**XOR** (**exclusive-OR**) gate
acts in the same way as the logical "either/or." The output is "true" if either, but not both, of the inputs are "true." The output is "false" if both inputs are "false" or if both inputs are "true." Another way of looking at this circuit is to observe that the output is 1 if the inputs are different, but 0 if the inputs are the same.
![[DIGILOG21PRELIM13.png|center]]

**[[DIGILOG21PRELIM1NOT|Inverter]]**/**NOT** gate
to differentiate it from other types of electronic inverter devices, has only one input. It reverses the logic state. If the input is 1, then the output is 0. If the input is 0, then the output is 1.
![[DIGILOG21PRELIM14.png|center]]

**[[DIGILOG21PRELIM1NAND|NAND]]** gate
operates as an AND gate followed by a NOT gate. It acts in the manner of the logical operation "and" followed by negation. The output is "false" if both inputs are "true." Otherwise, the output is "true."
![[DIGILOG21PRELIM16.png|center]]

**[[DIGILOG21PRELIM1NOR|NOR]]** gate
is a combination OR gate followed by an inverter. Its output is "true" if both inputs are "false." Otherwise, the output is "false."
![[DIGILOG21PRELIM17.png|center]]

**XNOR** (**exclusive-NOR**) gate
is a combination XOR gate followed by an inverter. Its output is "true" if the inputs are the same, and "false" if the inputs are different.
![[DIGILOG21PRELIM18.png|center]]

<br>

# 
---
- [What is logic gate (AND, OR, XOR, NOT, NAND, NOR and XNOR)?](https://www.techtarget.com/whatis/definition/logic-gate-AND-OR-XOR-NOT-NAND-NOR-and-XNOR#:~:text=A%20logic%20gate%20is%20a,of%20logic%20gates%20in%20them.)