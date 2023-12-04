# React: Intro to React

## Complex JS in JSX

src/App.js
```
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
```
Using the `list` array and the map function, we can call the function for every array item.
```
{list.map(function(item) {
  return (
    <div key={item.objectID}>
      <span><a href={item.url}>{item.title}</a></span>
      <span>{item.author}</span>              
      <span>{item.num_comments}</span>
      <span>{item.points}</span>
    </div>
  );
})}
```

Note that the `key` attribute should be a stable identifier.
```
// don't do this
{list.map(function(item,key) {
  return (
    <div key={key}>
      ...
    </div>
  );
})}
```

## Arrow functions

```
//function expression
function(){...}

// arrow function expession
() => {...}
```

A function expression always defines its own `this` object. Arrow fucntion expression hae the `this` object of the enclosing context.

```
// allowed
item => {...}

// allowed
(item) => {...}

// not allowed
item, key => {...}

// allowed
(item, key) => {...}
```

