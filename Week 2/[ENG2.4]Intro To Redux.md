# Intro to Redux

This lesson explains what Redux is and overviews how to use it in a practice. Another lesson will cover it deeper. 

## Learning objectives

* TNTs will understand the importance of Redux
* TNTs will learn how the store, reducer and actions work together
* TNTs will have a basic understanding of Redux

## Time required and pace

Total time: 2 hours 30

* 30 minutes - pre-session
* 60 minutes – instructional session
  * Why Redux? (10 minutes)
  * Redux concepts and architecture (15 minutes)
  * Coding a React app with Redux (35 minutes)
* 60 minutes - post-session: pair-programming exercise

## References

* [Redux basic tutorial](https://redux.js.org/basics/basic-tutorial)
* [Redux with TypeScript](https://redux.js.org/recipes/usage-with-typescript)
* [Store](https://redux.js.org/recipes/configuring-your-store)
* [Actions](https://redux.js.org/basics/actions)
* [Reducers](https://redux.js.org/basics/reducers)
* [Providers](https://react-redux.js.org/api/provider)
* [Connect](https://react-redux.js.org/api/connect)

## Pre-session (30 minutes)

Prepare for the session [here](https://github.com/tnt-summer-academy/Curriculum/wiki/%5BENG-2.4%5D-Intro-to-Redux)

## Instructional session (60 minutes)

### What is Redux and why do we need it?

* Redux is a state management container.
* React permits to solve the problems of maintaining application state and making it consistent with the UI.
* Redux, on the other hand, was introduced to maintain the application state. Each component having a state complicates maintaining a general application state, especially with the dependecies between components. Your typical app does a lot of state generating, processing, and transferring.
* So far, you have only been exposed to immutable properties passed into components (from their parents) and mutable states changed within components.
* What if we need to pass a mutable property between components, change the said property and have the change affect different components?
* Redux lets us keep the state that persists through out the app in one place, the store, that can be accessed by every component.

There are four basic parts in Redux: Store, Actions, Reducer, and Connect. We will go over what each part does and provide an illustrative example. 

![Why redux](https://github.com/tnt-summer-academy/Curriculum/blob/main/Week%202/%5BENG2.4%5D%20whyredux.png)
[Ref: https://www.systango.com/blog/free-react-redux-starter-kit]

### Three principles of Redux

* Single source of truth - the global state of the application is saved in a single store.
* State is read-only - the only way to change the state is to emit an action.
* Changes are made through pure functions - these functions are called reducers. They take the state and an action as parameter and return a new state.

### Architectural overiew of Redux

#### High level architecture view

![redux architecture](https://github.com/tnt-summer-academy/Curriculum/blob/main/Week%202/%5BENG2.4%5Dreduxhighlevelarchitecture.png)
[Ref: https://www.kirupa.com/react/using_redux_with_react.htm]

#### Store

* The whole state of the app is stored inside a single read-only store. 
* The store is created once.
* The only way to change the store is to emit an action. 

#### Actions

* Actions are used to change the store.  
* Actions do not modify the store directly. 
* Actions are dispatched to express an intent to modify the store.

#### Reducers

* Reducers tie together Actions and Store and returns a new state object. 
* Reducers are collections of functions that map / dispatch actions to the store.
* Reducers called “pure functions” because they do nothing but return a value based on their parameters. They have no side effects into any other part of the system.

#### Connect

* We need to connect React components to Redux.
* Connect is used to connect components, property maps and action maps to the store. 

#### Putting everything together

![ReduxDataFlow](https://github.com/tnt-summer-academy/Curriculum/blob/main/Week%202/%5BENG2.4%5Dredux-data-flow.png)

### Coding a React app with Redux

To add Redux to an app:

* Provide your app a reference to the Redux store
* Map the action creators, dispatch functions, and state as props to whatever component needs data from the store

The code below cover a simple counter example. The screenshot shows the final results. The code is available here.

#### Installation

* `yarn add redux`
* `yarn add react-redux`

#### Store

* Store is an object with several methods
  * `createStore(<reducer> [<preloaded state>, <enhancer>])` - creates a Store and returns the whole state tree of the application. 
  * `store.getState()` - returns the complete state tree of the application.
  * `store.dispatch(action)` - dispatches an action and returns the next state. This is the only way to trigger a state change.

index.tsx file

```typescript
// imports
store = createStore(<reducer>);
```
#### Provider

* React Redux provides `<Provider />`, which makes the Redux store available to the rest of your app.
* The application will render a `<Provider>` at the top level, with the entire app’s component tree inside of it.

index.tsx file

```typescript
// imports
ReactDOM.render(
  <Provider store={store}>
    <Counter />
  </Provider>,
  document.querySelector('#root')
);
```

Check the imports in index.tsx

```typescript
import React from 'react';
import ReactDOM from 'react-dom';
import Counter from './Counter';
import {createStore} from 'redux';
import {Provider} from 'react-redux';
import counterReducer from './reducer';
import './index.css';
```

#### Actions

* Actions are objects
  * They have a `type` property that indicates the type of action being performed.
  * The `type` is typically a string constant.
* Action creators are functions that create / return actions. This is a way to abstract the objects.

action.tsx file

```typescript
// Action
const INCREASE = "INCREASE";

export let increaseAction = {
    type: INCREASE
};

// Action creator

export function increaseCounter() {
    return increaseAction;
};
```

#### Reducer

* A reducer is a pure function that takes the previous state and an action, and returns the next state. 
* Redux will call a reducer with an undefined state for the first time. This is where the initial state of the app needs to be initialized.

types.tsx file

```typescript
// State of the app
import {increaseAction, decreaseAction} from './actions';
export interface CounterAppState {
    count: number
  }
export type CounterActionsTypes = typeof decreaseAction | typeof increaseAction;
export default CounterAppState;
```

reducer.tsx file

```typescript
import { increaseAction, decreaseAction } from './actions';
import { CounterAppState, CounterActionsTypes } from './types';

const intialState: CounterAppState = { count: 0 }

function counterReducer(state: CounterAppState | undefined, action: CounterActionsTypes) {
    if (state === undefined) {
        return intialState;
    }
    let c = state.count;
    switch (action.type) {
        case increaseAction.type: {
            return { count: c + 1 };
        }
        case decreaseAction.type:
            return { count: c - 1 };
        default:
            return state;
    }
}

export default counterReducer;
```

#### Connect

* We are now looking at how to connect a React component with the Redux store.
* We create a component `Counter`.
* We'll generate a container component with the React Redux library's `connect()` function. This function takes 2 functions as parameters: `mapStateToProps` and `mapDispatchToProps`.
  * `mapStateToProps` does exactly what its name suggests. It connects a part of the Redux state to the props of a React component. By doing so a connected React component will have access to the exact part of the store it needs.
  * `mapDispatchToProps` does something similar, but for actions. It connects Redux actions to React props. This way a connected React component will be able to send messages to the store.

```typescript
import React from 'react';
import './App.css';
import { increaseAction, decreaseAction } from './actions';
import { CounterAppState } from './types';
import { connect } from 'react-redux';
class Counter extends React.Component<any> {
    render() {
        return (
            <div className="root" >
                <b>COUNTER</b>
                <button className="buttons" onClick={this.props.decreaseCount}> - </button>
                <span>{this.props.countValue}</span>
                <button className="buttons" onClick={this.props.increaseCount}> + </button>
            </div>
        )
    };
}

function mapStateToProps(state: CounterAppState) {
    return {
        countValue: state.count
    }
}

function mapDispatchToProps(dispatch: any) {
    return {
        increaseCount: function () {
            return dispatch(increaseAction);
        },
        decreaseCount: function () {
            return dispatch(decreaseAction);
        }
    }
}

let connectedComponent = connect(
    mapStateToProps,
    mapDispatchToProps
)(Counter);

export default connectedComponent;
```

### Rules to follow for easier development 

* Use meaningful names for variables, modules, components etc.

* Use interfaces instead of 'any' type

* Create an interface for your state to ensure that no reducer can put in a property that shouldn't exist.

* Create an interface for your actions and an enum / constants for your action types. This ensures that your reducer won't expect a property that doesn't exist on that action type.

* Decompose the app - reducer, actions, types, components etc.

# Stretch

* Implement a to-do-list example in React (TypeScript) with Redux.
* [More examples on Redux](https://redux.js.org/introduction/examples) (To convert to TypeScript!)

# Code

Samples - The session uses redux-simple-counter [here](https://github.com/tnt-summer-academy/Samples/tree/main/Week_2)

Exercises - The exercise is about finishing redux-simple-counter [here](https://github.com/tnt-summer-academy/Exercises/tree/main/Week_2)
