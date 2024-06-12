2024-05-14 12:59

Status: 

Tags: #math 

# Alternating Series Test

**Definition:** Alternating series are whose terms alternate between positive and negative and are of special importance


1) $$\sum^\infty_{k=1}(-1)^{k+1} \frac{1}{k}=1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\frac{1}{5}$$
2) $$\sum^\infty_{k=1}(-1)^{k} \frac{1}{k}=-1+\frac{1}{2}-\frac{1}{3}+\frac{1}{4}-\frac{1}{5}$$
#### Theorem: 
An alternating series of either form 1 or 2 converges if the following two conditions are satisfied
- $a_{1}≥a_{2}≥a_{3}≥a_{k}$
- $\lim_{ k \to \infty }a_{k} = 0$

### Examples 
#### Example 1: 
Using alternating series test to show that the following series converge 
$$\sum^\infty_{k=1} (-1)^{k+1} \frac{1}{k}$$
The two conditions in the alternating series test are satisfied since 
$$a_{k}= \frac{\frac{1}{k}>1}{k+1} = a_{k+1} \text{ and } \lim_{ k \to \infty } a_{k}=\lim_{ k \to \infty } \frac{1}{k} = 0$$
#### Example 2:
The two conditions in the alternating series test are satisfied since 
$$\frac{a_{k+1}}{a_{k}}=\frac{k+4}{(k+1)(k+2)} * \frac{k(k+1)}{k+3} = \frac{k^2+4k}{k^2+5k+6} = \frac{k^2+4k}{(k^2+4k)+(k+6)}<1$$
so we can conclude $a_{k} > a_{k+1}$ and 
$$\lim_{ k \to \infty } a_{k} = \lim_{ k \to \infty } \frac{k+3}{k(k+1)} = \lim_{ k \to \infty } \frac{\frac{1}{k}+\frac{3}{k^2}}{1+\frac{1}{k}} = 0$$

#### Approximating Sums of Alternating Series
$$\begin{align}

\end{align}$$