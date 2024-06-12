2024-05-15 12:04

Status: 

Tags: #math 

# Maclaurin and Taylor Polynomials

**Definition:** Both polynomials are a way of approximating a function. Maclaurin polynomials allow you to approximate a function at 0 and Taylor polynomials allow you to approximate a function at a specific value. 
- Generally people assume something is at 0 if you don't specify it 

### Local Quadratic Approximations:
- General Formula: $p(x) = f(x_{0}) + f'(x_{0})(x-x_{0})$
- This will approximate the value $x_{0}$ using a quadratic, this value will be accurate only around $x_{0}$ and will get increasingly worse as $x$ gets farther away from $x_{0}$

##### Example 1: 
- Find the local linear and quadratic approximations of $e^x$ at $x=0$

If we let $f(x) = e^x$, then $f'(x) = f''(x) = e^x$, then 
$$f(0)= f'(0)=f''(0)=e^0=1$$
Thus the local quadratic approximation of $e^x$ at $x=0$ is 
$$
e^x \approx 1+x+\frac{x^2}{2}
$$
And the local linear approximation of $e^x$ at $x=0$ 
$$
e^x\approx 1+x
$$
## Maclaurin Polynomials
- **Definition:** We can improve our approximation by adding additional terms to our function $p(x)$. 
###### Given a function which can be differential n times at $x=x_{0}$, find the polynomial $p$ of degree $n$ with the property that the value of $p$ and the values of its first derivatives match those of $f$ at $x_{0}$

We can begin solving this problem in the case where $x_{0} = 0$
$$
p(x) = c_{0}+c_{1}+c_{2}x^2+c_{3}x^3+\dots+c_{n}x^n
$$
such that 
$$
f(0)=p(0) , f'(0) = p'(0) , f''(0) = p''(0),\dots,f^{(n)}(0)=p^{(n)}(0)
$$

but 

$$f^{(n)}(0) = p^{(n)}(0)=n(n-1)(n-1)\dots(1)c_{n} = n!c_{n}$$
which yields the following values for the coefficients of $p(x)$

$$
c_{0}= f(0), c_{1}=f'(0), c_{2} = \frac{f''(0)}{2!}, c_{3}=\frac{f'''(0)}{3!}\dots, c_{n} = \frac{f^{(n)}(0)}{n!}
$$


$$\begin{aligned}

p_{0}(x)=f(0)=1 \\ 
p_{1} (x) = f(0) +f'(0)x = 1+x \\
p_{2}(x)=f(0)+f'(0)x=\frac{f'(0)'}{2!}x^2 = 1 + x +\frac{x^2}{2!}= 1 + x \frac{1}{2} x^2\\ 
p_{3}(x)=f(0)+f'(0)x=\frac{f'(0)'}{2!}x^2 + \frac{f'''(0)}{3!}x^3 \\ 
p_{n}(x)=f(0)+f'(0)x + \frac{f''(0)}{2!}x^2 + \frac{f^{(n)}(0)}{n!}x^n
= 1 + x \frac{x^2}{2} + \dots+\frac{x^n}{n!}

\end{aligned}$$

