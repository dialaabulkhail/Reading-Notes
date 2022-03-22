# Dunder Methods
- also known as magic/special methods
- are a set of predefined methods you can use to enrich your classes.

## Special Methods and the Python Data Model
### Object Initialization: __init__
used as a constructor to create objects from the class.

### Object Representation: __str__, __repr__
__repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

__str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

### Iteration: __len__, __getitem__, __reversed__
Example of using them:
```
class className:
     ...

    def __len__(self):
        return len(self._transactions)

    def __getitem__(self, position):
        return self._transactions[position]
        
```
      
### Operator Overloading for Comparing Accounts: __eq__, __lt__
```
from functools import total_ordering

@total_ordering
class Account:
    # ... (see above)

    def __eq__(self, other):
        return self.balance == other.balance

    def __lt__(self, other):
        return self.balance < other.balance
```

### Operator Overloading for Merging Accounts: __add__

### Callable Python Objects: __call__
You can make an object callable like a regular function by adding the __call__ dunder method.

### Context Manager Support and the With Statement: __enter__, __exit__

[More](https://dbader.org/blog/python-dunder-methods)
______________________________________________________________________________________

# Basic Statistics in Python — Probability
Probability: the chance of an event to happen.
normal distribution: The normal distribution refers to a particularly important phenomenon in the probability and statistics field. 
>> The most important qualities to notice about the normal distribution is its symmetry and its shape.

difference between the context of probabilities and statistics context in the normal distribution:

![](https://i.imgur.com/egqrj58.jpg)

## Revisiting the normal

>> The normal distribution is significant to probability and statistics thanks to two factors: the Central Limit Theorem and the Three Sigma Rule.

### Central Limit Theorem
Central Limit Theorem lets us know that the average of many trials means will approach the true mean. " With more trials, the closer the average of these trials approach the true probability, even if the individual trials themselves are imperfect"

### Three Sigma Rule
AKA: 68-95-99.7 rule, it is an expression of how many of our observations fall within a certain distance of the mean.
given a normal distribution:
- 68%  of your observations will fall between one standard deviation of the mean.
- 95% will fall within two.
- 99.7% will fall within three

## Z-score
“Given a data point, how many standard deviations is it away from the mean?”

mean(): Arithmetic mean (“average”) of data.
fmean(): Fast, floating point arithmetic mean.
geometric_mean(): Geometric mean of data.
harmonic_mean(): Harmonic mean of data.
median(): Median (middle value) of data.
median_low(): Low median of data.
median_high(): High median of data.
median_grouped(); Median, or 50th percentile, of grouped data.
mode(): Single mode (most common value) of discrete or nominal data.
multimode(): List of modes (most common values) of discrete or nominal data.
quantiles(): Divide data into intervals with equal probability.
pstdev(): Population standard deviation of data.
pvariance(): Population variance of data.
stdev(): Sample standard deviation of data.
variance(): Sample variance of data.
covariance(): Sample covariance for two variables.
correlation(): Pearson’s correlation coefficient for two variables.
linear_regression(): Slope and intercept for simple linear regression.

[More](https://www.dataquest.io/blog/basic-statistics-in-python-probability/)
______________________________________________________________________________________
### Statistical features -->
like bias, variance.. help us explore a dataset to gain valuable insights.

### Probability distribution -->
defines the perfect chance that some event will occur, used to understand the spread of data.

### Basian statistics -->
expresses probability as a degree of belief in an event which can change as new information is gathered rather than a fixed value based on frequency.

### [Statistics cheat sheet](http://web.mit.edu/~csvoss/Public/usabo/stats_handout.pdf)

[Intro to statistics](https://www.youtube.com/watch?v=MdHtK7CWpCQ&ab_channel=SirajRaval)





