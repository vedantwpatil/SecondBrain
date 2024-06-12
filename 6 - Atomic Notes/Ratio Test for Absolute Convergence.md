2024-05-14 18:30

Status: 

Tags: 

# Ratio Test for Absolute Convergence

## Overview
The Ratio Test is a method used to determine whether an infinite series converges absolutely. It is particularly useful for series where each term is a function of factorials or exponential functions.

## Formula
Given an infinite series $\sum a_n$, the Ratio Test states that the series converges absolutely if:

$\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| = L < 1$

- **Converges**: $L < 1$
- **Diverges**: $L > 1$
- **Inconclusive**: $L = 1$

## Examples 
### Example 1: Converging Series Consider the series $$ \sum \frac{2^n}{n!} $$Applying the Ratio Test: $$ \lim_{n \to \infty} \left| \frac{\frac{2^{n+1}}{(n+1)!}}{\frac{2^n}{n!}} \right| = \lim_{n \to \infty} \frac{2}{n+1} = 0 $$#####
Since $0 < 1$, the series converges absolutely. 
### Example 2: Diverging Series Consider the series $$ \sum n! $$Applying the Ratio Test: $$ \lim_{n \to \infty} \left| \frac{(n+1)!}{n!} \right| = \lim_{n \to \infty} (n+1) = \infty $$
 Since $\infty > 1$, the series diverges.
### Example 3: Inconclusive Case Consider the series $$ \sum \frac{1}{n} $$. Applying the Ratio Test: $$ \lim_{n \to \infty} \left| \frac{\frac{1}{n+1}}{\frac{1}{n}} \right| = \lim_{n \to \infty} \frac{n}{n+1} = 1 $$
 Since $L = 1$ the test is inconclusive. Further analysis is required to determine convergence or divergence.