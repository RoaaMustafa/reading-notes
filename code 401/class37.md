# React 1
## [ES6 Syntax and Feature Overview](https://www.taniarascia.com/es6-syntax-and-feature-overview/)


|Keyword| Scope         |	Hoisting  |Can Be Reassigned  |Can Be Redeclared|
|-------|---------------|-----------|-------------------|-----------------|
|var	  | Function scope|	Yes	      |Yes		            |Yes              |
|let	  |Block scope    |	No		    |Yes	              |	No              |
|const  | 	Block scope |	No		    |No		              |No               |



## React
+ React - Hello World
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);

```
+ React - JSX

```
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);

```
+ React - Rendering Elements

```
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));

```
+ React - Components & Props

```
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```
+ React - State & Lifecycle

```
class Clock extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>It is {this.state.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}

```
+ React - Handling Events
```
class Toggle extends React.Component {
  constructor(props) {
    super(props);
    this.state = {isToggleOn: true};

    // This binding is necessary to make `this` work in the callback
    this.handleClick = this.handleClick.bind(this);
  }

  handleClick() {
    this.setState(prevState => ({
      isToggleOn: !prevState.isToggleOn
    }));
  }

  render() {
    return (
      <button onClick={this.handleClick}>
        {this.state.isToggleOn ? 'ON' : 'OFF'}
      </button>
    );
  }
}

ReactDOM.render(
  <Toggle />,
  document.getElementById('root')
);

```


## Tailwind CSS


+ Tailwind’s flexbox and padding utilities (`flex`, `flex-shrink-0`, and `p-6`) to control the overall card layout
+ The max-width and margin utilities (`max-w-sm `and `mx-auto`) to constrain the card width and center it horizontally
+ The background color, border radius, and box-shadow utilities (bg-white, rounded-xl, and shadow-md) to style the card’s appearance
+ The width and height utilities (`w-12` and `h-12`) to size the logo image
+ The space-between utilities (`space-x-4`) to handle the spacing between the logo and the text
+ The font size, text color, and font-weight utilities (`text-xl`, `text-black`, `font-medium`, etc.) to style the card text


## Next.js

Next.js: The React Framework
IT gives solution for these problems :

### Why ? 
To build a complete web application with React from scratch, there are many important details you need to consider:

+ Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
+ You need to do production optimizations such as code splitting.
+ You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side rendering or client-side rendering.
+ You might have to write some server-side code to connect your React app to your data store.
