# Components

This lesson explains how you can layout components

## Learning objectives

* TNTs will understand how to layout a table with React
* TNTs will understand the basics of CSS flexbox layout

## Time required and pace

Total time: 1 hour

* 15 minutes – Building a table with react
* 15 minutes – Explain the basics of CSS flexbox
* 30 minutes - Practice

## Background / review

## Lesson details

### Building a Table component (15 minutes)

Start to think about the elements required for a basic HTML table such as a table header and table rows. These elements can help us start to build a Table component that can be reused.

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

Configuring the Table component with data will allow us to dynamically create the table headers and rows.

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



### Build a React table with CSS flexbox (30 minutes)
*Exercise for NTs building a table with basic CSS flexbox layout*

## Stretch (20 minutes)

  1. Extract the table into components.
