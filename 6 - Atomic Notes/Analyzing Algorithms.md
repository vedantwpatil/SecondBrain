---
id: Analyzing Algorithms
aliases: []
tags: []
---

2024-06-24 21:36

Status: 

Tags: 

# Analyzing Algorithms

**Definition:** This document will hold the standard definition of how we analyze algorithms and how to calculate the efficiency of an algorithm to compare to others

## Complications 

There are also some obvious considerations to make which can affect the performance of the algorithm. Some of these are, running tasks in the background, the language you are running the test in as well as the speed of the computer which is running it. Running time also gets impacted by the input and can take different amounts of time depending on how sorted the data is.


All of these considerations have to be taken into consideration when calculating the efficiency and speed of the algorithm so the book [[Introduction to Algorithms]]
uses a RAM model. 
### Ram Model
Some things the ram model assumes are 
- One processor generic machine
- Instructions execute one after another with no concurrent operations 
- Each instruction takes the same amount of time as any other instruction 
- Each access of data takes the same amount of time as another access of data
- Each word of data has a limit on the number of bits
	- If an input of size n we assume the integers are represented as $c\log_{2}n$ bits for a constant $c\geq1$
	- When $c\geq_{1}$ then each word can hold the value of n, allowing us to index the individual input elements.

The ram model does not allow for shortcuts such as assuming sorting takes one step, and aims to maintain realistic expectations. 

The data types are similar to the standard data types
- integer
- floating point
- character

There is no data type for boolean values and instead test whether an integer value is 0 or non-zero, false or true

#### Non Properly Demonstrated
There are a few things which the ram model doesn't properly implement into the model and are a gray area for the model 

These are 
- Is exponentiation a constant time instruction?
	- In math terms, it is not however the way in which computers calculate exponents allow for it to be in constant time
		- Computers will shift the bit of the number to the left or right, which is equivalent to multiplying by 2 allowing for $2^n$ to be a constant time instruction 
- Does not account for memory hierarchy which allows for categorization of memory based on their types to improve performance and increase the efficiency of data storage 

### Input Size
The best notion for determining input size is still debated about and depends on the problem being studied. For many problems, it makes the most sense to use the number of items in that input, such as using n number of items in a list. For other problems it makes more sense to use the total number of bits used to represent the input size.

### Running Time
**Definition:** The number of instructions and data accesses executed. We make this calculation within the [[#Ram Model]]. We assume that a constant amount of time is required to execute each line of pseudocode.

While analyzing an algorithm there are many different ways to characterize the speed of the algorithm, there is a set lanaguage of symbols used to denote the speed of the algorithm. This is gone into more depth here [[Running Times|running times]]

#### Case Analysis 
**Definition:** Analysis of algorithms contain the best case, average case and worse case analysis which all can be different values depending on the situation. For sorting algorithms, the best case will always be O(0) meaning that the input list is already sorted, with the average and worst cases changing depending on the algorithm.

It is important to know about these separate cases as it allows to generally estimate the effectiveness of certain algorithms.

The worst case is often used as a benchmark and an upper bound that guarantees the algorithm will never take any longer. The average case is usually as bad as the worst case.

