# React: Basics in React.md

## Internal Component State

Internal componenet state (also known as local state) allows you to save, modify, and delete properties that are stored in your component.

_src/App.js_
```
class App extend Component {

  constructor(props) {
    super(props);
  }

  ...
  
}
```

A constructor is a special function that creates and initializes an object instance of a class. In JavaScript, a constructor gets called when an object is created using the new keyword. The purpose of a constructor is to create a new object and set values for any existing object properties.
When having a constructor in your class component, it is mandatory to call `super();` because the App Component is a subclass of `Component`. Hence the `extends Component` in your App component declaration.
You can also call `super(props);` as well. It sets `this.props` in your constructor in case you want to access them in the constructor. Otherwise, when accessing `this.props` in your constructor, they would be undefined.

_src/App.js_
```
import React, {Component} from 'react';
import './App.css';

const list = [
  {
    title: 'React',
    url: 'https://facebook.github.io/react/',
    author: 'Jordan Walke',
    num_comments: 3,
    points: 4,
    objectID: 0,
  },
  {
    title: 'Redux',
    url: 'https://github.com/reactjs/redux',
    author: 'Dan Abramov, Andrew Clark',
    num_comments: 2,
    points: 5,
    objectID: 1,
  }
]


class App extends Component {

  constructor(props) {
    super(props);

    this.state = {
      list: list,
    };
  }
  render () {
    const helloWorld = "Welcome to the road to learn React";
    return (
      <div className="App">
        <h2>{helloWorld}</h2>
        {this.state.list.map(item => { 
          return (
            <div key={item.objectID}>
              <span><a href={item.url}>{item.title}</a></span>
              <span>{item.author}</span>              
              <span>{item.num_comments}</span>
              <span>{item.points}</span>
            </div>
          );
        })}
      </div>
    )
  }
}

export default App;
```


