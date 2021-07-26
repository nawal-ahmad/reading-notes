# FileIO & Exceptions

## Reading and Writing Files in Python

What makes up a file and why that’s important in Python
The basics of reading and writing files in Python
Some basic scenarios of reading and writing files

- > a file is a contiguous set of bytes used to store data, these byte files are translated into binary 1 and 0 for easier processing by the computer.

- Files are constituent of three parts:

  - Header: metadata
  - Data: file contents
  - End of file (EOF): special character

- **File Path**: is a string that represents the location of a file, consist of (Folder Path, File Name, Extension)

#### Opening and Closing a File

- > _file = open('dog_breeds.txt')_
- > _file.close()_
- > with open('dog_breeds.txt') as reader file:
- > with open('dog_breeds.txt', 'r') as reader:

> Character --> Meaning
> 'r' --> Open for reading (default)
> 'w' --> Open for writing, truncating (overwriting) the file first
> 'rb' or 'wb' --> Open in binary mode (read/write using byte data)

- There are three different categories of file objects:

  - Text files
  - Buffered binary files
  - Raw binary files

## Python Exceptions: An Introduction

- > In Python, an error can be a syntax error or an exception.
- > A Python program terminates as soon as it encounters an error.

#### Exceptions versus Syntax Errors

- Syntax Errors: sth is wrong with the syntax, detects an incorrect statement(extra bracket, extra comma)
- Exception Errors:
  > occurs whenever syntactically correct Python code results in an error.

#### Raising an Exception

raise allows you to throw an exception at any time.

```
x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))
output:
Traceback (most recent call last):
  File "<input>", line 4, in <module>
Exception: x should not exceed 5. The value of x was: 10

```

#### The AssertionError Exception

- Assert enables you to verify if a certain condition is met and throw an exception if it isn’t.

- Instead of waiting a program to crash midway, We assert that a certain condition is met.
  If this condition true then the program can continue. If the condition False, the program will throw an AssertionError exception.

#### Handling Exceptions Through try and except Block

- > In the try clause, all statements are executed until an exception is encountered.
- > except is used to catch and handle the exception(s) that are encountered in the try clause.

```
def linux_interaction():
    assert ('linux' in sys.platform), "Function can only run on Linux systems."
    print('Doing something.')
try:
    linux_interaction()
except
    pass
```

#### The else Clause

Execute a certain block of code only in the absence of exceptions.

```
try:
    linux_interaction()
except AssertionError as error:
    print(error)
else:
    print('Executing the else clause.')
```
