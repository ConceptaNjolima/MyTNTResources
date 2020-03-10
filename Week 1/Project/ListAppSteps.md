_PreReq: variables, constants, arrays, array-methods(maps, length, etc)_

**Activity Steps:**
1. Make a new typescript app
2. Delete contents of index.html, index.tsx, App.tsx and  App.css
3. u
  a. Add list name and app to index.html
  b. Create class in App.tsx and add list to it (explain render function)
  c. In Index.tsx, map App in App.tsx to App id in index.html
4.
  a. Create interface and state
  b. Replace list with state&#39;s list
5.Add input
  a. Add Form And input
  b. Alert input&#39;s value on submit
  c. And try to show input&#39;s value in list (should&#39;nt update because input is a variable not in state hence no rerender. Explain that the value change but the app didn&#39;t rerender)
6. Add new item to list
  a. Change submitForm to update array.
    i. Explain thatsetstae causes rerender
    ii. Explain why we prevent default( so we don&#39;t refresh the page)
    iii. Explain why we make a newArray (reference vs copy)
7. TODO: make listItem component to learn passing props

**Extra Tasks for students:**

1. Add new item button
2. clear inputValue
3. Add Delete functionality
4. Sort List
