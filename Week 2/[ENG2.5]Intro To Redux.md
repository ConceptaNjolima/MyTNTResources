# Intro to Redux

This lesson explains what redux is and how to use it in a practical scenario.

## Learning objectives

* TNTs will understand the importance of redux
* TNTs will learn how the store, reducer and actions work together
* TNTs will have a basic understanding of redux

## Time required and pace

Total time: 1 hour

* 45 minutes – explain what is redux and the benefits
* 15 minutes - rules to follow for easier development

## Background / review

## Lesson details

### Redux description (45 minutes)

What is redux and why do we need it:

* Redux is a state management container similar to the state you're familiar with in react.
* So far you've only been exposed to immutable properties passed into components and mutable states changed within components.
* What if we need to pass a mutable property between components, change said property and have the change affect different components.
* Redux lets us keep a state that persists through out the app and can be accessed by every component

There are four basic parts of redux. Let's go over what each part does and an example of what it looks like:

#### Connect

This is used to connect our component, property maps and action maps to the store

```js
import { connect } from 'react-redux'
import { increment, decrement, reset } from './actionCreators'

// Map store properties to component properties
const mapStateToProps = (state /*, ownProps*/) => {
  return {
    counter: state.counter
  }
}

// An object full of action creators
const mapDispatchToProps = { increment, decrement, reset }

// Connect Counter component to the redux store
export default connect(
  mapStateToProps,
  mapDispatchToProps
)(Counter)
```

#### Actions

This is a function used to change the state

```js
export function addTodo(payload) {
  return { type: "ADD_TODO", payload }
};
```

#### Store

This is the state object (key value pairs) that exists throughout the app. The store is generally defined once at the top of your app.

```js
// Example of a state object
const appState= {
   todos: []
}
```

#### Reducer

The reducer ties together Actions and Store and returns a new state object. This is a collection of functions that map actions to the store.

```js

const initialState = {
  todos: []
};

function reducer(state = initialState, action) {
  if (action.type === "ADD_TODO") {
    return Object.assign({}, state, {
      todos: state.todos.concat(action.payload)
    });
  }
  return state;
}

export default reducer;
```

#### Let's put all 4 parts together

![ReduxDataFlow](./redux-data-flow.png)

### Rules to follow for easier development (15 minutes)

Use interfaces instead of 'any' type

* Create an interface for your state to ensure that no reducer can put in a property that shouldn't exist.

```js
export interface AppState {
  todos: string[];
}
```

* Create an interface for your actions and an enum for your action types. This ensures that your reducer won't expect a property that doesn't exist on that action type.

```js
// Action Types
export const ADD_TODO = "ADD_TODO"

export interface AddToDoAction extends Action {
   type: typeof ADD_TODO,
   payload: string
}

// Action Creators
export function addToDo(payload: string) {
   return {
      type: ADD_TODO,
      payload: payload
   }
}
```
