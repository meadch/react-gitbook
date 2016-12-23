# String vs. object concatenation

```js
document.getElementById('myElement').innerHTML = `
    <div>
        <h1>Hello Dojo!</h1>
        <h1>Counter: <span>${counter}</span></h1>
    </div>
`;
```

```js
var myElements = React.createElement('div', null, 
    React.createElement('h1', null, 'Hello Dojo!'),
    React.createElement('h1', null, 'Counter: ', 
         React.createElement('span', null, counter),   
    ),
)

ReactDOM.render(myElements, document.getElementById('react'))
```

## Todo: Add a button that alerts the counter `onClick`



