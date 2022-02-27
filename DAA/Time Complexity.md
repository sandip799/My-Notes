# Time Complexity
## What Do We Consider When Thinking About Time Complexity
- Always look for the worst case complexity
- Always look at complexity for large date
- Here we don't care about the actual time because for example suppose we run a program in different computer and we noticed that the actual time taken by the computer to give output is different and this is happened because of the processing power or other internal activities that's why we don't calculate the exact time, we only derive the relation 
- `Example:-`
## Big- Oh Notation
- Upper Bound
- it means that the complexity will never go beyond the relation 
- for example suppose a program has the time complexity O(N), that means the time taken by the program might be O(1) , O(log N) etc for some value or O(N) but not beyond that
- `Mathematical Representation:-`
## Big-Omega Notation
- Opposite of O(N)
- Lower Bound
- `Mathematical Representation`
## Big-Theta Notation
- `What if an algo has lower bound and upper bound of both O(N^2)`
- For this big theta is introduced 
- Both upper bound and lower bound that means its complexity must not increase or decrease, it will remain same
- `Mathematical Representation:-`
## Little-O Notation
- This is also giving the upper bound 
- in words it means loose upper bound
- it is more stronger statement than big oh
- `Mathematical Representation:-`
## Little-Omega Notation
**Note**- ***in reality we use only the big oh notation in interviews and competitive coding we also use the big oh notation***
## Space Complexity
- Space complexity of an algorithm is the extra space taken by the algorithm with respect to the input size
- Space complexity is the combination of both auxiliary space and space taken by the input
- **Example** - if we want to compare standard sorting algorithm on the basis of the space, then auxiliary space would be a better criteria than space complexity, Merge sort uses O(n) auxiliary space while insertion sort and Heap sort use O(1) auxiliary space but the space complexity of all these algorithm is O(n) though.
## Recursive Algorithm
![[tc1.png]]