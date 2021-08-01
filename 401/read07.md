# Read07: Game of Greed 2

## Python Scope & the LEGB Rule

### Modifying the Behavior of a Python Scope

- scope rules how variables and names are looked up in your code.
- **LEGB** stand for Local, Enclosing, Global, and Built-in scopes
- The scope of a name defines the area of a program in which you can unambiguously access that name, such as variables, functions, objects..etc
- global names: available to all your code.
- local names: only available or visible to the code within the scope.

### Names and Scopes in Python
-assign a name to a variable, constant, function, class, instance, module, or other Python object.
-For example, if you assign a value to a name inside a function, then that name will have a local Python scope. In contrast, if you assign a value to a name outside of all functions—say, at the top level of a module—then that name will have a global Python scope.

### Python Scope vs Namespace
- In Python, the concept of scope is closely related to the concept of the namespace.in python names stored in a special attribute called .dict.
- Python resolves names using the LEGB rule, which is named after the Python scope for names.

###Using the LEGB Rule for Python Scope
- Local scope: is the code block or body of any Python function or lambda expression.
- Enclosing (or nonlocal) scope: only exists for nested functions.
- Global (or module) scope: is the top-most scope in a Python program, script, or module.
- Built-in scope: created or loaded whenever you run a script or open an interactive session.

### Modifying the Behavior of a Python Scope
#### The global Statement
- The statement consists of the global keyword followed by one or more names separated by commas.

- Example:
```
counter = 0 # A global name … def update_counter(): … global counter # Declare counter as global … counter = counter + 1 # Successfully update the counter
global_counter = 0 # A global name … def update_counter(counter): … return counter + 1 # Rely on a local name
```
- UnboundLocalError an error that is shown when trying to access a variable that is not defined in a certain scope.

#### The nonlocal Statement
- The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas.
- it is used in nested functions, it cannot be used in a global or local scope.

- Example:
```
def func(): … var = 100 # A nonlocal variable … def nested(): … nonlocal var # Declare var as nonlocal … var += 100
```
- A SyntaxError arises when trying to define a nonlocal name using the nonlocal statement and it doesn’t exist in the enclosing scope of the function.
