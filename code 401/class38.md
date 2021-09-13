# React 2


## React - Conditional Rendering


Conditional rendering in React works the same way conditions work in JavaScript. 
Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.

```
function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {
    return <UserGreeting />;
  }
  return <GuestGreeting />;
}

ReactDOM.render(
  // Try changing to isLoggedIn={true}:
  <Greeting isLoggedIn={false} />,
  document.getElementById('root')
);
```


## React - Lists & Keys


Usually you would render lists inside a component

Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements
a stable identity:
 ```
 const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li key={number.toString()}>
    {number}
  </li>
);
 ```


## React - Forms


HTML form elements work a bit differently from other DOM elements in React, because form elements naturally keep some internal state.


## React - Lifting State


+ Often, several components need to reflect the same changing data. We recommend lifting the shared state up to their closest common ancestor. 

+ There should be a single “source of truth” for any data that changes in a React application.

+ Usually, the state is first added to the component that needs it for rendering. 

+ Then, if other components also need it, you can lift it up to their closest common ancestor. 

+ Instead of trying to sync the state between different components, you should rely on the top-down data flow.

+ Lifting state involves writing more “boilerplate” code than two-way binding approaches, but as a benefit, it takes less work to find and isolate bugs. 

+ Since any state “lives” in some component and that component alone can change it, the surface area for bugs is greatly reduced. Additionally, you can implement any custom logic to reject or transform user input.

+ When you see something wrong in the UI, you can use React Developer Tools to inspect the props and move up the tree until you find the component responsible for updating the state.


## React - Composition vs Inheritance


eact has a powerful composition model, and we recommend using composition instead of inheritance to reuse code between components.


### What About Inheritance?


+ At Facebook, we use React in thousands of components, and we haven’t found any use cases where we would recommend creating component inheritance hierarchies.

+ Props and composition give you all the flexibility you need to customize a component’s look and behavior in an explicit and safe way. 

+ Remember that components may accept arbitrary props, including primitive values, React elements, or functions.

+ If you want to reuse non-UI functionality between components, we suggest extracting it into a separate JavaScript module.

The components may import it and use that function, object, or a class, without extending it.


## Thinking in React


React is, in our opinion, the premier way to build big, fast Web apps with JavaScript. It has scaled very well for us at Facebook and Instagram.

One of the many great parts of React is how it makes you think about apps as you build them.
