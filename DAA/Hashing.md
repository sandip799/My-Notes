# Hashing
- Hashing is useful for searching
- We already studied about searching algorithm like binary and linear search where linear search takes O(n) time whereas binary search takes O(logn) time
- But we use hashing because it takes constant time to for searching
## Drawbacks Of Binary & Linear Search
- Although O(N) is not a bad time complexity but it is slightly costly and in the binary search if the array is not in sorted order then we cant apply the searching technique
- But in hashing it is of O(1), thats why hashing is much better than these two
- Yes there are few drawbacks of hashing, when we learn more about this topic we explore the whole concept so keep studying.
## Hashing Technique
- Suppose there are few keys given like 8,5,6,10,15,9,4 and a hash table which is a array of size 16 because the highest valued keys is 15, and we have to store all the keys in the hash function so this is like domain and a range, so elements from domain are mapped in the range, so this is a **Relation** or **Function**
### Types of Mapping Available in the Relation
- So there are four relational mapping
	1. One to One(Function)
	2. One to Many
	3. Many to One(Function)
	4. Many to Many
#### One to One
- To map keys in the hash table it uses a function which generates the index number and at that location the key is placed
- `h(x) = x` this is the function used here, and we call this function as ideal hashing because time taken for searching or storing or deleting an element is of O(1)
- But the draw back of this function is it takes lots of memory space because if there is a big number in the keys then it will allocate that number of memory spaces inside the memory, then only we will achieve the ideal hashing,
- `so who will responsible for this drawback?` the ideal hash function, because this function is giving the index
- and to achieve the same functionality in minimized memory space we need a well modified hash function
##### Lets Modify The Hash Function
- Suppose there are keys available like 8,3,5,10,15,9,4,25
- here hash function that we modified is `h(x)=x%10` and we also minimize the size of the array and according to that hash function we specify indexes
- but the problem the keys 5 and 25 will mapped to the same index so here we will face collision
- So when ever you modify the ideal hash function then there must collision occurs, so this is the drawback of the hash function and this is of many to one relation
##### How To Resolve This Collision
- For solving the problem there are tow major methods 
	1. Open Hashing
	2. Closed Hashing
### Chaining
- So in the chaining hash technique the aim is to distribute all the key in a uniform way to the hash tables so that every index has same amount of keys 
- We already studied about data structures and we know that the number of inputs are always responsible for the time complexity but in hash **Loading Factor** is responsible for the time complexity
- then `what is loading factor?` it is denoted by **Lambda** and `loading factor = n/size`, here n = number of elements and size = hash table size