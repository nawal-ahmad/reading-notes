# Read04 : React Docs - thinking in React

## thinking in React

- How would you break a mock into a component heirarchy?
  We need to know what component do we have then the components that appear within another component in the mock should appear as a child in the hierarchy with give them all names.
  <br/>

- What is the single responsibility principle and how does it apply to components?
  Every class should have a single responsibility. and ideally do one thing. If it ends up growing, it should be decomposed into smaller sub-components.
  <br/>

- What does it mean to build a ‘static’ version of your application?
  The components will only have render() and props and no interactivity without any states.
  <br/>

- Once you have a static application, what do you need to add?
  add State to make the UI interactive.
  <br/>

- What are the three questions you can ask to determine if something is state?

  1. Is it passed in from a parent via props? If so, it probably isn’t state.

  2. Does it remain unchanged over time? If so, it probably isn’t state.

  3. Can you compute it based on any other state or props in your component? If so, it isn’t state.

  <br/>

- How can you identify where state needs to live?

  1. Identify every component that renders something based on that state.

  2. Find a common owner component, Either the common owner or another component higher up in the hierarchy should own the state.

  3. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

<br/>

<br/>

# References:

[RThinking in React](https://reactjs.org/docs/thinking-in-react.html) <br/>
