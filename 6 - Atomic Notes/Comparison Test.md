2024-05-09 02:51

Status: 

Tags: #math 

# Comparison Test

**Definition:** The comparison test is if

$$ 
\sum_{k=1}^\infty a_{k}  \text{and} \sum^\infty_{k=1}b_{k} \text{be series with non negative terms and suppose that }
$$
$$
a_{1} ≤ b_{1}, a_{2} ≤ b_{2}, a_{3} ≤ b_{3}, \dots a_{k}≤b_{k}
$$
$$\text{If the bigger series} \sum b_{k} \text{ converges, then the smaller series } \sum a_{k} \text{ also converges}$$

##### The comparison test is where if both series contain non negative terms, if we check that $a_1 ≤ b_{1} \dots a_{k}≤b_{k}$ then this means 
- If the bigger series **converges**, then the smaller series as to converge as well
- If the smaller series **diverges**, then the bigger series also has to diverge 

Additionally, if the area of $\sum b_{k}$ is finite then the area of $\sum a_{k}$ has to also be finite
### When using the Comparison Test we need to check for 2 conditions: 
- Guess at whether the series $\sum u_{k}$ converge or diverges 
- Find a series which supports our conclusion
	- If we conclude that $\sum u_{k}$ diverges, we then need to find a divergent series which is smaller than $\sum u_{k}$
	- If we conclude that $\sum u_{k}$ converges, we then need to find a convergent series which is bigger than $\sum u_{k}$

#### Examples:

##### Problem 1:
$$\sum ^\infty _k \frac{1}{\sqrt{ k }-\frac{1}{2}}$$
##### Informal Principle: 
- Constant terms in the denominator can be delated without affecting the convergence/divergence of the series
	- This is because the term is constantly being added/subtracted so it wont't affect the outcome of the series

We can get rid of the $\frac{1}{2}$ without affecting convergence/divergence. 

$$\sum ^\infty _k \frac{1}{\sqrt{ k }}$$

We can now compare this with the series  $\sum^\infty_k \frac{1}{\sqrt{ k }-\frac{1}{2}}$  with the $\sum_{k}^\infty \frac{1}{\sqrt{ k }}$, we can assume that the first series diverges by the [[P-Series Test]] test.

This series $\sum_{k}^\infty \frac{1}{\sqrt{ k }}$ is also larger than $\sum^\infty_k \frac{1}{\sqrt{ k }-\frac{1}{2}}$ so we can infer using the comparison test that the given series diverges 

##### Problem 2:
$$\sum^\infty_{k=1} \frac{1}{2k^2 + k}$$
##### Informal Principle: 
- If there is a polynomial in a series, we can disregard all the terms apart from the highest power terms for the numerator and denominator without affecting convergence/divergence
	- This is because the highest power will affect the speed at which it grows/decreases the most 

###### According to this principle we can remove all but the leading terms

$$\sum^\infty_{k=1} \frac{1}{2k^2}$$
We can now remove the 1/2 because it is constantly being applied to the series 

Thus the given polynomial should behave like
$$\frac{1}{2}\sum_{k=1}^\infty \frac{1}{k^2}$$

This series is larger than the given series $\sum^\infty_{k=1} \frac{1}{2k^2 + k}$ so we can conclude that this series converges by the [[P-Series Test]] test and therefore conclude that the given series converges using the comparison test 

# Reference
