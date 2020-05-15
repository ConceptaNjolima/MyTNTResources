# ToDo List App Instructions and Steps

## Prerequisites

Knowledge of variables, constants, arrays, array-methods(maps, length, etc)

## Steps to create a ToDo List app

1. Make a new typescript app
    - [Create React app with Typescript](https://create-react-app.dev/docs/adding-typescript/)
2. Delete contents of index.html, index.tsx, App.tsx and App.css
3. Create App class
    - Add a list title using HTML elements such as `<p>` and the App component to index.html
    - Create class in App.tsx and add a list to it (explain render function)
    - In index.tsx, map App in App.tsx to App id in index.html
4. Add state to App
    - Create interface and state object
    - Add list to the state object
    - Replace the existing list with the state objects list
5. Add Input element
    - Add Form And Input element
    - On form submit show an `alert` to display the Input elements value
    - Try to show inputs value in list (shouldn't update because input is a variable not in state hence no re-render. Explain that the value changed but the app didn't re-render)
6. Add new item to list
    - Change form submit to update array.
    - --- Explain that `setState()` causes a re-render
    - --- Explain why we prevent default (so we don't refresh the page)
    - --- Explain why we make a new Array (reference vs copy)
7. Create `ListItem` component to learn passing props to child components

## Stretch Features

1. Add "New To Do" button
2. Clear Input value after form submit
3. Add `delete()` functionality
4. Sort list alphabetically
