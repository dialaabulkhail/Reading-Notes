# Game of Greed 2

## Python Scope & the LEGB Rule:

### Scopes overview
- Determines how variables and names are looked up, or their visibility in your device.
- The scope depends of the place where a variable is created.
- The scope is presented in **LEGB rule** (Local, Enclosing, Global, Built-in).
- A name will only be accessible in its scope.

### Scope types
1. **Global scopes**: avalible for all code.
2. **Local scopes**: available only within the scope.


**You can create Python names through one of the following operations:**
[^1]
|**Operation** |**Statement** |
| ----------- | ----------- |
|Assignments | x = value |
|Import operations |import module/from module import name |
|Function definitions |def my_func()|
|Argument definitions in the context of functions |def my_func(arg1, arg2,... argN)|
|Class definitions |	class MyClass|

>> Note: There’s an important difference between assignment operations and reference or access operations. When you reference a name, you’re just retrieving its content or value. When you assign a name, you’re either creating that name or modifying it.

### Python Scope vs Namespace
- Python scopes are implemented as dictionaries that map names to objects(called namespaces). 
- This is the mechanism of storing names. They’re stored in a special attribute called .__dict__.

### Using the LEGB Rule for Python Scope
- Local scope --> is the code block or body of any Python function or lambda expression.
- Enclosing (or nonlocal) --> only exists for nested functions, The names in the enclosing scope are visible from the code of the inner and enclosing functions.
- Global (or module) -->  contains all of the names that you define at the top level of a program or a module.
- Built-in scope --> This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. names are available from everywhere in your code, aytomatically loaded whenever you run a script or a program.

>> The LEGB rule is a kind of name lookup procedure, which determines the order in which Python looks up names. For example, if you reference a given name, then Python will look that name up sequentially in the local, enclosing, global, and built-in scope. If the name exists, then you’ll get the first occurrence of it. Otherwise, you’ll get an error.

**Differences between LEGB rules**

![](https://www.pythontutorial.net/wp-content/uploads/2020/11/Python-nonlocal-Scopes-nonlocal-variable-lookup.png)

[More](https://realpython.com/python-scope-legb-rule/)

____________________________________________________________________________
## Big O notation
- How much time and space in memory it being consumed while an algorithm is being executed.
- It is a way to measure how the algorithm will process to increasing data in terms of time and space.
- A way of comparing different algorithm.
- Big O notation gives the worst case senario.
- Computational complexity:
1. O(1) : constant running time.
2. O(n) : linear running time.
3. O(n^k): polynomial running time.
4. O(log n): logathimic running time.
5. O(n log n): log-linear running time.

![](https://miro.medium.com/max/1200/1*leuidehqYrPSmoBRRjG8zA.png)

[More](https://www.youtube.com/watch?v=5Uqawfl0VHQ)
[^1]:https://realpython.com/python-scope-legb-rule/
