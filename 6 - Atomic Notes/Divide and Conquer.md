---
id: Divide and Conquer
aliases: []
tags: []
---

2024-06-30 00:51

Status: 

Tags: 

# Divide and Conquer

**Definition:** A way of describing certain algorithms and are usually easier to analyze their running time

### General Principles
Most recursive algorithms are using the divide and conquer method, they will break the main problem down into several subproblems which are easier to solve. They then will solve them recursively and combine all these solutions and form a general solution to the main problem.

If the problem is small enough, you can solve it without recursing otherwise there will be 3 steps 

**Divide** the problem into smaller subproblems 
**Conquer** the subproblems by solving them recursively 
**Combine** the subproblem solutions to find a general solution 

One of the most mainstream sorting algorithms which follow this methodology is the [[Merge Sort]]

### Recurrences

**Definition:** Recurrences are equations which describes a function by how it effects other smaller arguements, in other words is a function which describes a sequence recursively. 

The general for of a recurence is a equation or inequality which describes a function by using the function itself and some smaller integers. If the case contains the original function describing itself in smaller iterations then thats the recursive case and if the function does not contain that then it is the base case. 

The general thought process is that if there is no explicit base case we can assume that the recurrnece is algorithmic instead of recursive.

There is a more mathematical approach to recurences and these will pop up later in math so I'll tag this here [[Recurrences|Recurrences]]


