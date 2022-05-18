## What are Hashtables?
Hashtables are a type of data structures that stores data as key-value pairs.
This means every **Node** or **Bucket** has both a key, and a value.

### Hashtables Components
**1. Buckets**

A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key-value pairs if a collision occurs.

**2. Collisions**

A collision is what happens when more than one key gets hashed to the same location of the hashtable.

**3. Hash**

A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
-  The result (hash) is the index of the key-value pair in the hash table.

![buckets](https://user-images.githubusercontent.com/97671741/169027313-2c7e781f-13e6-4062-8194-d948bdf0c80a.jpg)




## Pros & Cons
- Can hold keys of many data types as long as they're hashTable.
- Worst case time complexity of Access, Insert, Delete or Search are O(n).
- Hard to look for maximum and minimum values.
- requesting a value with a given key takes O(1).
- requesting a key from a given value takes O(n).

## References
- [https://www.youtube.com/watch?v=MfhjkfocRR0](https://www.youtube.com/watch?v=MfhjkfocRR0)
- [https://algodaily.com/lessons/an-executable-data-structures-cheat-sheet#hash-table-7](https://algodaily.com/lessons/an-executable-data-structures-cheat-sheet#hash-table-7)
- [https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
- 
