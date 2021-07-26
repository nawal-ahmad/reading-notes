# Read02: Testing and Modules

# Testing and Modules

- In Tests We Trust — TDD with Python Unit tests are some pieces of code to exercise the input,the output and the behavior of your code.You can write them anytime you want.

- example: we want to determine if the user is female or male depend on name, from api lets write unit tests, we don't have code to test;Important aspects about the unit test.

- We care about the structure AAA concept:
  - Arrange: organize the data needed to execute that piece of code (input)
  - Act: execute the code being tested
  - Assert: check if the result (output) is the same as you were expecting.

### The Cycle

- The cycle is made by three steps:

  - Write a unit test and make it fail.

  - Write the feature and make the test pass!

  - Refactor the code.

### Final thoughts on TDD

- TDD is a smart and effective way to code.
- TDD will save you time and effort(though it is hard at the beginning) and will enable better maintenance and development of software.

## Recursion

- The process in which a function calls itself directly or indirectly.
- enables solving certain problems easily
- In recursive functions it is important to use base condition.
  - the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems.
- _Example_
  int fact(int n)
  {
  if (n < = 1) // base case
  return 1;
  else  
   return n\*fact(n-1);  
   }

- If the base case is not reached or not defined, then the stack overflow problem may arise.

- There are two types of recursion (direct & indirect)
- Recursion provides a clean and simple way to write code.

### Memory Allocation In Recursion

> When any function is called from main(), the memory is allocated to it on the stack. A recursive function calls itself, the memory for a called function is allocated on top of memory allocated to calling function and different copy of local variables is created for each function call. When the base case is reached, the function returns its value to the function by whom it is called and memory is de-allocated and the process continues.

## Modular programming:

- Modular programming is the process of breaking a large, unwieldy programming task into separate, smaller, more manageable subtasks or modules.

### advantages to modularizing:

- Simplicity: Easier to understand and debug the code. Easier to understand and debug the code.Rather than focusing on the entire problem at hand, a module typically focuses on one relatively small portion of the problem.

- Maintainability: Modules are typically designed so that they enforce logical boundaries between different problem domains.
