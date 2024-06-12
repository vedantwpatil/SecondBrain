2024-05-14 12:05

Status: 

Tags: #math 

# Limit Comparison Test

**Definition:** 
$$
\begin{align}
\sum a_{k} \text{ and } \sum b_{k} \text{ both are series with positve terms}\\ \\
p =\lim_{ k \to \infty } \frac{a_{k}}{b_{k}}\\\\
\text{if p is finate and p > 0, then the series both converge or both diverge}

\end{align}
$$

The limit comparison test builds off of the [[Comparison Test]] and is not as straightforward to find the series required for comparison 

### Examples: 
##### Example 1:
$$\sum_{k=1} ^\infty \frac{1}{\sqrt{ k } + 1}$$

The series is likely to be a divergent [[P-Series Test]], to prove that the given series diverges we apply the limit comparison test with 
$$\begin{align}
a_{k} = \frac{1}{\sqrt{ k }+1 } \text{ and } b_{k}=\frac{1}{\sqrt{ k }}
\end{align}$$
We can disregard the $+1$ in the $\sqrt{ k }+1$ as it won't affect the series outcome as determined earlier

$$p=\lim_{ k \to \infty } \frac{a_{k}}{b_{k}} = \lim_{ k \to \infty } \frac{\sqrt{ k }}{\sqrt{ k }+1} = \lim_{ k \to \infty } \frac{\sqrt{ k }(1)}{\sqrt{ k }\left( 1+\frac{1}{\sqrt{ k }} \right)} =\lim_{ k \to \infty } \frac{1}{1+\frac{1}{\sqrt{ k }}}=1$$
Since p is finite and positive, we can conclude that both series diverge and that the given series diverges by [[P-Series Test]]

##### Example 2:
$$a_{k} = \frac{1}{2k^2+k} \text{ and } b_{k} = \frac{1}{2k^2}$$
$$p = \lim_{ k \to \infty } \frac{a_{k}}{b_{k}} = \lim_{ k \to \infty } \frac{2k^2}{2k^2+2} = \lim_{ k \to \infty } \frac{2}{2+\frac{1}{k}}=1$$
Since p is finite and positive, we can conclude that both series converge and that the given series converges by [[P-Series Test]]

##### Example 3:
$$\sum^\infty _{k=1} \frac{3k^3-2k^2+4}{k^7-k^3+2}$$

The given series is likely to behave like 
$$\sum^\infty_{k=1} \frac{3k^3}{k^7}=\sum^\infty_{k=1} \frac{3}{k^4}$$
which converges since it is a constant multiplied by a convergent [[P-Series Test]]. Thus the given series is likely to converge 

$$p = \lim_{ k \to \infty }  \frac{\frac{3k^3-2k^2+4}{k^7-k^3+2}}{\frac{3}{k^4}} \lim_{ k \to \infty } \frac{3k^7 - 2k^6 +4k^4}{3k^7-3k^3+6}  = 1$$
Since p is finite and nonzero, we can conclude that both series have the same outcome and that both series converge 