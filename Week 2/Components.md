#
# Components Explained

This lesson explains in detail how a component works and how it&#39;s methods function

## **Learning objectives**

- TNTs will understand how a component&#39;s key methods function
- TNTs will understand how the store, reducer and actions work together

## **Time required and pace**

Total time: 1.5 hour

- 20 minutes – explain basic component&#39;s content
- 10 minutes – Explain component&#39;s lifecycle
- 20 minutes - practice

## **Background / review**

- Component Properties
- Component State
- Interfaces
- Component render()

## **Lesson details**

### **Component description(20 minutes)**

A component is an object that returns a Javascript XML Element (JSX Element)

There are two types of components:

1)Function Components

Example:

    function App(Properties:any) {

        return <div>Hello World</div>

    }

2) Class Components

       export default class Tile extends React.Component<Properties, State>{

          render() {

              return (

                  <div>Hello World</div>

              )

          }

       }

### **Class Component ( 10minutes):**

1. **1.** Render (required): This method returns the JSX element to be displayed by the class. It runs whenever the component&#39;s view updates.
2. **2.** Properties (optional): This are arguments passed into the component from its parent components. They cannot be changed by the component.
3. **3.** State (optional): This is are arguments that exists only withing the component. Changing them causes the component to update
4. **4.** LifeCycle methods: as component gets introduced

### **Function Component ( 10minutes):** Add redux to list app

1. The function is expected to return the JSX element to be displayed.
2. Properties (optional): These arguments are passed in from the component&#39;s parent similarly to passing parameters to a function. They cannot be changed in the component.
3. UseState: A hook function that returns a state variable, giving function components a way to manipulate a state the way class components do.

### **LifeCycle Methods (10 minutes)**

These are methods that are trigger through out a components existence from when they&#39;re constructed to when they are dismissed.

### PICTURE

[https://www.w3schools.com/react/react\_lifecycle.asp](https://www.w3schools.com/react/react_lifecycle.asp)

## **Stretch (20 minutes)**


  1. Convert a giving class Component to a functionComponent.
  2. Convert a given function component to a class component.
