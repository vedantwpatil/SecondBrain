2024-06-02 01:08

Status: 

Tags: This is how the book analyzes algorithms [[Analyzing Algorithms]]

# Insertion Sort

**Definition:** We compare each element against the other and insert it into the correct place 
**Time Complexity:** $O(n^2)$ for a list of $n$ items
**Input:** A sequence of $n$ numbers $(a_{1},a_{2}\dots a_{n})$
**Output:** A reordering $(a_{1}',a_{2}'\dots a_{n}')$ of the input sequence 

```python

A = [n]
for j in range(1, len(A)):
	key = A[j] 
	i = j - 1 
	while i > 0 and A[i] > key:
		A[i+1] = A[i]
		i -= 1
	A[i+1] = key
	
```

### Explanation:
**Algorithm Explanation**: The takes an element and compares it to the rest of the list and inserts it into the correct position. 
**Code Explanation:** We start the loop at the 2nd element and compare it against the first element. If the first element is greater than the 2nd we then shift all the values down and insert at the correct place 
#### Loop Invariant
A loop invariance is a way of checking the algorithm for correctness, the way that insertion sort checks itself is by the innermost while loop which checks if the current value is greater than the key value `A[i] > key`. 
##### Technical Terms
- **Initialization:** Is it true prior to the first iteration of the loop
- **Maintenance:** If the initialization is true, it must remain true before the next iteration 
- **Termination:** When the loop terminates, the invariant shows if the algorithm is correct.

**Initialization:** Before the first iteration of the for loop the list is trivially sorted 
**Maintenance:** During each iteration the key element is `A[j]` is inserted into the correct position in the sorted subarray in the inner loop
**Termination:** After the outer loop terminates the list is sorted 

### Analysis of Insertion Sort 
There are obvious things which can impact the performance of a script, such as the language, speed of the computer, background tasks running on the computer and can all have varying degrees of effect on the test. Because of this, [[Introduction to Algorithms]] uses another way of [[Analyzing Algorithms]]

The book then highlights a proof of the best case run time for Insertion Sort, using series to add up the cost of each operation. However, I don't believe for that to be important to focus on and write about. 

