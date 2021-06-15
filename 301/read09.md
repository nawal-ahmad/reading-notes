# Read09: FUNCTIONAL PROGRAMMING

## Functional Programming Concepts

- What is functional programming?
  Functional Programming is a style of building the structure and elements of computer programs, that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.
  <br/>

- What is a pure function and how do we know if something is a pure function?
  Pure function, are functions that return the same result if given the same arguments (they are also referred as deterministic), and they do not cause any observable side effects.
  <br/>

- What are the benefits of a pure function?

  1. The code is easier to test.
  2. We don’t need to mock anything
  3. The code is consistent1
     <br/>

- What is immutability?
  To say a code is immutable, to mean that it is unchanged or unable to change. When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.
  <br/>

- What is Referential transparency?
  A function that consistently yields the same result for the same input, is referentially transparent.
  `pure functions + immutable data = referential transparency`
  <br/>

## Node JS Tutorial for Beginners #6 - Modules and require()

- What is a module?
  A module is a part of a code that represent some functionality, and is made to be used in other code. So, instead of writing a big code in one file, we split the code into pieces of modules. Each module will have a single or two things to do, which will make our code easier to be expanded and edit, and highly reusable.
  <br/>

- What does the word ‘require’ do?
  `require` will import the module, and enable us to use its functionality.
  <br/>

- How do we bring another module into the file the we are working in?
  Call module `const counter = require('\path')`

- What do we have to do to make a module available?
  export the part of module we want it to be available to other files like `module.export counter`
  <br/>

- To use a function inside a module for example the module is called count.js and its file is in the home directory and contains a function called counter, in a file called app.js we write the following code to use the module inside it.

  1. First, inside count.js we have to specify the function to use outside, so we write in its global scope the following:
     `module.export counter`
  2. After that, inside app.js, assign the function of count.js in a variable with the use of require:
     `const counter = require('\path')`
  3. Now we can use the function inside app.js.

  <br/>
  <br/>

# Refrences:

[Functional Programming Concepts](https://www.youtube.com/watch?v=xHLd36QoS4k)
<br/>
[Node JS Tutorial for Beginners](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)
<br/>
