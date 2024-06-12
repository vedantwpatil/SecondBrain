2024-05-14 12:31

Status: 

Tags: #math 

# Ratio Test

**Definition:**
$$\begin{aligned}
\text{Let } \sum u_{k} \text{ be a series with positive terms and suppose that} \\
p = \lim_{ k \to \infty } \frac{u_{k+1}}{u_{k}}\\
\text{If p < 1, the series converges} \\ 
\text{If p >, or p = } \infty \text{, the series diverges}\\ 
\text{If p = 1, the series may converge or diverge, another test must be used}
\end{aligned}$$

### Examples

#### Example 1: 
$$\sum_{k=1}^\infty \frac{1}{k!}$$
The series converges, since 
$$p = \lim_{ k \to \infty } \frac{u_{k+1}}{u_{k}}=\lim_{ k \to \infty } \frac{\frac{1}{(k+1)!}}{\frac{1}{k!}} = \lim_{ k \to \infty } \frac{k!}{(k+1)!} = \lim_{ k \to \infty } \frac{1}{k+1} = 0 < 1$$
#### Example 2: 
$$\sum_{k=1}^\infty \frac{k}{2^k}$$
The series converges, since
$$p = \lim_{ k \to \infty } \frac{u_{k+1}}{u_{k}} = \lim_{ k \to \infty } \frac{k+1}{2^{k+1}} * \frac{2^k}{k} = \frac{1}{2} \lim_{ k \to \infty } \frac{k+1}{k} = \frac{1}{2} < 1$$

#### Example 3: 
$$\sum^\infty_{k=1} \frac{k^k}{k!}$$
This series converges, since
$$p = \lim_{ k \to \infty } \frac{u_{k+1}}{u_{k}} = \lim_{ k \to \infty } \frac{(k+1)^{k+1}}{(k+1)!}* \frac{k!}{k^k} = \lim_{ k \to \infty } \frac{(k+1)^k}{k^k}=\lim_{ k \to \infty } \left( 1+\frac{1}{k} \right)^k = e > 1$$
