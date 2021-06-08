# Read03: Passing Functions as Props

## React Docs - lists and keys

- What does .map() return? 

`array.map()` returns a new array with the same length.

- If I want to loop through an array and display each value in JSX, how do I do that in React?

    1. by using `map()` function to loop through array and return array's values as a list `li` using curly braces `{}`: `  <li>{number}</li>`.

    2. then rendering that list as `ul`: `<ul>{listItems}</ul>`.
<br/>

- Each list item needs a unique <ins>key</ins>. 
`<li key={number.toString()}>{number}</li>`

- What is the purpose of a key?

Keys help React identify which items have changed, are added, or are removed.

<br/>

## The Spread Operator

- What is the spread operator?

It's a syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.

- List 4 things that the spread operator can do.

1. Concatenating or combining arrays
2. Using an array as arguments
3. Adding an item to a list
4. Adding to state in React

- Give an example of using the spread operator to combine two arrays.

````````````````````````````````````````````
let carsOne = ['GMC','BMW']

let carsTwo = ['Mazda','Fiat']

let carsArr = [...carsOne,...carsTwo]

console.log (...carsArr) // GMC BMW Mazda Fiat
````````````````````````````````````````````
<br/>

- Give an example of using the spread operator to add a new item to an array.
````````````````````````````````````````````
let frstArr = ['A','B','C']

let scndArr = ['D','E', ...frstArr]

console.log(scndArr) //  Array(5) [ "D","E","A","B","C" ]
````````````````````````````````````````````
<br/>

- Give an example of using the spread operator to combine two objects into one
````````````````````````````````````````````
const objectOne = {hello: "👧"}

const objectTwo = {world: "🍀"}

const objectThree = {...objectOne, ...objectTwo, love: "💓"}

console.log(objectThree) // Object { hello: "👧", world: "🍀", love: "💓" }

````````````````````````````````````````````
<br/>

<br/>

## How to Pass Functions Between Components

- In the video, what is the first step that the developer does to pass functions between components?

He create a functions where the state going to change.

- In your own words, what does the increment function do?

Update the state count according to the name

- How can you pass a method from a parent component into a child component?

Declared a prop in parent with a function then call it in the child.

- How does the child component invoke a method that was passed to it from a parent component?
By accesing the prop that have a function value which passed from the parent `this.props.name`




## References :

[Lists and Keys](https://reactjs.org/docs/lists-and-keys.html) <br/>
[The Spread Operator](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab) <br/>
[Passing Functions between Components](https://www.youtube.com/watch?v=c05OL7XbwXU)
