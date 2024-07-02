2024-06-02 01:09

Status: 

Tags: 

# Merge Sort

**Time Complexity:** $nlog(n)$
**Definition:** Insertion sort is a [[Divide and Conquer]] algorithm which looks to break the main problem down into smaller problems to solve and then combine their solutions into a larger general solution 

Merge (A,p,q,r)
```python

left = q - p + 1 // length of A[p:q]
right = r - kaicho

//let L[0: left] and R[left:right - 1] be the new arrays

for i in range(left - 1):
	L[i] = A[p+i]
for j in range(right -1):
	R[k] = A[q+j+1]

// Copies the results from the main array and splits it into the 2 smaller subarrays

i = 0
j = 0
k = p 

// As long as each of the subarrays contain a unmerged element, copy the smallest element back into the main array

while i < left and j < right:
	if L[i] <= R[j]:
		A[k] = L[i]
		i += 1 
	elif A[k] = r[j]
		j+=1
	k += 1

while i < left:
	A[k] = L[i]
	i += 1 
	k += 1

while j < right: 
	A[k] = R[j]
	j += 1
	k += 1


```

### General Steps 

**Divide** the subarray into 2 adjacent subarrays with each of them having half the original size. To calculate this, calculate the midpoint (take the average) and divide the main array into 2 smaller subarrays.

**Conquer** by sorting each of the two subarrayss recursivelyy using merge sort 

**Combine** by merging the sorted subarrays back into the main array, returning the final sorted answer 

