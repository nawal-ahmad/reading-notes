# Read: Class 04

## Classes and Objects

- > Objects contains variables and functions into a single entity.
- > Objects get their variables and functions from classes.
- > Classes are essentially a template to create your objects.

```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")
```

## Thinking Recursively

- In order to solve any problem, first of all the problem should be broken down into smaller elements.
- _Iterative Algorithm_ built on an explicit loop construction
- Anything that can be defined in terms of smaller entities is a recursive

```
houses = ["Eric's house", "Kenny's house", "Kyle's house", "Stan's house"]
def deliver_presents_iteratively():
    for house in houses:
    print("Delivering presents to", house)
```

### recursive functions

- Definition:
  > A recursive function is a function defined in terms of itself via self-referential expressions, continue to call itself and repeat its behavior until some condition is met to return a result.
- Structure:
  - base case
  - recursive case

### Maintaining State

- > Thread the state through each recursive call so that the current state is part of the current call’s execution context
- > Keep the state in global scope

### recursive data structures

- > A data structure is recursive if it can be deﬁned in terms of a smaller version of itself.
- list, set, tree, dictionary, e are recursive data structures

## Pytest Fixtures and Coverage

- pytest : a library for testing Python code

### Fixtures

- > In pytest, the fixtures are define using a combination of the pytest.fixture decorator, along with a function definition

### Coverage

- > Now, 100% code coverage doesn't mean that your code is perfect or that it lacks bugs. But it does give you a greater degree of confidence in the code and the fact that it has been run at least once.
