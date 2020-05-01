# Component Libraries

This lesson provides an overview of component libraries specifically Fluent UI, how to use and tips on reading documentation

## Learning objectives

* TNTs will understand what component libraries are
* TNTs will understand how to import component libraries into their project
* TNTs will understand how to add components to their existing project

## Time required and pace

Total time: 1.25 hours

* 15 minutes – what are component libraries
* 15 minutes – installing/using Fluent UI
* 15 minutes - how to read documentation
* 30 minutes - practice building a new React component using Fluent UI components

## Lesson details

### What are component libraries (15 minutes)

A component library is a collection of components installed generally through a package manager that provides common solutions whether it's a UI library, testing library, etc.

Why use a component library?

* Prebuilt out of the box solutions
* Increase speed of delivery
* Customization of an application
* Allows focus on core application competencies vs boilerplate features

Things to consider before using a component library

* Components may become outdated as other technologies advance
* Consider the popularity and communitity activity for the component library
* Ease of use generally through an API defined by the component library
* Tradeoffs between speed, customization time, cost and immediate business needs

### Installing/Using Fluent UI (15 minutes)

[https://developer.microsoft.com/en-us/fluentui#/get-started](https://developer.microsoft.com/en-us/fluentui#/get-started)

We will use Microsofts Fluent UI to practice using a component library. Using an existing project in the terminal use npm to install the component library.

    npm install @fluentui/react

Using a few steps we can start using a component. In the example below we are using Fluent UI's Persona component.

1. Import the component at the top of your file

       import { Persona } from "@fluentui/react"

2. Add the Persona component in the render function of a Component class

        export default class MyPersona extends Component<MyPersonaProps> {
            render() {
                return (
                    <div id="persona-container">
                        <Persona
                            imageUrl={this.props.imageUrl.href}
                            text={this.props.text}
                            secondaryText={this.props.secondaryText}
                        />
                    </div>
                );
            }
        }

3. Note: Persona (and other components) allows customization via its properties e.g. imageUrl, text and secondaryText

### How to read documentation (15 minutes)

Most (if not all) libraries will contain a "How to" section to quicky get started but may not include how to use all the components. This is where knowing how to interpret documentation and more importantly class interfaces.

A few tips on reading documentation:

* Look for examples or demos
* Class interfaces

Below is a link to Persona properties interface.

[https://developer.microsoft.com/en-us/fluentui#/controls/web/persona](https://developer.microsoft.com/en-us/fluentui#/controls/web/persona)

* Explain interfaces
* Explain the use of 'extends' and how to navigate interface extensions

### Practice: Building a new component using Fluent UI (30 minutes)

Build a FeedItem component that is made up of multiple components. Using Fluent UI, CSS Flexbox and CSS styling build the component below. Which Fluent UI components to use are labeled.

![feedItem](./fluent-ui-practice.png)

### Stretch

1. Create a Feed component that will display multiple FeedItems
2. Add a TextField component so users can leave comments
