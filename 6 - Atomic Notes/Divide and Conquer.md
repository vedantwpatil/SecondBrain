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