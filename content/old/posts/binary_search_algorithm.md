---
title: "Binary Search Algorithm"
slug: binary-search-algorithm
description: "How to understand the binary search algorithm"
date: "2024-11-07"
tags:
- binary search
- array
- binary tree
---

Binary Search Algorithm (BSA) is a search method that halves the search space with each iteration. It requires the array to be sorted.

*Time complexity:* O(logn)

Assume we have the Array *A*= [2, 3, 4, 5, 6, 7] and we are looking for the position of element 2.
The first step in BSA is to find the position in the middle of the array.
We then checked if the middle element  is equal to 2. In this case, it is not, as the middle element is 4 (at position 3). Next, we determine if 2 is greater than or less than 4.

Since 2 is less than 4,  we  ignore all elements after position 3 and focus on the first half of the array: *A*= [2, 3]. Now, the algorithm begins the next iteration, calculates the new middle position, and checks the element.

If the element we are searching for is greater than 4, we would focus on the second half of the array: *A*=[5,6,7]. In both cases, the middle element is discarded.

If the element we are looking for does not exist in the array, the algorithm returns -1.

It's important to note that the array itself is not split in each iteration. Instead, the algorithm uses two variables (pointers) to represent the start and the end of the search range.

The code below implements the BSA.

```java
public int binarySearch(int[] nums, int target) {
        int mid = nums.length / 2;
        int start = 0;
        int end = nums.length - 1;
        while(start <= end){
            mid = ((end - start) / 2 ) + start;
            if(nums[mid] == target){
                return mid;
            }
            if(nums[mid] < target){
                start = mid + 1;
            }else{
                end = mid - 1;
            }
        }
        return -1;
}
```

## References

Cormen, Thomas H., et al. Introduction to algorithms. MIT press, 2022.

McDowell, Gayle Laakmann. "Cracking the Coding Interview: 189 programming questions and solutions 6th Ed.

Sedgewick, Robert, and Kevin Wayne. Algorithms. Addison-wesley professional, 2011.