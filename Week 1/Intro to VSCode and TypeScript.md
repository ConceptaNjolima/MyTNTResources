# Intro to VS Code and TypeScript
This lesson introduces VS Code and TypeScript including why this set of technology, a tour and basics using the IDE, and TypeScript fundamentals. 

*Open questions in lesson plan*
* *VS code already set up?*
* *Thoughts on people behind product bit?*
* *Sample code needed*
* *What's the classroom management for code samples? Branch? Fork? into NT's repo, room repo, team repo? Naming conventions?*

## Learning objectives
* TNTs will be able navigate VS Code.
* TNTs will be able to create new and run TypeScript file.
* TNTs will learn the basics of TypeScript datatypes, functions, components.

## Time required and pace
Total time: 1.5 hour
* 10 minutes - engage: people behind the product
* 20 minutes - explain and explore: Visual Studio Code tour, create and run first TypeScript 
* 35 minutes - explain and explore: introduction to TS datatypes, functions, components
* 10 minutes - elaborate: review
* 15 minutes - evaluate: fix and complete the code sample

## Background / review
* Load video before starting: https://www.youtube.com/watch?v=g8SCdMvUH2A
* [Getting started with Visual Studio Code](https://code.visualstudio.com/docs)
* [TypeScript in Visual Studio Code](https://code.visualstudio.com/docs/languages/typescript)
* [VS Code User Interface Guide](https://code.visualstudio.com/docs/getstarted/userinterface)
* [VS Code User Shortcuts](https://code.visualstudio.com/docs/getstarted/keybindings)
* [TS Hello World](https://www.typescriptlang.org/docs/handbook/basic-types.html)
* [Basic TS data types](https://www.typescriptlang.org/docs/handbook/basic-types.html)
* [What's the difference between a console, a terminal, and a shell](https://www.hanselman.com/blog/WhatsTheDifferenceBetweenAConsoleATerminalAndAShell.aspx)

Pre-reqs
* [Visual Studio Code](https://code.visualstudio.com/)
* [Node.js Package Manager](https://www.npmjs.com/)

## Lesson details
### People behind the products (10 minutes)
1. Visual Studio Code (VS Code) is the integrated development environment we'll use to build apps. It's built by Microsoft and was released in 2015.
2. It represents a significant change in how Microsoft builds and ships products. 
    * It's lightweight and customizable, you can install what you need to use. 
    * It's an [open source project](https://github.com/microsoft/vscode), anyone can contribute. Over 19.1K people contributed in 2019 according to the [GitHub State of the Octoverse report](https://octoverse.github.com/). 
    * It works on Windows, Mac OS, and Linux. 
    * It was the most popular IDE in the [StackOverflow 2019 Developer Survey](https://insights.stackoverflow.com/survey/2019#development-environments-and-tools).
3. The product is the result of customer driven engineering, understanding user needs and building software that does a great job at meeting the user needs. Testing and validating hypothesis and applying user feedback.
4. Julia Liuson is the head of Microsoft's developer division and lead the culture change that enabling building this product. In 2019 she was inducted into to the Women in Technology Hall of Fame.
5. Here's a little bit about Julia Liuson ([YouTube](https://www.youtube.com/watch?v=g8SCdMvUH2A)).

### Visual Studio Code Tour, create and run TypeScript (20 minutes)
1. Open VS Code, without a workspace folder open.
    * Highlight the activity bar, status bar, and side bar.
    * Highlight the "Help" option in the toolbar for quick access to references.
    * Call out that "Learn" is in the landing page. It takes time to get to adopt VS Code, for everyone.

2. Install the TypeScript compiler `tsc`.
     * TypeScript language is supported out of the box. The TypeScript compiler must be installed.
     * `npm install -g typescript`, the `-g` installs it globally
     * Checked that it installed correctly by checking the version `tsc --version`
     * Review using the terminal - integrated in VS Code for command line tasks like installation. The terminal can be opened from "View" in the toolbar or `Ctrl+\`` 
     * Review npm - an online repository for publishing open-source node.js projects and a command line utility for interacting with the repo for package installation, version management, and dependency management. 
         * It makes it easy to install and maintain packages. [What is node](https://nodejs.org/en/knowledge/getting-started/npm/what-is-npm/).
         * A package contains all the files needed for a module.
         * A module is a file that's re-used throughout an application.

3. **Demo** - Hello World tutorial [instructions](https://code.visualstudio.com/docs/typescript/typescript-tutorial)
    * Create a new folder, workspace, for the project
    * Create a file in workspace
    * Declare and print the string <br /> 
    ```typescript
    let message: string = 'Hello World';
    console.log(message);
    ```
    * Compile the TS code. TS compiles to JS and runs as JS. In the terminal `tsc filename.ts`. `filename.js` is created.
    * Create a file call tsconfig.json in the same folder.
    * add the following lines to tsconfig.json:
    ```
    {
      "compilerOptions": {
        "target": "es5",
        "module": "commonjs",
        "outDir": "out",
        "sourceMap": true
      }
    }
    ```
    * while in your typescript file click on the debug/run menu and click start debugging
    * select node.js as the environment
    this allows you to run the typescript file and set breakpoints/debug the file

4. VS Code TS language support features
    * Introduce and demo - IntelliSense and Code Snippets.
    * Here to help but you need to drive and understand.
    * IntelliSense - code completion, hover info, and signature information.
    * Snippets - chunks of TS.
    
5. **Try it** - NTs create and run HelloWorld.ts

### Introduction to TS datatypes, functions, components (35 minutes)
1. Datatypes - [overview of the datatypes](https://www.typescriptlang.org/docs/handbook/basic-types.html).
    * Datatypes - what type of value can be assigned to a variable depends on the datatype
    * TypeScript uses types to describe data (get it, *Type*Script), JS doesn't 
    * `let` is used to define variables inside a scope and var can be accessed outside a scope
    * *todo - sample of let vs var vs const*

2. Functions - [overview of functions]()
    * Functions are building blocks of applications in JS
    * They're used for abstraction, TS also has classes, name spaces, and modules
    * Functions can be named or anonymous
    * Functions can have types and optional default parameters
    * Let's talk about `this` parameter
    * *todo - sample of functions

3. Objects
   * reference vs Copy
   * Interface
   
4. Class
   * *todo - sample classes 

5. Components - [overview of components]()
    * Components are building blocks of React Apps that split up the UI intro reusable pieces
    * Conceptually they're like JS functions, the accept inputs "props" and return React elements that describe what should appear on the screen, or how the user interface should *react*
    * More on React in a future lesson

6. **Try it** - NTs clone a sample repo with different data types and functions
    * *todo - create code sample*
    * *todo - instructions for cloning and running*
    
### Review (10 minutes)
1. Poll the room - what went well, what didn't go well?
2. Walk through any blocking concepts, demo code snippets that cause confusion

### Fix and complete the code sample (15 minutes)
1. Fork the repo - 
2. Read through the code comments and identify what the code is trying to do.
3. Try running the code, why isn't it working?
4. Fix the code and complete the sample.
5. Push the changes back to your fork.

## Stretch
[Links and other projects for further learning and exploration]
