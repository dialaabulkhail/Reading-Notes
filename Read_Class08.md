# Game of Greed 3

# List Comprehensions
Basically Python list comprehensions powerful and essential method to use, they are used to make your code more readable and eaiser to understand.
- faster than other methods.
- better than using for loops regarding to flexibility.
- you can add conditional statements in the form of filters.

## Syntax
```
my_new_list = [ expression for item in list ]
```
## Range() method

- using range() in comprehension lists:
```
digits = [x for x in range(10)]
```
output of printing digits --> [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

- using comprehension lists to doublicate a range of numers:
```
squares = [x**2 for x in range(10)]
```
- using comprehension lists to find even numbers in a range of numers:
```
even_numbers = [ x for x in range(1,20) if x % 2 == 0]
```
- using comprehension lists to print first letter of each author: 
authors = ["Ernest Hemingway","Langston Hughes","Frank Herbert","Toni Morrison",
    "Emily Dickson","Stephen King"]
```
letters = [name[0] for name in authors]
```
- use list comprehension to print the letters in a string:
```
letters = [ letter for letter in "20,000 Leagues Under The Sea"]
```
output --> `['2', '0', ',', '0', '0', '0', ' ', 'L', 'e', 'a', 'g', 'u', 'e', 's', ' ', 'U', 'n', 'd', 'e', 'r', ' ', 'T', 'h', 'e', ' ', 'S', 'e', 'a']`

## lower() and upper() methods

- Changing a letter’s case:
```
lower_case = [ letter.lower() for letter in ['A','B','C'] ]
upper_case = [ letter.upper() for letter in ['a','b','c'] ]
```

## isdigit() method

- to extract numbers from letters:
```
user_data = "Elvis Presley 987-654-3210"
phone_number = [ x for x in user_data if x.isdigit()]
```
output --> list in which each element represents a number from the string above.

## Parsing files 
Using list comprehension, we can iterate through the lines of text in the file and store their contents in a new list.
```
file = open("dreams.txt", 'r')
poem = [ line for line in file ]

for line in poem:
    print(line)
```
output --> 
Hold fast to dreams

For if dreams die

Life is a broken-winged bird

That cannot fly.

-Langston Hughs

## Functions 

- Adding arguments to list comprehension
```
def double(x):
    return x*2

nums = [double(x) for x in range(1,10)]
print(nums)
```
- we can add a condition to the previous for doubling only even numbers:
```
even_nums = [double(x) for x in range(1,10) if x%2 == 0]
```
- Additional arguments can be added to create more complex logic:
```
nums = [x+y for x in [1,2,3] for y in [10,20,30]]
```
output --> `[11, 21, 31, 12, 22, 32, 13, 23, 33]`

[More](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)

# Primer on Python Decorators
Decorators provide a simple syntax for calling higher-order functions.

- **First-Class Objects**
functions are first-class objects. This means that functions can be passed around and used as arguments

- **Inner Functions**
they are functions inside other functions, the inner functions are not defined until the parent function is called, the printing only happens when the inner functions are executed.

[More on decorators](https://realpython.com/primer-on-python-decorators/)





