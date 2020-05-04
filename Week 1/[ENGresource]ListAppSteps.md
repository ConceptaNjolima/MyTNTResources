_PreReq: variables, constants, arrays, array-methods(maps, length, etc)_

1. Make a new typescript app
2. Delete contents of index.html, index.tsx, App.tsx and  App.css
3. create App class
    - Add list name and app to index.html
    - Create class in App.tsx and add list to it (explain render function)
    - In Index.tsx, map App in App.tsx to App id in index.html
4. Add state to App
    - Create interface and state
    - Replace list with state's list
5. Add input
    - Add Form And input
    - Alert input's value on submit
    - And try to show input's value in list (shouldn't update because input is a variable not in state hence no re-render. Explain that the value change but the app didn't re-render)
6. Add new item to list
    - Change submitForm to update array.
    - --- Explain thatsetstae causes re-render
    - --- Explain why we prevent default( so we don't refresh the page)
    - --- Explain why we make a newArray (reference vs copy)
7. TODO: make listItem component to learn passing props

**Stretch tasks for:**

Add new item button

clear inputValue

Add Delete functionality

Sort List
