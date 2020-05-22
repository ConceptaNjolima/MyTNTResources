# Redux

This lesson goes more in depth on Redux including how to debug redux, applying middleware and replacing our state in the Todo app to redux

## Learning objectives

* TNTs will get a recap on basics of Redux
* TNTs will understand Redux in depth
* TNTs will understand what middleware is
* TNTs will get an introduction to redux devtools to help with redux debugging
* TNTs will add redux to the To Do app

## Time required and pace

Total time: ~ 2 hours

* 10 minutes - recap of redux
* 20 minutes - redux in depth
* 20 minutes - what is middleware
* 10 minutes - redux devtools
* 45 minutes - practice

## Session set up

Resources for instructors

Using redux: [https://react-redux.js.org/using-react-redux/connect-mapstate](https://react-redux.js.org/using-react-redux/connect-mapstate)

Redux devtools: [https://github.com/zalmoxisus/redux-devtools-extension](https://github.com/zalmoxisus/redux-devtools-extension)

Middleware: [https://redux.js.org/advanced/middleware](https://redux.js.org/advanced/middleware)

Thunk middleware: [https://github.com/reduxjs/redux-thunk](https://github.com/reduxjs/redux-thunk)

## Lesson details

### Recap of Redux (10 minutes)

Store - This is the state object (key value pairs) that exists throughout the app.

Action - Actions are functions that serve as a signal for a reducer.

Reducer - The reducer ties together Actions and Store and returns a new state object. This is a collection of functions that map actions to the store. A reducer receives an action as a signal on how to change the state.

### Redux in depth (20 minutes)

How does redux work with your App and it's components?

#### Redux Store

The store is supplied to your App component via HOC (High Order Component)

```js
render(
  // Provider is a High Order Component
  <Provider store={store}>
      <App />
  </Provider>,
  document.getElementById("root")
);
```

#### Connect our child components to Redux

For React components to connect to Redux it will use connect. In the example below a component called TodoList needs to connect to our Redux store.

```js
import React from "react";
import { connect } from "react-redux";

// Map TodoList property to Redux
const mapStateToProps = state => {
  return { todos: state.todos };
};

const TodoList = ({ todos }) => (
  <ul>
    {todos.map(todo => (
      <li>{todo.title}</li>
    ))}
  </ul>
);

// Connect our TodoList component to Redux
const List = connect(mapStateToProps)(TodoList);

export default List;
```

#### Actions

An action of a component can be anything from clicking a button to add a todo or checking a box. This action needs to be dispatched to Redux. Think of it as a way of communicating view events or something that has happened on a component.

```js
// Action Creators
export function addToDo(todo) {
  return { type: "ADD_TODO", todo }
};

// Map our TodoPage prop called addToDo to our Redux action
function mapDispatchToProps(dispatch) {
  return {
    addToDo: todo => dispatch(addToDo(todo))
  };
}

export default class TodoPage extends Component {
    ...// Constructor

    handleAddTodo(event) {
        event.preventDefault()
        this.props.addToDo(this.state.todo)
    }

    render() {
        return (
            <ToDoList />
            <button onclick={this.handleAddToDo}>Add</button>
        )
    }
}

// Connect TodoPage component to Redux
const Page = connect(null, mapDispatchToProps)(TodoPage);
```

### What is middleware (20 minutes)

Middleware is a function that intercepts the Redux action before it reaches the reducer to modify the state. Think of it as a proxy or middle man between 'Action' and 'Reducer'. This allows our application to inspect an actions payload to provide logic such as data validation.

You can write your own middleware or import 3rd party component libraries such as redux-thunk: [https://github.com/reduxjs/redux-thunk](https://github.com/reduxjs/redux-thunk)

Example of a middleware that inspects a string for anything resembling a credit card number before it's added to the Redux store

```js
import { ADD_COMMENT } from "../constants/action-types";
import CreditCardValidator from "../service/CreditCardValidator"

export function creditCardFilterMiddleware({ dispatch }) {
  return function(next) {
    return function(action) {
      if (action.type === ADD_COMMENT) {
        const containsCreditCardInfo = CreditCardValidator.validate(action.payload.comment)

        if (containsCreditCardInfo) {
          return dispatch({ type: "FOUND_CREDIT_CARD_INFO" });
        }
      }

      return next(action);
    };
  };
}
```

### Redux Devtools (10 minutes)

Redux Devtools browser extension allows a developer to view the Redux store and it's changes while debugging. This is a great tool for any React developer during debugging.

Steps to install:

1. Install to Microsoft Edge:
[https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd/related](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd/related)

2. Install in your React project

    ```js
    npm install --save redux-devtools-extension
    ```

3. Once both are installed import the extension and wrap your 'applyMiddleware' function with 'composeWithDevTools'.

    ```js
    import { createStore, applyMiddleware } from 'redux';
    import { composeWithDevTools } from 'redux-devtools-extension';
    import { creditCardMiddleware } from './services/CreditCardMiddleware'

    const store = createStore(reducer, composeWithDevTools(applyMiddleware(creditCardMiddleware)));
    ```

    More info on how to use: [https://github.com/zalmoxisus/redux-devtools-extension](https://github.com/zalmoxisus/redux-devtools-extension)

### Practice: Add redux to To Do app (45 minutes)

NTs should focus on implementing one piece of Redux at a time and work their way to the complete solution

1. Install react-redux
2. Install redux-devtools (Optional) - See above for instructions on installation
3. Implement redux in the Todo app by moving all state to redux

## Stretch

1. Create a middleware to check if a Todo has emojis in it. If it has an emoji then do not include it in the redux store.  
