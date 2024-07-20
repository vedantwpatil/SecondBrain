---
id: 1721349414-QEFU
aliases:
  - Running Times
tags: []
---

# Running Times
When analyzing algorithms it is important to have a concreate way of differentiating which one is better than the other. One of these ways of differentiating is running time and seeing how fast the algorithm runs in comparison to the other. 

### Different Ways of Evaluating Speed
There are 3 different symboles we use to evalute the speed of an algorithm 

They are O, thetha, and omega with each symbol representing a different condition. This notation is often called Big O notation and is used to differentiate the speeds of algorithms. 

When speaking about algorithms although an algorithm may have the same speed across all its fields, it is important to be concise and accurate while describing an algorithm's speed. The example of this is although 0(n), thetha(n) and omega(n) may all be correct ways to describe [[Insertion Sort|insertion Sort]]s speed, the most precise way of saying this is thetha(n)

However this is the standard amongst those who are deeply into studying algorithms and is not very commonly used terminalogy outside of that field. So it is unlikely to be encountering this terminalogy that frequently unless studying you are studying algorithms directly. 

#### Notation
By using different symbols, the time complexity can mean different things. For example, using a O(n) to measure the time complexity characterizes an upper bound on the function, meaning that the function grows no faster than O(n). Using omega notation characterizes a lower bound and using a theta notation characterizes a tight bound, meaning it will always grow at a certain rate. 

Another way to think about this is that O(n) is the worst case scenario with the symbol thetha representing the best case scenario and that the omega symbol represents the average scenario

#### Order of Growth
There are a bunch of abstractions used to allow us to analyze an algorithm, another one is called the rate of growth and is used to measure the [[#Running Time]]. We mainly consider the leading term in a function because it will affect the speed of growth the most out of all the terms. A quadratic term will not grow as fast as a linear term.

**Big O Notation:**
Despite there being 3 symbols to represent time complexities, we primarily use one and that is big O. This is because it is more valauble to know the worst case scenario rather than knowing the best or average case. In more formal terms, it means that whatever algorithm it is describing does not grow faster than a specific rate. 

In most algorithms the worst case time complexity often skews the average speed alot, making it a statistic that we don't care that much about.

Some of the common time complexities are 
- $O(1)$
	- Constant time.
- $O(n)$
	- Linear time.
- $O(n^2)$
	- Quadratic time.

##### Little o notation:
In addition to the upercase O being a symbol, undercase 0 is also symbol. Little O notation is used when we need a stricter declaration of the growth speed. Little o requires the algorithm to grow strictly less than the description. I don't understand it the best but this the best description I can give of it and would reccomend looking this up if I need to have a better understanding. There is a more lengthy math definition using limits, however I don't consider it helpful.

##### Little omega notation:
With there being [#Little o notation:](#little-o-notation) there is also little omega notation denoted by the symbol ω and is used similarly to little o notation just with the omega cases instead. 

Knowing time complexities are very important as its one of the things tested by a [[Software Engineer]]ing interview. Something that people use to practice for this and learn their algorithms time complexities is [[Neetcode]]
