## About
This is ongoing project which records my leetcode problem process. It also summarizes the common data structure, algorithm, and gives a template.<br>
## Array
#### Easy
1. [Two sum](https://leetcode.com/problems/two-sum/)
2. [Minimum differences](https://leetcode.com/problems/minimum-difference-between-largest-and-smallest-value-in-three-moves/description/)
## String
#### Easy
1. [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/description/)
## Linkedlist
## Stack
## Queue
## Priority queue
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
1. [calculate power](https://leetcode.com/problems/powx-n/)
## Bit manipulation
|>> signed right shift(divide the number by power of 2) e.g. (1000)_2>>2=(1110)_2 -2|<< signed left shift(preserve the sign)
|--------------------------------------------------|----------------------------------------------------------------------|
|>>> unsigned right shift |<<< unsigned left shift
|bitwise and &  | bitwise or \| 
|bitwise XOR ^ (result is 0 if both bits are the same)| bitwise coomplement ~
|1's complement: invert all bits, add up to 1 e.g. (1000)<sub>2</sub>=8 (0111)<sub>2</sub>=-7 | 2's complement: invert all bits and add one, msb is signed e.g. (0110)<sub>2</sub>=6 (1001)<sub>2</sub>+1=(1010)<sub>2</sub>=-1x2<sup>3</sup>+1x2=-6
## Backtrack
## Tree
## Graph
## Greedy/optimization
## DP

## Reference
1. [leetcode-master](https://github.com/youngyangyang04/leetcode-master)
2. [neetcode](https://neetcode.io/practice)
