# Dynamical Interplay between Awareness and Epidemic Spreading in Multiplex Networks

## Quenched Multiplex Network

### A. Quenched Mean Field (QMF)

> Quenched Mean Field, also called the individual-based mean filed (IBMF) or N-Intertwined mean field approximation (NIMFA), is a theoretical approach based on the state of the node and its neighbors.
>
> This method considers a set of N equations to describe the time evolution of the probabilities. **Implicitly, it makes the assumption of independence between the state of the nodes.**

### B. Stack Exchange

> If you want the cooling to be the only dynamics that the metal responds to: to ensure that, **this needs to happen much faster than any other process. **

### Summary

+ fast (independent from other influence factors)
+ independent (state of nodes at first)

## UAU-SIS

### Structure

<img src="C:\Users\cheng\OneDrive\图片\Typora\image-20220724203256129.png" alt="image-20220724203256129" style="zoom:50%;" />

### Chain

![image-20220724203809901](C:\Users\cheng\OneDrive\图片\Typora\image-20220724203809901.png)

| Network | Matrix   | Probability   | Probability              |
| ------- | -------- | ------------- | ------------------------ |
| UAU     | $a_{ij}$ | $p_i^{AI}(t)$ | $p_i^{UI}(t)(Undefined)$ |
| SIS     | $b_{ij}$ | $p_i^{AS}(t)$ | $p_i^{US}(t)$            |

### Equation 1

$$
r_i(t) = \prod_j(1-a_{ji}p_i^A(t)\lambda)\\
q_i^A(t) = \prod_j[1-b_{ji}p_i^{AI}(t)\beta^{A}]\\
q_i^U(t) = \prod_j[1-b_{ji}p_j^{AI}(t)\beta^{U}]
$$

For $a_{ij}$:
$$
\begin{bmatrix}
  & A & B & C & D & E & F	\\
A & {\color{blue}0} & 1 & 0 & 1 & 0 & 0	\\
B & 1 & {\color{blue}0}					\\
C & 0 & 1 & {\color{blue}0}				\\
D & 1 & 0 & 1 & {\color{blue}0}			\\
E & 0 & 1 & 0 & 1 & {\color{blue}0}		\\
F & 0 & 0 & 1 & 0 & 1 & {\color{blue}0}	\\	
\end{bmatrix}
$$

$$
a_{ij}=a_{ji}
$$

For $r_i(t)$: (not to be informed):
$$
r_i(t) = [1-a_{11}p_1^A(t)\lambda]
[1-a_{21}p_2^A(t)\lambda]
[1-a_{31}p_3^A(t)\lambda]\cdots
$$

| Term       | Meaning       |
| ---------- | ------------- |
| $a_{ij}$   | connected?    |
| $p_1^A(t)$ | Aware?        |
| $\lambda$  | Communicated? |

For $q_i^A(t)$:(not be infected for the nodes that are Aware)

| Term          | Meaning                                                     |
| ------------- | ----------------------------------------------------------- |
| $b_{ji}$      | connected?                                                  |
| $p_j^{AI}(t)$ | is the neighbor infected?(must be infected by the infect)   |
| $\beta^{A}$   | $\gamma\beta^U$:the probability to be infected by neighbors |

For $q_i^U(t)$:(not be infected for the nodes that are Unaware)

### Equation 2

