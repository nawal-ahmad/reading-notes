# Read: 02 - Arrays, Loops, Imports

## Packages and Import

- In Java, packages means directory which contains the .java files.

- We declare packages when we define java program.

- To use packages from other libraries we have to name the packages in an import statement .

### Package declaration
The first statement in a Java source file, must be the package declaration, after importing a package you can specify classes from that package.


### Statement order in java file is as follows:
1. Package statment (optional).
2. Imports (optional).
3. Class or interface definitions.

### Imports options:
1. make all the classes visible.
2. make a single class visible
3. fully qualified class name without import.


### Common imports

- import java.awt.*;	Common GUI elements.
- import java.awt.event.*;	The most common GUI event listeners.
- import javax.swing.*;	More common GUI elements. Note "javax".
- import java.util.*;	Data structures (Collections), time, Scanner, etc classes.
- import java.io.*;	Input-output classes.
- import java.text.*;	Some formatting classes.
- import java.util.regex.*;	Regular expression classes.


### some facts about importing in java
- importing all classes in a package will not make the file larger because the import is only tell the compiler where to look.
- You can import all classes or import only one class, nothing will change.
- All classes in the java.lang package are visible without an import.

## A Guide to Java Loops

- Loops can execute a block of code as long as a specified condition is reached.
- Loops are handy because they save time, reduce errors, and they make code more readable.



### types of loops in Java:

- **for loop**: used when we know exactly how many times we want to loop through a block of code.
```
for (int i = 0; i < 5; i++) {
  System.out.println(i);
}
```
- **for-each loop**: sed exclusively to loop through elements in an array.
```
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
```
- **While loop**: The while loop loops through a block of code as long as a specified condition is true.
```
int i = 0;
while (i < 5) {
  System.out.println(i);
  i++;
}
```
- **Do-While loop**: The do/while loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.
```
int i = 0;
do {
  System.out.println(i);
  i++;
}
while (i < 5);
```

## References

[Java Imports (ignore the parts about NetBeans)](https://perso.ensta-paris.fr/~diam/java/online/notes-java/language/10basics/import.html)
<br/>

[A Guide to Java Loops](https://www.baeldung.com/java-loops)
<br/>

