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

## Hashing
Basically, a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.

## Creating a Hash
A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:

1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo to get the remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.

> Each index of the array can hold many types of values. The trick is how the values are stored in comparison to efficiency. Each Index of the array contain “buckets”. Each of these “buckets” holds one key/value pair combination. When there is no entry in a specific bucket, the buckets (each index of the array) all start null. The hash table starts each bucket empty and overwrites their value once a key generates a hashCode that corresponds with an index.

### Collisions
A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions. To put this into perspective, the worst possible hash is one that hashes every single key to the same exact index of an array. The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.

### Bucket Sizes
Hash Maps can have any number of buckets. If a hash map has only a few buckets it will be densely full and have many collisions. If a hash map has more buckets it will be more sparsely populated, there will be less collisions, but there may be a lot of extra empty space.

It’s possible to compute the “load factor” of a hash table. The load factor tells us something about how full the hash table is. A hash table can start with only a few buckets, calculate it’s own load factor, recognize when it gets too full and automatically grow and add more buckets to itself to accommodate more data.

## Internal Methods
### Add()
- send the key to the GetHash method.
- Once you determine the index of where it should be placed, go to that index
- Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
- If something does exist, add the new key/value pair to the data structure within that bucket.

### Find()
- The Find takes in a key, gets the Hash, and goes to the index location specified.
- Once the index location is found in the array.
- The algorithm iterates through the bucket and see if the key exists and return the value.

### Contains()
- The Contains method will accept a key, and return a bool on if that key exists inside the hashtable.
- The best way to do this is to have the contains call the **GetHash** and check the hashtable if the key exists in the table given the index returned.

### GetHash()
- The GetHash will accept a key as a string
- conduct the hash.
- Return the index of the array where the key-value should be placed.

## References
- [https://www.youtube.com/watch?v=MfhjkfocRR0](https://www.youtube.com/watch?v=MfhjkfocRR0)
- [https://algodaily.com/lessons/an-executable-data-structures-cheat-sheet#hash-table-7](https://algodaily.com/lessons/an-executable-data-structures-cheat-sheet#hash-table-7)
- [https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
