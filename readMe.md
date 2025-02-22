## About
This is ongoing project which records my leetcode problem process. It also summarizes the common data structure, algorithm, and gives a template.<br>
## Auto load web page
```javascript
function autoLoadTrades() {
    setInterval(() => {
        window.scrollTo(0, document.body.scrollHeight);
    }, 2); // Scroll every .002 seconds
}
```
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
## Heap/priority queue
[K closest points](https://leetcode.com/problems/k-closest-points-to-origin/description/)
## Binary search tree
## Hash table:Hashing
# 
## Sorting
| name | worst case | best case | additional space(in place) | stable(relative order) |
| --- | ----------- | --- | --- | --- |
| 1. bubble sort | O(n<sup>2</sup>) | O(n) | O(1) | yes
| 2. selection sort | O(n<sup>2</sup>) | O(n<sup>2</sup>) | O(1) | no
| 3. insertion sort | O(n<sup>2</sup>) | O(n) | O(1) | yes
| 4. merge sort | O(nlogn) | O(nlogn) | O(n) | yes
| 5. quick sort | O(n<sup>2</sup>) | O(nlogn) | O(logn) | no
| 6. heap sort | O(nlogn) | O(nlogn)| O(1) | no
| 7. shell sort | O(nlogn<sup>2</sup>) | O(n) | O(1) | no
| 8. bucket sort | O(n<sup>2</sup>) | O(n+k) (k:bucket size)| O(n+k)| yes
| 9. radix sort | O(n*k/d) (d:number of largest digit) | O(n*k/d) | O(n+2<sup>d</sup>) | yes
| 10. Tim sort | O(nlogn) | O(nlogn) | n | yes
## Binary Search ##
1. [min number of days to make bouquets](https://leetcode.com/problems/minimum-number-of-days-to-make-m-bouquets/description/)
2. [703 Binary search](https://leetcode.com/problems/binary-search/description) <br>
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
## Two pointers/sliding window
[fruit into baskets](https://leetcode.com/problems/fruit-into-baskets/description/)
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
1.[number of islands](https://leetcode.com/problems/number-of-islands/description/)
# BFS(G,s) G:graph s:start node
```py
for each vertex u in G.V-{s}:#initialize
   u.color = WHITE #not visited
   u.d = inf #distance from s to u
   u.pred = NIL #predecessor
s.color = GRAY # visiting
s.d = 0
s.pred = NIL
Q = Enqueue(Q,s);
while Q not empty:
   u = Dequeue(Q)
   for each v in G.Adj[u]:
      v.color = Gray
      v.d = u.d + 1
      v.pred = u
      Enqueue(Q,v)
   u.color = Black # finish visiting u
```
Time:O(V+E)
Space:O(V)
# DFS(G) G:graph
```py
for each vertex u in G.V: #initialize
   u.color = White
   u.pred = NIL
time = 0
for each vertex u in G.V:
   if u.color = White:
      DFS-VISIT(G,u)

DFS-VISIT(G,u):
   time = time + 1
   u.d = time #start time when discovering u
   u.color = Gray
for each v in G.Adj[u]:
   if v.color == White:
      v.pred = u
      DFS-VISIT(G,v)
u.color = Black
time = time + 1
u.f = time #time after finish visiting u
```
time:O(V+E) space:O(V)
## Greedy/optimization
## DP
1. [odd even jump](https://leetcode.com/problems/odd-even-jump/description/)
2. [Longest increasing subsequence](https://leetcode.com/problems/longest-increasing-subsequence/description/)
3. [coin change](https://leetcode.com/problems/coin-change/description)
## Reference
1. [leetcode-master](https://github.com/youngyangyang04/leetcode-master)
2. [neetcode](https://neetcode.io/practice)
