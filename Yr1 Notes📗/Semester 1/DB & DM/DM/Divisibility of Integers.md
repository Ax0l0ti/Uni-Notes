# Divisibility of Integers
---
> [!info]+ File Details
> Includes information about this (genus:: Note). Contains details on when this was created, what module the note belongs to.
> > *Date :* 04-12-2023
> > *Module :* (ModCode :: CM12004DM) 
> > *Teacher*: #
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#Speed Run]]
> [[#Z / mZ]]
> [[#Maths of Mod]]
> 
--- 

>[!danger] Speed Run
> - $a = q_1.m + r$ and $b = q_2.m + r$
> - $a = b \space mod \space m$ **means** $( a - b )$ is divisible by $m$ 
> 	- also shown as $m|(a-b)$ or $a - b = m . k$
> - mod is **Equivalent Relation**
> 	- **Reflexive** $a \equiv a \space mod \space m$
> 	- **Symmetric** - if $a \equiv b \space mod \space m$ then $b \equiv a \space mod \space m$
> 	- **Transitive** - if $a \equiv b \space mod \space m$ and $b \equiv c \space mod \space m$ then $a \equiv c \space mod \space m$
> - If $a ≡ b \space mod \space m$ and $c≡ d \space mod \space m$ then 
> 	- $a + c ≡ b + d$ $mod$ $m$ 
> 	- $ac ≡ bd$ $mod$ $m$.

--- 

> [!note] a = b mod m 
> $a = b \mod m$ means $km + b = a$ where $k$ is an integer variable

### Fermats theorem
$xm−1 \mod m = 1$
$a^{p – 1} ≡ 1 (\mod p)$
when m is prime and x and m are coprime. This also yields
$xk \mod m = (x^{k \mod (m−1)}) \mod m$
### $Z / mZ$ 

The finite family of all residue classes modulo m is denoted by $Z/mZ$ or just $Zm$

This is divided into the resultant remainder. for the Finite family of m, there are m 


Finite set size of m 
m possible remainders from $0 \leq r \lt m-1$ in $a = q.m + r$

### Maths of Mod
#TODO
> [!info] Addition
> $$ 
(a+b)\mod m = ((a \mod m) + (b\mod m)) \mod m
$$

> [!success] Multiplication
> $$\begin{align}
(a\times b)\mod m = ((a\mod m) \times (b\mod m)) \mod m \\
\end{align}
$$

> [!bug] Division
> $$\begin{align}
(\frac{a}{b})\mod m = (a \times c) \mod m \mod m \\
\text{Where $c$ is the modular inverse of $c \mod m$} \\ 
\text{Only exists if b and m are co-prime} \\
bc \mod m = 1 \text{. Rearanged this equates to } bc - km = 1
\end{align}
$$


> [!danger] exponential
> $$\begin{align}
> \text{where $a$ is coprime with m}  
> a^b \mod m = a^{b}
\end{align}$$



---