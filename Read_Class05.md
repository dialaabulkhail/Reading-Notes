# Data structures

## A term refers to how your dta should be structured and the access fo the data and manipulating the data in the most effecient way.
Effeciency and performance: how much excecution time it will take, time and space complexity...

**One of the applications that present data as: trees are google maps and facebook**

## Linked lists
An example of data structre, Its a way to store data in a block chain.

A Linked list is a sequence of Nodes, each node(is devided into two parts) one contains data item and the other contains the reference (an adress )of the next node.

**the last node has no adress (null)**

**the first node is called "Head"**

**Next -> a property that contains the reference of the next node**

**Current -> the current node** 

- we only have access to Head.
- its type is: node
-  its initial value is : null --> no data yet

### Two types of liked lists:
- singly -> the node only has one pointer to the next node.(only one reference)
- doubly -> the node has a front and back pointers to the next and previous nodes.

**Traversal --> we go through the nodes and stop for each node to search for something, i will be traversing(walkig through nodes)** 
- When condition is wrong in the first node --> current = next(adress of next node) and so on until the condition is applied.
- O(n) --> because we have to go through all nodes

**Traversal method is used instead of for loop, we can use while loop to help us know if the next nodes adress is null.
-> we have to take care of that using an exception to **NillReferenceException**.

**includes: when we want to check for a value if it exists or not in nodes, we use traversal for looking.**

- O(n) --> for time
- O(1) --> for space, no additional space is being used.

[More](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

## Types of data structures
- **linear data structures**
A sequence and an order to how data are constructed and traversed.

- **non-linear data structures**
 items don’t have to be arranged in order, which means that we could traverse the data structure non-sequentially.
 
 ### Memory management
 When an array is created, it needs a certain amount of memory(bytes), one byte next to the another, all together, in one place.
 
 But with linked lists One byte could live somewhere, while the next byte could be stored in another place in memory altogether!

- Arrays are static data structures.
- linked lists are dynamic data structures.
- 
[More](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)

## Big O notation and linked lists
Big O Notation is a way of evaluating the performance of an algorithm.

>> There are two major points to consider when thinking about how an algorithm performs: how much time it requires at runtime given how much time and memory it needs.

### Growing a linked list
-  all we need to do in order to add something to our linked list is figure out which pointer needs to point to where.
-  >> Inserting an element at the beginning of a linked list is particularly nice and efficient because it takes the same amount of time, no matter how long our list is, which is to say it has a space time complexity that is constant, or O(1).

>> a linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element.[^1]
![](https://miro.medium.com/max/1400/1*cUehR5S18XSoVLaPNfNzlA.jpeg)

[More](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)


[^1]:https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996




