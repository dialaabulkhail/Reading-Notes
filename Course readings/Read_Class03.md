## Reading and writing files on Python 
### What is a file?
A file is a set of bytes used to store data of all sizes, these bytes are translated to binary language so that the computer process them.

**Files components:**
- Header: meta data of file content--> name, size, type..
- Data: the content (data) itself.
- End of file (EOF) : special character at the end of the file.

**data type**:
it depends on the extension used at the end of the file.

### File Paths:
Represents the location of the file, has three parts:
1. folder path
2. folder name
3. extension

**The double-dot (..) can be chained together to traverse multiple directories above the current directory.**

### Character Encodings
>> An encoding is a translation from byte data to human readable characters. This is typically done by assigning a numerical value to represent a character.[^1]

You cannot create or parse your file using two different encodings.

### Opening and Closing a File in Python
to open a file :

`file = open('file_name.extension')`

**not closing a file could lead to recourse leaks**

to close a file:

` file = open('file_name.extension') `

`
try:
    # Further file processing goes here
`

`
finally:
    reader.close()
`

a second way:
`with open('dog_breeds.txt') as reader:
    # Further file processing goes here`
    
    
|Character|	Meaning|
| ----------- | ----------- |
|'r'	| Open for reading (default)|
|'w'	| Open for writing, truncating (overwriting) the file first|
|'rb' | or 'wb'	Open in binary mode (read/write using byte data)|


### Exceptions versus Syntax Errors
> Syntax errors occur when the parser detects an incorrect statement.

### Raising an Exception
use (raise) to throw an exeption when a certain condition occurs

### Assertion
We assert that a certain condition is met

### try and except
The try and except block in Python is used to catch and handle exceptions.

## Summing Up [^2]

- raise allows you to throw an exception at any time.
- assert enables you to verify if a certain condition is met and throw an exception if it isn’t.
- In the try clause, all statements are executed until an exception is encountered.
- except is used to catch and handle the exception(s) that are encountered in the try clause.
- else lets you code sections that should run only when no exceptions are encountered in the try clause.
- finally enables you to execute sections of code that should always run, with or without any previously encountered exceptions.

[^1]: https://realpython.com/read-write-files-python/
[^2]: https://realpython.com/python-exceptions/
