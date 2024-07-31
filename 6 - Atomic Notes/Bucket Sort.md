---
id: Bucket Sort
aliases: []
tags: []
---

# Bucket Sort

### General Defintions 

**Defintion:** Bucket sort is a sorting algorithm which works by distributing elements into several different buckets, sorting each bucket and then combining all the buckets to one final sorted list. 

**Time Complexity:** O(n^2), Thetha(n+k)

Bucket sort is similar to a [[Divide and Conquer]] algorithm, however instead of being recursive bucket sort is instead iterative and there are differences in its divide step. 

Each bucket is meant to represent something, in my use cases I've used them to represent frequency like how you do for the solution of [[Top K Frequent Elements|Top K Frequent Elements]] 

Once every element is sorted into their own bucket, we then run a sorting algorithm on the bucket. Typicaly we combine these two steps into one by using [[Insertion Sort]].

After sorting all the elements into their individual buckets, we then bring all the buckets together into one array to give us the final sorted array. 

#### General Use Cases: 
Bucket sort is the most effectivge when the input is either uniformly distributed over a range or when there are floating point values to be sorted. Importantly, we should not be using bucket sort when all or most of the values fall into just a few of the buckets. 

#### Code Example: 

```python
def bucketSort(array):
    bucket = []
    for i in range(len(array)):
        bucket.append([])
    
    for j in array:
        index_b = int(10 * j)
        bucket[index_b].append(j)
    
    for i in range(len(array)):
        bucket[i] = sorted(bucket[i])
    
    k = 0
    for i in range(len(array)):
        for j in range(len(bucket[i])):
            array[k] = bucket[i][j]
            k += 1
    return array

# Example usage
array = [.42, .32, .33, .52, .37, .47, .51]
print("Sorted Array:", bucketSort(array))
```
