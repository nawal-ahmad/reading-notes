# Read: 02 - HTML Text, CSS Introduction, and Basic JavaScript Instructions

## Duckett HTML book:

### Chapter 2: “Text” 

- We have two types of text markup:
  1. Structural markup: the elements that use to describe headings and paragraphs
    - Headings from h1 (main heading) to h6.
    - Paragraphs **p**
    - Bold **b** & Italic **i**
    - Superscript **sup** superscript & Subscrip **sub** subscript.
    - White Space to make code easier to read.
    - Line Breaks **br/** (new line) & Horizontal Rules **hr/** (break between theme)
  2. Semantic markup: which provides extra information like where emphasis should be placed, and others.
    - **strong** used to define text with strong importance.
    - **em** used to define emphasized text.
    - **blockqoute** used to tag specifies a section that is quoted from another source.
    - **q** used for shorter quotes that sit within a paragraph.
    - **abrr** use an abbreviation or ancronym.
    - **cite** defines the title of a creative work.
    - **dfn** used to indicate the defining instance of a new term.
    - **address** defines the contact information for the author/owner of a document or an article.
    - **ins** e used to show content that has been inserted into a document.
    - **del** n show text that has been deleted from it.
    - **s** indicates something that is no longer accurate or relevant.


### Chapter 10: Ch.10 “Introducing CSS”

##### How to make your web pages more attractive?
By controlling the design through using CSS.
- CSS works by associating rules with HTML elements
    h1, h2, h3 {
      font-size: 50px;
      color: red;}

- **link** can be used in an HTML document to tell the browser where to find the CSS file.
- **style** include CSS rules within an HTML page by placing them inside a **style** element inside the **head** of the page.
- CSS selector types:
  * Universal selector: applies on all element on the document. *{}
  * Type selector: element names. h1, h2{}
  * Class selector:. .container
  * ID selector: #introduction
  * Child selector: i>a {}
  * Descendant selector: p a {}
  * Adjacent sibling selector: h1+p {}
  * General sibling selector: h1~p {}
-  CSS rules use external style sheet, although they may appear within an HTML page.


## Duckett JS book:

### Chapter 2: “Basic JavaScript Instructions”

#### What are data types in JavaScript?
  - numeric data type
  - string data type
  - boolean data type

- variables are containers for storing data values.
- - Array: It's a special type of variable stores a list of values. 
  example: 

      var studentName; 
      studentNames= ['Ahmad','Khaled','Ali']; 
- Expressions: evaluate into a single value.
- Expressions rely on operators to calculate a value
- Arithmetic operators: (addition, substraction, division, multiplication, increment,decrement and modulus)
- String operator **+** symbol for oncatenation.

#### what are the rules for naming the variable in JavaScript?
- names can contain letters, digits,underscores, and dollar signs.
- Names must begin with a letter
- Names can begin with $ and _ 
- JavaScript keywords) cannot be used as names
- Use camel case if the variable name more than one word. firstName 

### Chapter 4: “Decisions and Loops”

- Conditional statements allow the code to make decisions about what to do next. 
- There are two components to a dcision:
  1.An expression is evaluated which retuen value.
  2.A conditional statement says what to do in a given situation.
- Comparison operators: 
  * == equual to
  * != not equal to
  * === strict equal to
  * !== strict not equal to
  * **>** greater than
  * **<** less than
  * **>=** greator than or equal
  * **<=** less than or equal
- Logical operators:
  * **&&** logical and
  * **||** logical or
  * __!__ logical not  
- If statement: to specify a block of JavaScript code to be executed if a condition is true.
- else statement: o specify a block of code to be executed if the condition is false. 
- The switch statement executes a block of code depending on different cases.

