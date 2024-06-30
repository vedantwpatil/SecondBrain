2024-06-02 01:09

Status: 

Tags: 

# Merge Sort

**Time Complexity:** $nlog(n)$
**Definition:** Insertion sort is a [[Divide and Conquer]] algorithm which looks to break the main problem down into smaller problems to solve and then combine their solutions into a larger general solution 

Merge (A,p,q,r)
```python

left = q - p + 1 // length of A[p:q]
right = r - q

//let L[0: left] and R[left:right - 1] be the new arrays

for i in range(left - 1):
	L[i] = A[p+i]
	

```

### General Steps 

**Divide** the subarray into 2 adjacent subarrays with each of them having half the original size. To calculate this, calculate the midpoint (take the average) and divide the main array into 2 smaller subarrays.

**Conquer** by sorting each of the two subarrayss recursivelyy using merge sort 

**Combine** by merging the sorted subarrays back into the main array, returning the final sorted answer 

