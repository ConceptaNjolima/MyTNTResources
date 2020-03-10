#
# Intro to web app architecture

This lesson explains what redux is and how to use it in a practical scenario.

## **Learning objectives**

- TNTs will understand the importance of redux
- TNTs will understand how the store, reducer and actions work together

## **Time required and pace**

Total time: 1.5 hour

- 30 minutes – explain why we need redux
- 40 minutes – walkthrough of adding redux to list app

## **Background / review**

- Component Properties
- Component State
- Interfaces
- Component render()

## **Lesson details**

### **Redux description(20 minutes)**

1. What is redux and why do we need it
  - Redux is a state management container similar to the state you&#39;re familiar with in react.
  - So far you&#39;ve only been exposed to immutable properties passed into components and mutable states changed within components. What if we need to pass a mutable property between components, change said property and have the change affect different components.
  - Redux lets us keep a state that persists through out the app and can be accessed by every component
2. 4 basic parts of redux:
  - Store-This is the state object that exists throughout the app
  - Reducer-This is a collection of functions that map actions to the State
  - Actions-This is a function used to change the state
  - Connect-This is used to connect our component&#39;s properties to the state
3. Store
  - The store is just a normal object (key-value pair) like you&#39;ve already been exposed to.
  - The store is generally defined once at the top of your app by calling in createStore(). It takes in one argument, your reducer and returns a state.
  - It&#39;s an immutable object that can be referenced anywhere in your app.
  - The state is referenced by calling mapStateToProps or mapDispatchToProps.
4. Reducer
  - This is a function that returns a state object. The state object can be c

### **How to add redux to a project ( 30minutes):** Add redux to list app

1. Yarn add react-redux
; Yarn add redux
; Yarn add @types/react-redux

2. Create a **reducer** : a function that takes in a state and action and returns a state.
b) Create the **store** using the reducer at the top of the app.

3. Create an action to modify the state.
 Define the action's behavior in the reducer.

4. Wrap the App component in a connect call
  a) Define mapStateToProps(gets the state's values) and mapDispatchToProps(modifies the state's values)
  b) Add the props to get/change the state in the App Component.
  c) Use the container in index.js
  d) We can now change the App component to use our new props

### **Rules to follow for easier development (15 minutes)**

Use interfaces instead of 'any' type

1. Create an interface for your state to ensure that no reducer can put in a property that shouldn&#39;t exists
2. Create an interface for your actions and an enum for your action types. This ensures that your reducer won&#39;t expect a property that doesn&#39;t exists on that action type.

## **Stretch**

-
  1. Move all states in your list app to redux state
