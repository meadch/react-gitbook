# From State to UI

Following up on the `state` object in a regular old todo application, you may have come up with something like the following:

```js
var state = {
  user: {
    name: "Charlie",
    email: "cmead@codingdojo.com"
  },
  todos: [
    {
      text: "Learn React",
      completed: false,
      due: "12/31/17"
    },
    {
      text: "Climb Mt. Everest",
      completed: false,
      due: "12/31/20"
    },
  ],
  newTodo: {
    text: '',
    due: ''
  }
}
```

To render the user interface that we want, we’ll probably want to know the `user`. And you can’t have a todo app without a list of `todos`, so you may have included an array of objects, each with `completed` and `due` properties. Our app also probably wants the ability to add a new todo to the list —- as the user interacts with our app \(by filling out a form\) we’ll need to keep track of that information so we have it at the ready when it’s submitted.

Now the big question, which is going to lead us into React land. How should state like this be translated into what we see on the screen?

