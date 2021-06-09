# Read04: React and Forms

## React Docs - Forms

- What is a ‘Controlled Component’? A Controlled Component is one that takes its current value (form element input) through props, handel and control by React 
(callbacks like onChange),  An input form element whose value is controlled by React in this way is called a controlled component.

- Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
We should update the state as soon as the user fill the form, because we need to take the state (user data input) to update the react state.


- How do we target what the user is entering if we have an event handler on an input field? By using value attributes that have a value in the state, and saved the targeted value in the state {value: event.target.value}


<br/>

## The Conditional (Ternary) Operator Explained

- Why would we use a ternary operator?
to simplify the code and make it easier to read that. The ternary operator is commonly used when assigning post data or validating forms.


- Rewrite the following statement using a ternary statement:

    using if condition:

 ````````````````````````````````````````````
 if(x===y){
    console.log(true);
} else {
 console.log(false);
}
 ````````````````````````````````````````````

<br/>

    using if condition:
    
 ````````````````````````````````````````````
 x==y ?console.log(true):console.log(false);
 ````````````````````````````````````````````

<br/>
# References: 
 
 [React Docs - Forms](https://reactjs.org/docs/forms.html) <br/>
 [The Conditional (Ternary) Operator Explained](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)


