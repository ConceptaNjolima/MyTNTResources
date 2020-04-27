# UI Debugging

This lesson explains how you can debug UI in Edge (Chromium) and introduces the developer tools in more detail.

## Learning objectives

* TNTs will learn about basic debugging
* TNTs will understand Edge's debugging UI
* TNTs will understand how to make file changes while debugging
* TNTs will practice the debugging tools

## Time required and pace

Total time: 1.1 hours

* 10 minutes – Navigating around Edge developer tools
* 20 minutes – Debugging basics
* 20 minutes - File changes while debugging
* 20 minutes - Exercise

## Background / review

* Enable Developer Tools in Microsoft Edge

## Lesson details

### Edge Debugger UI (10 minutes)

The developer tools are best shown in action. Open a website and show and demo the panels.

The developer tools provide several panels to assist with debugging. Here are a few noteworthy panels:

1. Elements panel - View the DOM and CSS
2. Console panel - View messages and logs
3. Sources panel - View resources loaded by the web page and debug Javascript files via breakpoints
4. Network panel - View network traffic, HTTP status codes, file types, file size, download times, etc.
5. Performance - View performance metrics

### Debugging Basics (20 minutes)

1. View the console panel for any errors or warnings
2. Use the Sources panel to pause your code with breakpoints and view the call stack, variables, threads and more
3. When your breakpoint has been hit then you have a few actions you can take:
    * Pause/Resume: Stop and continue debugging
    * Step Over: Gives you the ability to "step over" a line of code
    * Step Into: Go further into a function call
    * Step Out: If you've decided to Step Into a line of code to go back you can Step Out to navigate back to your last line of code

### File Changes While Debugging (20 minutes)

Let's explore the Elements panel to see how it can help us with UI debugging.

1. Navigating the DOM
2. Edit the DOM - Add or remove HTML elements to preview the layout
3. Edit the CSS - Update classes to see changes
4. Break on DOM modifications - You can start debugging on any DOM element changes that have been made by Javascript

### Exercise: Explore with the UI debugger (15 minutes)

1. Go to [www.microsoft.com](www.microsoft.com)
2. Open Developer tools.
3. Familiarize yourself with the panels.
4. In the Console, what warnings do you see? Share with you team.
5. With the elements panel, change the color of the banner and on screen change some text. Post a screenshot to your Team's channel.