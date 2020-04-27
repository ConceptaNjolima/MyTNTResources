# Component Layout

This lesson explains how to layout components, how to organize components with alignment and distribute space dynamically.

## Learning objectives

* TNTs will learn how to layout a table with React
* TNTs will understand the basics of CSS Flexbox layout
* TNTs will practice using Flexbox

## Time required and pace

Total time: 1 hour

* 15 minutes – Building a table with react
* 15 minutes – Explain the basics of CSS Flexbox
* 30 minutes - Practice

## Background / review

## Lesson details

### Building a Table component (15 minutes)

Start to think about the elements required for a basic HTML table such as a table header and table rows. These elements can help us start to build a Table component that can be reused.

Below a basic HTML Table Element

    <table>
        <thead>
            <th>Name</th>
            <th>Email</th>
            <th>Phone Number</th>
        </thead>
        <tbody>
            <tr>
                <td>John Appleseed</td>
                <td>john.appleseed@microsoft.com</td>
                <td>(555) 555-5555</td>
            </tr>
        </tbody>
    </table>

If we configure our Table component with data this will allow us to dynamically create the table headers and rows. We can convert the basic table element above into our Table component below.

    render() {
        return (
            <table>
                <thead>
                    {this.header()}
                </thead>
                <tbody>
                    {this.rows()}
                </tbody>
            </table>
        )
    }

### CSS Flexbox layout (15 minutes)

The Flexbox Layout is an efficient way to layout and distribute child items in a parent container allowing for child items to either take up space or shrink based on the UI requirements.

When configuring a Flexbox layout both the Parent Container and Children Items have properties you can set to meet your UI needs. We will go more in depth in ENG3.1 Adaptive Layouts.

Below are a few examples of Flexbox properties for both the Parent Container and Child Items.

Parent Properties:

    flex-direction: row | row-reverse | column | column-reverse

![FlexDirection](./flex-direction.svg)

Children Properties:

    flex-grow or flex-shrink

![FlexGrowShrink](./flex-grow.svg)

[https://css-tricks.com/snippets/css/a-guide-to-flexbox/](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
### Practice: Build a React table with CSS flexbox (30 minutes)
*Exercise for NTs building a table with basic CSS flexbox layout*

## Stretch (20 minutes)

  1. Extract the table into Header and Row components.
  2. Add filtering to the Table component.
