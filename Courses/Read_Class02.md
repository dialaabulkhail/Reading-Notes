# Testing and Modules
## TDD: Test-Driven Development 
through TDD, you can grow your software design easily and constantly with building what you need to make your code pass.
whenever you write a test, you can think of breaking the design into smaller pieces.

## Unit tests

### the structure of any function commonly have AAA convention, which refers to: Arrange, Act and Assert

**Arrange**: is where you pay attention to the order of your data in the code.

**Act**: is where your code is executed correctly.

**Assert**: is where you compare to check your output with the expected one.

## The Cycle
the cycle in TDD is made of three steps:
- Write a unit test and make it fail
- Write the feature and make the test pass
- Refactor the code

To summarize that up, TDD offers design software first which is great and also it offers more reliable code.
[More](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)

# If name equals main
## What does the if __name__ == “__main__”: do?
a module is a file that contains statements and definitions of Python. 
whenever you are running in the module (source) there is a variable called __name__ that will have a value called __main__.
now if you decided to import this module to another file; the file name is the module name wth .py; and the module’s name is available as value to __name__ global variable.
That means using (if __name__ == “__main__) will let you execute the file when you invoke the function directly.
[More](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)

# Recursion
> The process in which a function calls itself directly or indirectly 
you need to have a base case inside a condition that indicates the final execution of the code, and also the recursive part.[^1]

The difference between direct and indirect recursion:
when the function calls itself it it a direct function, and it is indirect when it calls another function.

The difference between tailed and non-tailed recursion:
when the recursive call is the last thing executed it is a tailed function.

## pros and cons of using recursive:
- The recursive program has greater space requirements than iterative program as all functions will remain in the stack until the base case is reached.
- it requires more time.
- provides a simple and clean coding.
- some cases are better written recursively than iteratively.
[More](https://www.geeksforgeeks.org/recursion/)



[^1]: https://www.geeksforgeeks.org/recursion/



