# Generating UI

One extremely popular strategy for generating UI -- on both the front- and back-end -- is to do some form of templating.

Templating allows us to intersperse logic into our HTML code that will eventually be transformed into the correct UI representation. 

```html
<!-- someAngularTemplate.html -->
<div ng-controller='todoController'>
    <h1>Welcome back {{ user.name }}!</h1>
    <h2>Here's your ToDo list:</h2>
    <ul>
        <li 
          ng-repeat="todo in todos" 
          class="{{(todo.completed) ? 'complete' : ‘incomplete’}}"
          >
            {{ todo.text }} -- {{ todo.due }}
        </li>
    </ul>
</div>
```

The example we’re looking at is a snippet of Angular 1.x code that’s accessing a couple of pieces of our state. One of the nicest things about templating is the ease at which we can run a loop right smack in the middle of our HTML, but with heavier logic performed elsewhere. Coding this way basically supports the idea that the presentation and logic layers of our client-side app should be separate. 

React has a different take on things, and basically says it doesn’t matter if logic and presentation are housed in the same layer of code, as long as we’re diligent about separating the app into small composable pieces. React also has a nifty system to make sure the UI reflects the current state, which we’ll talk about later.

The upshot? **React doesn't do templates.**

We're going to be writing our UI exclusively with JavaScript, instead of mixing JavaScript in with HTML. Take a look at the pseudocode below:

```js
function UICreator(){
  return (
    createDOMElement('h1', 'Hello World');
  )
}
```

That's the core idea we'll be building upon throughout this course. It's a strategy that's based on **components** rather than templates, a subject we'll explore more later.

Why is that better? Proponents argue that by breaking down our app into functional pieces rather than by technology (HTML vs. JavaScript controller), we have a codebase in which it’s easy to reuse small pieces. And a lot of developers argue that unifying markup with our logic makes things a lot easier to maintain.

That ends our brief high-level overview of React -- let's start digging into some code!
