# read08: Game of Greed 3

## List Comprehensions in Python

- List comprehension offers a shorter syntax when you want to create a new list based on the values of an existing list.
- consists of brackets containing any expression followed by a for clause, then zero or more for or if clauses. 
- The expressions can be anything, meaning you can put in all kinds of objects in lists.


The syntax:
```
newlist = [expression for item in iterable if condition == True]
```
<br/>
Example:

```
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
  if "a" in x:
    newlist.append(x)

print(newlist)

```

for more examples please visit [List Comprehensions](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)