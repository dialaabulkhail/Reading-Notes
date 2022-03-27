
# Stacks:

Data structure consists of nodes each node reference to next node in the stack but does snot reference its previous .

- the most important part of a stack:  the (Top) attribute/pointer always pointing of the last element/node added to the stack
_______________

One of the most common methods for stack are: **push** and **pop**
in linked lists i can insert or delete any of the nodes, but in stacks I only can edit the node that the (top) is pointing on (the first node)
--- that makes it always give me a time complexity of O(1)
_______________

## Push creteria:
Top pointer will point on the top of the node.

-create a node (3)
- make the next of new node to be the value of ehat the pointer top is referring to (None)
- make the top pointer refer to the new node

pushing another one:
-create naother node(5)
- make the next of it equal the value of top pointer referring to  (fisrt node)
- make the top refer to the new node

5 -> 3 -> None  ---> Top is pointing to (5)
______________
![](https://www.tutorialspoint.com/data_structures_algorithms/images/stack_representation.jpg)

```
class Node:
    def __init__(self, value):
        self.value  = value
        self.next = None
```

```
class Stack:
    def __init__(self, node = None):
        self.top = node    --> always refers to a node, that will start with None

    def push(self, value):
        node = Node(value)  ---> creating a node
        node.next = self.top ---> making the next equal what top is referring to
        self.top = node ---> changing pointer top to be on the new value
```
___________
testing:
```
import your python file

def test_push():
    stack = Stack()
    stack.push(5)
    stack.push(3)
    stack.push(2)

actual = stack.top.value
expexted = 2
assert actual == expected
```
_____________

## Pop method:
-create a temp pointer to refer on the top/first node
- change the top pointer to refer to the previous one
- change the next of the to temp(fisrst node) and make it refer to None

_____________
```
    ...
    def pop(self): ---> with no values because its always popping the frist node
    
        temp = self.top ---> create  a new pointer to take the top place 
        
        self.top = self.top.next ---> changing the top to be referring to the second node
        
        temp.next = None  --> disconnected the node from the stack
        
        return temp
```
_____________

## tests:

```
def tes_pop():
    stack = Stack()
    stack.push(5)
    stack.push(3)
    stack.push(2)

    actual = stack.pop() ---> because in the method i am returning temp which is the popped value
    expected = 2
    assert actual == expeted
 ```
_____________

## FILO--> fist in last out
_____________

peek --> will return the top value of the stack 
```
    def peek(self):
        return self.top.value
```

```
    def is_empty(slelf):
"""
checks weather the stack is empty -- returns true if its empty
"""
        return self.top == None ---> if i have a value for top it will give me true 
```
__________
```
def test_peek():
    stack = Stack()  --> [2,3,5]
    stack.push(5)
    stack.push(3)
    stack.push(2)

assert 2 == stack.peek()
```
____________
```
def test_is_empty():
    stack = Stack()

assert True == stack.is_empty()
```
___________

we can use fixtures for the repeated 
(  stack = Stack()
    stack.push(5)
    stack.push(3)
    stack.push(2)
)

-imoprt pytest first

```
@pytest.fixtures
def stack():
    
    s = Stack()   
    stack.push(5)
    stack.push(3)
    stack.push(2)
    
    return s    ----->> now we can replace the above in each test with passing (stack)
```

Example:
```
def test_push(stack):

actual = stack.top.value
expexted = 2
assert actual == expected
```
___________________________

# Queue:

Linear data structure that contains two properties:
front -> which points to the fist node in the queue
rear -> points to last node in the queue

- if a new node wants to join the queue:
it will be pushed after the rear --> so the new rear is the new node.

- the front can leave and the front will be pointed to the next node

*adding new node --> enqueue method --> happens from rear
*remove a node --> dequeue method --> happens form fornt

# FIFO --> first in first out
# LILO --> last in last out 
___________
enqueue:
- create a node
- rear.next make it equal to new node
- change the rear value to be the new node
 ------
- if i have an empty queue:
when queue is None (rear and front are None):
the front AND the rear are going to point to the new node(as the first and last node)
____________
![](https://benoitpasquier.com/images/2020/03/queue-data-structure.png)

```
class Queue:
    def __init__(self)
        self.front = None
        self.rear = None

    def enqueue(self, value):
        node = Node(value)
        if not self.front: --> if its None, empty// if self.rear:
            self.rear = node
            self.front = node    

        else:    
            self.rear.next = node
            self.rear = node
```
_____________
```

def test_enqueue():
    queue = Queue()  --> [5,7,9]--> [rear, .. , front]
    queue.enqueue(5)
    queue.enqueue(7)
    queue.enqueue(9)

    actual = queue.rear.value
    expected = 5
    assert actual == expected
```

_____________________________________
[More](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)
