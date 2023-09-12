---
cssclasses:
  - hide-header-underline-1
  - t-w
  - table-nalt
aliases: []
tags: []
---
**[[DIGILOG21PRELIM1|BACK]]**

---
## `XOR` Gate
acts in the same way as the logical "either/or." The output is "true" if either, but not both, of the inputs are "true." The output is "false" if both inputs are "false" or if both inputs are "true." Another way of looking at this circuit is to observe that the output is 1 if the inputs are different, but 0 if the inputs are the same.

**Boolean notation: ** $\mathbf{A}\ \oplus\ \mathbf{B}\quad$ **or** $\quad(\mathbf{A}\ \cdot\ \overline{\mathbf{B}}) + (\overline{\mathbf{A}}\ \cdot\ \mathbf{B})$
![[DIGILOG21PRELIM13.png|center]]

![[Pasted image 20230911174048.png]]

| Pin Number          | Description                                              |
| ------------------- | -------------------------------------------------------- |
| <center>1</center>  | <mark class="hltr-lightblue">A Input Gate 1</mark>       |
| <center>2</center>  | <mark class="hltr-lightblue">B Input Gate 1</mark>       |
| <center>3</center>  | **<mark class="hltr-lightblue">Y Output Gate 1</mark>**  |
| <center>4</center>  | <mark class="hltr-lightgreen">A Input Gate 2</mark>      |
| <center>5</center>  | <mark class="hltr-lightgreen">B Input Gate 2</mark>      |
| <center>6</center>  | **<mark class="hltr-lightgreen">Y Output Gate 2</mark>** |
| <center>7</center>  | *Ground*                                                 |
| <center>8</center>  | **<mark class="hltr-pink">Y Output Gate 3</mark>**       |
| <center>9</center>  | <mark class="hltr-pink">B Input Gate 3</mark>            |
| <center>10</center> | <mark class="hltr-pink">A Input Gate 3</mark>            |
| <center>11</center> | **<mark class="hltr-orange">Y Output Gate 4</mark>**     |
| <center>12</center> | <mark class="hltr-orange">B Input Gate 4</mark>          |
| <center>13</center> | <mark class="hltr-orange">A Input Gate 4</mark>          |
| <center>14</center> | *Positive supply*                                        |
