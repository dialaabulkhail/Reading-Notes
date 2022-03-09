# Game of Greed 1

## Random Modules
### Overview 
Random modules let you have random numbers/order when attached to a funciton.

### Random functions
1. **Radiant** --> just like a range, genertes a random integer between two parameters "the first one will be out of range"

Example: 
```
import random
print random.randint(0, 5)
#This will output either 1, 2, 3, 4 or 5.
```

2. **Random** --> This is used when you want to generate a large number, you can multiply by the number of range.

Example: 
```
import random
random.random() * 100
#This will find a random between 0 and 100.
```

3. **Choise** --> It is used to choose a random number from a list.

Example: 
```
import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```

4. **Shiffle** --> Shuffles the order of elements in a list.

```
x = [[i] for i in range(10)]
shuffle(x)
```

5. **Randrange** --> Generate a randomly selected element from range(start, stop, step).

```
import random
for i in range(3):
    print random.randrange(0, 101, 5)
```

### An Examplpe of using Choise

```
import random
import itertools

outcomes = { 'heads':0,
             'tails':0,
             }
sides = outcomes.keys()

for i in range(10000):
    outcomes[ random.choice(sides) ] += 1

print 'Heads:', outcomes['heads']
print 'Tails:', outcomes['tails']
#There are only two outcomes allowed, so rather than use numbers and convert them, the words “heads” and “tails” are used with choice().
```
[More](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)
_____________________________________________________________________________________

## Risk Analysis
### Overview
According to references, Risk analysis is the process in which it defines and calculate the risk percendtage and effect on the software.
using risk analysis at the begining of any project insures the following:

1. It highlights the potential problem areas.
2. It gives a chance to developers to limit the risk.
3. It provides the damage possibility they may cause to your software along with solutions.


** Certain risks that you must know about:**
- The time that you allocated for testing
- Urgency from the clients to deliver the project
- A defect leakage due to the complexity or size of the application
- Incomplete requirements


**In order to take care of that:**
- Conduct Risk Assessment review meeting
- Use maximum resources to work on high-risk areas
- Create a Risk Assessment database for future use
- Identify and notice the risk magnitude indicators: high, medium, low.


**Risks identifications:**
1. Business Risks
2. Testing Risks
3. Premature Release Risk
4. Software Risks


**The following flowchart represents the Risk Assesment**

![Risk Assesment](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/08/Picture1-528x290.png)

[More](https://www.edureka.co/blog/risk-analysis-in-software-testing/)

________________________________________________________________________________________

## Big O notation
### There are four basic pieces of Big O:
1. If you have two different steps in your algorithm, you add up those steps:
if you have a first step that takes O(a) time, and a seconod step takes O(b) time ---> O(a+b)

2. Drop constants:
if you have a result of O(2n) just drop the constant 2 ---> O(n)

3. If you have different inputs you're going to use different variables to represent them:
if you have for example 2 arrays and you want to find the common elements.
n shouldn't be the array size,cause there're two, so here define a as size array 1 and b as size array b ---> O(a*b)

4. Drop non dominate terms:
if the first step takes O(n), and the second takes O(n^2) --> O(n+n^2) BUT this actually means ---> O(n^2)

[More](https://www.youtube.com/watch?v=v4cd1O4zkGw&ab_channel=HackerRank)







