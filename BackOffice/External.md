## Objectives  
1.  Introduction
2.  The first part of this unit introduces the material to be studied later. In addition to getting an overview of the material in the first part of the course, you should be able to explain
    
3.  : 
	- The difference between analog and digital systems and why digital systems are capable of greater accuracy
    - The difference between combinational and sequential circuits  
    - Why two-valued signals and binary numbers are commonly used in digital systems

---
### When we write decimal (base $_{10}$) numbers, we use a positional notation; each digit is multiplied by an appropriate power of  $_{10}$ depending on its position in the number. For example,
> $953.78_{10} = 9 \times 10^2 + 5 \times 10^1 + 3 \times 10^0 + 7 \times 10^{-1} + 8 \times 10^{-2}$

Similarly, for binary (base 2) numbers, each binary digit is multiplied by appropriate power of 2:
$$1011.11_2 = 1 \times 2^3 + 0 \times 2^2 + 1 \times 2^1 + 1 \times 2^0 + 1 \times 2^{-1} + 1 \times 2^{-2}$$
$$=8 + 2 + 1 + \frac{1}{2} + \frac{1}{4} = 11 \frac{3}{4} = 11.75_{10}$$
**Note** that binary point separates the positive and negative powers of inline style 2 just as the decimal point separates the positive and negative powers of inline style 10 for decimal numbers.

Any positive integer $R (R > 1)$ can be chosen as the *radix* or *base* of a number system. If the base $R$, then $R$ digits (0, 1, ..., $R - 1$) are used. For example, if $R = 8$, then the required digits are 0, 1, 2, 3, 4, 5, 6, and 7. A number written in positional notation can be expanded in a power series in $R$. For example,
$$N = (a_4 a_3 a_2 a_1 a_0.a_{-1}a_{-2}a_{-3})_R$$
$$= a_4 \times R^4 + a_3 \times R^3 + a_2 \times R^2 + a_1 \times R^1 + a_0 \times R^0 + a_{-1} \times R^{-1} + a_{-2} \times R^{-2} + a_{-3} \times R^{-3}$$
where $a_i$ is the coefficient of $R^i$ and $0 <= a_i <= R - 1$ . If the arithmetic indicated in the power series expansion is done in base 10, then the result is the decimal equivalent of $N$. For example,
$$147.3_8 = 1 \times 8^2 + 4 \times 8^1 + 7 \times 8^0 + 3 \times 8^{-1} = 64 +32 + 7 + \frac{3}{8}$$
$$= 103.375_{10}$$

The power series expansion can be used to convert to any base. For example, converting $147_{10}$ to base3 would be written as
$$147_{10} = 1 \times (101)^2 + (11) \times (101)^1 + (21) \times (101)^0$$
where all the numbers on the right-hand side are base 3 numbers. (Note: In base3, 10 is 101, 7 is 21, etc.) To complete the conversion, base3 arithmetic would be used. Of course, this is not very convenient if the arithmetic is being done by hand. Similarly, if $147_{10}$ is being converted to binary, the calculation would be
$$147_{10} = 1 \times (1010)^2 + (100) \times (1010)^1 + (111) \times (1010)^0$$
Again this is not convenient for hand calculation but it could be done easily in a computer where arithmetic is done in binary. For hand calculation, use the power series expansion when converting from some base into base10.

For bases greater than 10, more than 10 symbols are needed to represent the digits. In this case, letters are usually used to represent digits greater than 9. For example, in hexadecimal (base16), $A$ represents $10_{10}$, $B$ represents $11_{10}$, $C$ represents $12_{10}$, $D$ represents $13_{10}$, $E$ represents $14_{10}$, and $F$ represents $15_{10}$ Thus,
$$A2F_{16} = 10 \times 16^2 + 2 \times 16^1 + 15 \times 16^0 = 2560 + 32 + 15 = 2607_{10}$$

---
Next, we will discuss conversion of a decimal integer to base $R$ using the division method. The base $R$ equivalent of a decimal integer $N$ can be represented as
$$N = (a_na_{n-1}...a_2a_1a_0)_R = a_nR^n + a_{n-1}R^{n-1} +...+ a_2R^2 + a_1R^1 + a_0$$
If we divide *N* by *R*, the remainder is $a_0$:
$$\frac{N}{R} = a_nR^{n-1} + a_{n-1}R^{n-2} +...+ a_2R^1 + a_1 = Q_1, remainder =a_0$$
Then we divide the quotient $Q_1$ by *R*:
$$\frac{Q_1}{R} = a_nR^{n-2} + a_{n-1}R^{n-3} +...+ a_3R^1 + a_2 = Q_2, remainder=a_1$$
Next we divide the quotient $Q_1$ by $R$:
$$\frac{Q_2}{R} = a_nR^{n-3} + a_{n-1}R^{n-4} +...+ a_3 = Q_3, remainder = a_2$$
This process is continued until we finally obtain $a_n$. Note that the remainder obtained at each division step is one oft he desired digits and the least significant digit is obtained first.

---
### Example
- Convert $231.3_4$ to base7
![[Pasted image 20221008232837.png|500]]
The process for converting 231.3 base 4 to base 7 shows three division steps and four multiplication steps. 231.3 base 4 = 2 times 16 + 3 times 4 + 1 + three quarters = 45.75 base 10. The division process is as follows. Step 1. 45 divided by 7 = 6. Rem. 3. Step 2. 6 divided by 7 = 0. Rem. 6. The multiplication process is as follows. Step 1. 0.75 times 7 = (5).25. Step 2. 0.25 times 7 = (1).75. Step 3. 0.75 times 7 = (5).25. Step 4. 0.25 times 7 = (1).75. Therefore, 45.75 base 10 = 63.5 1 5 1 base 7, where 5 1 keeps repeating.

- Conversion from binary to hexadecimal (and conversely) can be done by inspection because each hexadecimal digit corresponds to exactly four binary digits (bits). Starting at the binary point, the bits are divided into groups of four, and each group is replaced by a hexadecimal digit:
As shown in Equation(1-1), extra 0's are added at each end of the bit string as needed to fill out groups of four bits.

<br>

# 
---
**[[0HEADQUARTERS]]**