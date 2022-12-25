## About the project
This project records my leetcode problem process. It also summarizes the common data structure, algorithm, and gives a template.<br>
Reference:[leetcode-master](https://github.com/youngyangyang04/leetcode-master)
## Array
#### Easy
1. [Two sum](https://leetcode.com/problems/two-sum/)
## String
## Linkedlist
## Stack
## Queue
## Heap/priority queue
## Binary search tree
## Hashing
# 
## Sorting
| name | worst case | best case | additional space | stable |
| --- | ----------- | --- | --- | --- |
| 1. bubble sort | O(n<sup>2</sup>) | O(n) | O(1) | yes
| 2. selection sort | O(n<sup>2</sup>) | O(n<sup>2</sup>) | O(1) | no
| 3. insertion sort | O(n<sup>2</sup>) | O(n) | O(1) | yes
| 4. merge sort | O(nlogn) | O(nlogn) | n | yes
| 5. quick sort | O(n<sup>2</sup>) | O(nlogn) | O(logn) | no
| 6. heap sort | O(nlogn) | O(nlogn)| O(1) | no
| 7. shell sort | O(nlogn<sup>2</sup>) | O(n) | O(1) | no
| 8. bucket sort | O(n<sup>2</sup>) | O(n+k) (k:bucket size)| O(n+k)| yes
| 9. radix sort | O(n*k/d) (d:number of largest digit) | O(n*k/d) | O(n+2<sup>d</sup>) | yes
| 10. Tim sort | O(nlogn) | O(nlogn) | n | yes
## Binary Search ##
__Template__
```cpp
int left = 0, right = int(nums.size()) - 1;
while (left <= right) {
// Get the middle index and the middle value. 
   int mid = left + (right - left) / 2;            
   // Case 1, return the middle index.
   if (nums[mid] == target) {
     return mid;
   } 
   // Case 2, discard the smaller half.
   else if (nums[mid] < target) {
     left = mid + 1;   
   } 
   // Case 3, discard the larger half.
   else {
     right = mid - 1;
   }
}        
// If we finish the search without finding target, return -1.
return -1;
```
#### Easy
1. [703 Binary search](https://leetcode.com/problems/binary-search/description)
## Two pointers/sliding window
## Matrix
## Math
## Bit manipulation
## Backtrack
## Tree
## Graph
## Greedy/optimization
## DP
