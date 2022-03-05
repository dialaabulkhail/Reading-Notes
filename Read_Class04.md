
# Classes and objects
### Objects are refered to a container that have functions and variables coming from classes.
### Classes are templates to create the object

- you have to define a variable that holds an object of the class, as follows:
`
myobjectx = MyClass()
`

- To access the variable inside of the newly created object:
`
print(myobjectx.variable)
`


**Each object you create in the class will have its own versions/copies of variables and functions.**

**__init__ : it is a function that is called when the class is being initiated, It's used for asigning values in a class**

[More](https://www.learnpython.org/en/Classes_and_Objects)

# Thinking Recursively in Python
## What is Recursive?

The basic idea around Recursive is breaking problems into subproblems.

Recursive function is a function that calls itself until it reaches the base case (a certain condition), then it returns the result.

All recursive functions has two parts: 
- base case
- recursive call

Recursive functions add to the Stack each time it is called, and once it reaches the base case it starts to return each call until excecution.

>> To maintain state during recursion you have to either:
>> - Thread the state through each recursive call so that the current state is part of the current call’s execution context 
>> - Keep the state in global scope [^1]


**This is an example of a recursive function for summing numbers**

![](https://files.realpython.com/media/state_3.3e8a68c4fde5.png)

### Recursive data structres in Python
Any data structure that is defined by calling itself is a recursive data structure:
- Lists
- Sets
- dictionaries
- trees

and more

### Naive Recursion is Naive
**interesting note:**
Fibonacci was defined to find the number of rabbits as: [^2]
>>the number of pairs of rabbits born in a given year is equal to the number of pairs of rabbits born in each of the two previous years, starting from one pair of rabbits in the ﬁrst year.

[More](https://realpython.com/python-thinking-recursively/)


# Pytest Fixtures and Coverage
Pytest is a library in Python used to test codes

### Fixtures
**"parametrized tests"**[^3]
>> When you're writing tests, you're rarely going to write just one or two. Rather, you're going to write an entire "test suite", with each test aiming to check a different path through your code. In many cases, this means you'll have a few tests with similar characteristics, something that pytest handles with "parametrized tests".

- Fixtures can act like data, it executes every time you invoke a test using that fixture.
- It can make calculations and decisions.
- You can decide how often a fixture is run.
- >>  if you set the scope of the fixture to be "module", it'll be available throughout your tests but will execute only a single time.[^3]
`@pytest.fixture(scope='module')`

### Coverage
A library that checka that your tests have run all of the code.

package: pytest-cov.

- invoke pytest with the --cov option.
- This will give you coverage of every part of your python library, so provide an argument with the option.
- You'll need to turn the coverage report into something human-readable like HTML 
`coverage html`
this will create a directory name htmlcov.

- And, you should indicate the directory into which the report should be written.
- in the index.html file, you'll get a web-based report showing (in red) where your program still lacks coverage, add a test to cover your code.

[More](https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage)


[^1]:https://realpython.com/python-thinking-recursively/
[^2]: https://realpython.com/python-thinking-recursively/
[^3]:https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage
