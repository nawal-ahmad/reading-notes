# Read: 01 - Java Basics

## Java Basics
### Variables

**The Java programming language defines the following kinds of variables**:

   - Instance Variables (Non-Static Fields): their values are unique to each instance of a class, they are declared in a class outside any method, constructor, or block. 

   - Class Variables (Static Fields): any field declared with the static modifier.

   - Local Variables: A variable defined within a block or method or constructor

   - Parameters: variables passed as arguments to methods


**Naming variables**

In Java Naming variables follow some rules:

   - variable names are case-sensitive
   - variable names begin with a letter
   - `$` sign character, by convention, is never used
   - use full words instead of cryptic abbreviations
   - if the name consists of more than one word, capitalize the first letter of each subsequent word
   - If the variable stores a constant value capitalize every letter and separating subsequent words with the underscore character

### Operators
   - postfix: expr++ expr--
   - unary: ++expr --expr +expr -expr ~ !
   - multiplicative: \* / %
   - additive: + -
   - shift: << >> >>>
   - relational: < > <= >= instanceof
   - equality: == !=
   - bitwise AND: &
   - bitwise exclusive OR: ^
   - bitwise inclusive OR: |
   - logical AND: &&
   - logical OR: ||
   - ternary ?: :
   - assignment: = += -= \*= /= %= &= ^= |= <<= >>= >>>=

### Expressions, Statements, and Blocks

   - **expression:** is a construct made up of variables, operators, and method invocations.

   - **Statements:** are roughly equivalent to sentences in natural languages.
    **Statements types**
     - expression statements
     - declaration statements
     - control flow statements
   - **A block** is a group of zero or more statements between balanced braces and can be used anywhere a single statement is allowed.

### Control Flow Statements

**Control flow statements**, break up the flow of execution by employing decision making, looping, and branching, enabling your program to conditionally execute particular blocks of code.

## Reddit thread on compiling

**The compiler** (usually another program) takes the program the human wrote, and converts it into the program the computer can understand

## References
[Java Basics](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/index.html)
<br/>

[The first response](https://www.reddit.com/r/explainlikeimfive/comments/233dq5/eli5_what_does_it_mean_to_compile_code/)
<br/>

[XKCD: Compiling](https://xkcd.com/303/)