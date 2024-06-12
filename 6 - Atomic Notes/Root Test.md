2024-05-14 12:59

Status: 

Tags: #math 

# Root Test

**When to use:** We use the root test when it is difficult or inconvenient to find the limit required for the ratio test

**Definition:** $$\begin{aligned}
\text{Let } \sum u_{k} \text{ be a series with positive terms and suppose that} \\
p = \lim_{ k \to \infty } u_{k}^{1/k}\\\\
\text{if p < 1, the series converges} \\
\text{if p > 1 or p = } \infty, \text{ the series diverges}\\
\text{If p = 1, the series may converge or diverge, another test must be tried }
\end{aligned}$$

### Examples:
#### Example 1: 
$$\sum^\infty_{k=2}{(\frac{4k-5}{2k+1}})^k$$
The series diverges, since 
$$p = \lim_{ k \to \infty } (u_{k})^{1/k} = \lim_{ k \to \infty } \frac{4k-5}{2k+1} = 2 > 1$$


#### Example 2:
$$\sum_{k=1}^\infty\frac{1}{(\ln(k+1))^k}$$
The series converges, since 
$$p = \lim_{ k \to \infty } (u_{k})^{1/k}= \lim_{ k \to \infty } \frac{1}{\ln(k+1)} = 0 < 1$$
