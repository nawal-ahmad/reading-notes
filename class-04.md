# Read: 04 - HTML Links, CSS Layout, JS Functions

## Duckett HTML book:

### Chapter 4: “Links”

- Links allow users to move from page to page in the same site or to other sites.
````````
<a href="url">link text</a>
````````
- To create a link opens email use mailto: inside the href attribute.
`````````
<a href="malito:nawalahmad.bme@gmail.com">My email</a>
`````````
- Use _blank target attribute to Opens document in a new window or tab
- Use id attribute to target elements within a page.
`````````
<a href="#top">
`````````

### Chapter 15: “Layout” 

- CSS treats each HTML element as boxes.
    -Block-level elements which start on a new line such as `<h>``<p>``<ul>``<li>`
    -Inline elements which flow between surrounding text such as `<img>``<b>``<i>`
    -Containing elements which is outer box containing two block-level element inside each other.
- CSS float property specifies how  element float.
- Controlling the position of elements by three scheme:
    - Normal flow
    - Relative positioning
    - absolute positioning
- Using box offset to determine where box should be positioned:
    - Fixed positioning
    - Floating positioning
- Overlapping elementts
- CSS clear property specifies what elements can float beside the cleared element and on which side.
- The design needs to be able to work on different sized screens
- Layout types:
    - [Fixed-width layout ](http://www.htmlandcssbook.com/code-samples/chapter-15/fixed-width-layout.html)
    - [Liquid layout](http://www.htmlandcssbook.com/code-samples/chapter-15/liquid-layout.html)
    - [Grid Layout](http://www.htmlandcssbook.com/code-samples/chapter-15/grid-layout.html)
- HTML can include multiple CSS files in one page.

## the Duckett JS book

### Chapter 3 (first part): “Functions, Methods, and Objects”

- A function is a block of code designed to perform a particular task.
- Function take parameters and return value.
- Function is executed when invokes it.
`````````
let square = function (num) 
{return num*num};
console.log(square(4));
`````````

```````
Output:
16
```````
### 6 Reasons for Pair Programming

- pair programming: is a practice of two developers sharing a single workstation.
- Pair programming helping developers by:
    1. explain out loud what code should do
    2. listen to others guidance
    3. read code that others have written
    4. write code themselves.
    
- The 6 reasons for pair programming:
    1. Greater efficiency, It's easier to catch mistakes when two developers work together and they could find the solutions faster and produce higher quality code and it could enhances the technical skills, team communication.
    2. Engaged collaboration, both programmers will focus more than if they were working alone and it help in find a solution for the problems without needing to ask for additional help.
    3. Learning from other students
    4. Social skills, help programmers to develop their interpersonal skills
    5. Job interview readiness
    6. Work environment readiness



