# Intro to VS Code and TypeScript
This lesson introduces VS Code and TypeScript including why this set of technology, a tour and basics using the IDE, and TypeScript fundamentals. 

*Open questions in lesson plan*
* *VS code already set up?*
* *Thoughts on people behind product bit?*

## Learning objectives
* TNTs will be able navigate VS Code.
* TNTs will be able to create new and run TypeScript file.
* TNTs will learn the basics of TypeScript datatypes, functions, components.

## Time required and pace
Total time: 1.5 hour
* 10 minutes - engage: people behind the product
* 60 minutes - explain and explore: Visual Studio Code tour, create and run first TypeScript, intro datatypes, functions, components
* 5 minutes - elaborate: review trouble spots
* 15 minutes - evaluate: specific activity to demonstrate understanding

## Background / review
* Load video before starting: https://www.youtube.com/watch?v=g8SCdMvUH2A
* [Getting started with Visual Studio Code](https://code.visualstudio.com/docs)
* [TypeScript in Visual Studio Code](https://code.visualstudio.com/docs/languages/typescript)
* [VS Code User Interface Guide](https://code.visualstudio.com/docs/getstarted/userinterface)
* [VS Code User Shortcuts](https://code.visualstudio.com/docs/getstarted/keybindings)
* [TS Hello World](Tutorial)
* [What's the difference between a console, a terminal, and a shell](https://www.hanselman.com/blog/WhatsTheDifferenceBetweenAConsoleATerminalAndAShell.aspx)

Pre-reqs
* [Visual Studio Code](https://code.visualstudio.com/)
* [Node.js Package Manager](https://www.npmjs.com/)

## Lesson details
### People behind the products (10 minutes)
1. Visual Studio Code (VS Code) is the integrated development environment we'll use to build apps. It's bulit by Microsoft and was released in 2015.
2. It represents a significant change in how Microsoft builds and ships products. 
    * It's lightweight and customizable, you can install what you need to use. 
    * It's an [open source project](https://github.com/microsoft/vscode), anyone can contribute. Over 19.1K people contributed in 2019 ([GitHub - State of the Octoverse](https://octoverse.github.com/)). 
    * It works on Windows, Mac OS, and Linux. 
    * It was the most popular IDE in the [StackOverflow 2019 Developer Survey](https://insights.stackoverflow.com/survey/2019#development-environments-and-tools).
3. The product is the result of customer driven engineering, understanding user needs and building software that does a great job at meeting the user needs. Testing and validating hypothesis and aplying user feedback.
4. Julia Liuson is the head of Microsoft's developer division and lead the culture change that enabling building this prouct. In 2019 she was inducted into to the Women in Technology Hall of Fame.
5. Here's a little bit about Julia Liuson [YouTube](https://www.youtube.com/watch?v=g8SCdMvUH2A) 

### Visual Studio Code Tour, create and run TypeScript (60 minutes)
1. Open VS Code, without a workspace folder open.
    * Highlight the activity bar, status bar, and side bar.
    * Highlight the "Help" option in the toolbar for quick access to references.
    * Call out that "Learn" is in the landing page. It takes time to get to adopt VS Code, for everyone.

2. Install the TypeScript compiler `tsc`.
     * TypeScript language is supported out of the box. The TypeScript compiler must be installed.
     * `npm install -g typescript`, the `-g` installs it globally
     * Checked that it installed correctly by checking the version `tsc --version`
     * Review using the terminal - integrated in VS Code for command line tasks like installation. The terminal can be opened from "View" in the toolbar or `Ctrl+\`` 
     * Review npm - an online repository for publishing open-source node.js projects and a command line utility for interacting with the repo for package installation, version management, and dependency management. It makes it easy to install and mantain packages. [What is node](https://nodejs.org/en/knowledge/getting-started/npm/what-is-npm/).

3. **Demo** - Hello World tutorial [instructions](https://code.visualstudio.com/docs/typescript/typescript-tutorial)
    * Create a new folder, workspace, for the project
    * Create a file in workspace
    * Declare and print the string <br /> 
    ```typescript
    let message: string = 'Hello World';
    console.log(message);
    ```
    * Compile the TS code. TS compiles to JS and runs as JS. In the terminal `tsc filename.ts`. `filename.js` is created.
    * In the terminal `node filename.js` to run the JS file. Look for the output in the terminal.

4. VS Code TS language support features
    * Introduce and demo - IntelliSense and Code Snippets.
    * Here to help but you need to drive and understand.
    * IntelliSense - code compleetion, hover info, and signature information.
    * Snippets - chunks of TS.
    
5. **Try it** - NTs create and run HelloWorld.ts

---


## Stretch
[Links and other projects for further learning and exploration]
