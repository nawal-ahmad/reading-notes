# Read: 03 - HTML Lists, CSS Boxes, JS Control Flow

## Duckett HTML book

### Chapter 3: “Lists” 

##### Types of the lists:
1. `<ol>` ordered lists which used numbers 
2. `<ul>` unordered lists which used bullets 
3. `<dl>` defintion lists which contains the term and the definition 
4. nested lists second list in `<li>` element

### Chapter 13: “Boxes” 

- CSS treats HTML elements like has a box around. 
- Boxes parts: 
    - Content like text or images 
    - Padding the area around the content. 
    - Border which goes around the padding and content
    - Margin thw area outside the border.
- Padding and margin are transparent
![Box Parts](R0c150fee87c95feb6aa4665012605450.png "Box")
- We can change border width, style and color.
- display property specifies the display behavior of each element.
- display values could be:
    - inline like span in the same line
    - block starts on new line and takes up the whole width
    - inline-block inline element with height and width values
- visibility property Make elements visible and hidden
- box-shadow property attaches one or more shadows to the element.
- border-radius property defines the radius of the element corners.


## Duckett JS book

### Chapter 2: “Basic sport cars Instructions”
 
- Array: It's a special type of variable stores a list of values. 
  example:
   
```
var studentName; 
studentNames= ['Ahmad','Khaled','Ali'];

```

### Chapter 4: “Decisions and Loops”

- Every value in JavaScript can be treated as if it were true or false
    - Truthy values include: 
        1. any string with content
        2. any number except zero
        3. true boolean value
        4. number calculations
    - Falsy values include:
        1. NAN not a number
        2. undefind
        3. false boolean value
        4. zero
        5. empty undeclared value

- If statement: to specify a block of sport cars code to be executed if a condition is true.
- else statement: to specify a block of code to be executed if the condition is false.
- The switch statement executes a block of code depending on different cases.
- Loops used to run the code with a different values.
    - for loops run a code for number of times
    - while run the code as long as the condition is true.
    - do/while run the code then check if the condition is true then repeat the loop.
- The break statement ends the loop.
- The continue statement skip one iteration if a specified condition occurs and continues the loop.

- for loop example:
```````````
const n = 5;
for (let i = 1; i <= n; i++) {
    console.log('I love sport cars.');
}
```````````
output:
````````````
I love sport cars.
I love sport cars.
I love sport cars.
I love sport cars.
I love sport cars.
````````````

- while example:

```````````
let i = 1, n = 5;
while (i <= n) {
    console.log(i);
    i += 1;
}
````````````
output:
````````````
1
2
3
4
5
````````````

- do-while example:

````````````
let i = 1;
const n = 5;
do {
    console.log(i);
    i++;
} while(i <= n);
`````````````
out:
`````````````
1
2
3
4
5
`````````````
