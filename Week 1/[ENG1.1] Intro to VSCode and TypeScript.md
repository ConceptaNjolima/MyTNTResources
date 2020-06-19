# Intro to VS Code and TypeScript

This lesson introduces VS Code and TypeScript including why this set of technology, a tour and basics using the IDE, and TypeScript fundamentals.

*Add debugging*

## Learning objectives

* TNTs will be able navigate VS Code.
* TNTs will be able to create new and run TypeScript file.
* TNTs will learn the basics of TypeScript datatypes, functions, components.

## Time required and pace

Total time: 1 hour 30 min

* 30 minutes - explain and explore: Visual Studio Code tour, create and run first TypeScript
* 35 minutes - explain and explore: introduction to TS datatypes, functions, components
* 10 minutes - elaborate: review
* 35 minutes - evaluate: fix and complete the code sample

## Background / review

* Load video before starting: https://www.youtube.com/watch?v=g8SCdMvUH2A
* [Getting started with Visual Studio Code](https://code.visualstudio.com/docs)
* [TypeScript in Visual Studio Code](https://code.visualstudio.com/docs/languages/typescript)
* [VS Code User Interface Guide](https://code.visualstudio.com/docs/getstarted/userinterface)
* [VS Code User Shortcuts](https://code.visualstudio.com/docs/getstarted/keybindings)
* [TS Hello World](https://code.visualstudio.com/docs/typescript/typescript-tutorial)
* [Basic TS data types](https://www.typescriptlang.org/docs/handbook/basic-types.html)

Pre-reqs

* [Visual Studio Code](https://code.visualstudio.com/)
* [Node.js Package Manager](https://www.npmjs.com/)

## Lesson details

### Visual Studio Code Tour, create and run TypeScript (30 minutes)

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
    1. Create a new folder, workspace, for the project using the command line.
    2. Create a file in workspace
    3. Declare and print the string

    ```typescript
    let message: string = 'Hello World';
    console.log(message);
    ```

    4. Compile the TS code. TS compiles to JS and runs as JS. In the terminal `tsc filename.ts`. `filename.js` is created. 
    5. Run the code. Enter `node helloworld.js` in the command line.
    6. Create a file call tsconfig.json in the same folder. This indicates the root of a TS file and defines how the project is compiled.
    7. Add the following lines to tsconfig.json:
    
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

    8. While in your typescript file click on the debug/run menu and click start debugging.
        * Select node.js as the environment. This allows you to run the typescript file and set breakpoints/debug the file
        * Running switches to the Run tab in the side bar. Click the top 'Explorer' icon to get back to the folder view.

4. VS Code TS language support features
    * Introduce and demo - IntelliSense and Code Snippets.
    * Here to help but you need to drive and understand the road.
    * IntelliSense - code completion, hover info, and signature information.
    * Snippets - chunks of TS.

5. **Try it** - NTs create and run HelloWorld.ts

### Introduction to TS datatypes, functions, components (35 minutes)

Samples for datatypes, functions, objects, and classes are available here: [Intro_TS.ts]([ENGresource]Intro_TS.ts). Open the file VS Code to talk through it with the descriptions that follow.

1. Datatypes - [overview of the datatypes](https://www.typescriptlang.org/docs/handbook/basic-types.html), [overview of variable declarations](https://www.typescriptlang.org/docs/handbook/variable-declarations.html)
    * Datatypes - what type of value can be assigned to a variable depends on the datatype. Boolean for true false statements, numbers, strings for text...
    * TypeScript uses types to describe data (get it, *Type*Script), JS doesn't
    * There are three different ways to define a variable.
       * `var` - scope, where it can be used from, is global or function/locally making it easy to accidently re-define.
       * `let` - block, scoped. Block in TS is a chunk of code bounded by {}. Let makes it easier to manage variables
       * `const` - maintain the same value, cannot be updated, can only be accessed within the block it was declared.
    * `let` is used to define variables inside a scope and var can be accessed outside a scope

2. Functions - [overview of functions](https://www.typescriptlang.org/docs/handbook/functions.html#functions)
    * Functions are building blocks of applications in JS.
    * They're used for abstraction, TS also has classes, name spaces, and modules.
    * Functions can be named or anonymous.
       * *Why is it important at this stage*
    * Functions can have types and optional default parameters
      * Types define the datatypes of the variables passed into and returned from the function.
      * Parameters are what's passed into the function.

3. Objects - [overview of objects](https://www.tutorialspoint.com/typescript/typescript_objects.htm)
   * An object represents key value pairs that describe something. For example a rectangle has length and width. A contact may have name, phone number and address.
   * Reference - creates an additional name for the same object. Changing a value in the reference object, changes the original object.
   * Copy - creates a copy of the object. Changing the copy object will not impact the original object.
   * An interface represents one of TypeScripts core principles, type checking the shape values have. Interfaces name the types.

4. Class - [overview of classes](https://www.typescriptlang.org/docs/handbook/classes.html#classes)
   * A class in object-oriented programming languages, like TypeScript is a template for creating objects. Classes are a feature of TS, only available in more recent versions of JS (from 2015 onwards).
   * A class contains properties, constructors, and methods. Constructors are methods automatically invoked when an instance of the class is created.
   * In a class, `this.` denotes that it's referring to one of the members in the class.
   * `new` is used to construct an instance of the class.
   * TS also introduces inheritance. Inheritance extends classes.
      * Classes inherit properties and methods from the base class.
      * View the [animal class example](https://www.typescriptlang.org/docs/handbook/classes.html#inheritance).

5. Components - [overview of components](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-1-8.html#function-components-in-react)
    * Components are building blocks of React Apps that split up the UI intro reusable pieces
    * Conceptually they're like JS functions, the accept inputs "props" and return React elements that describe what should appear on the screen, or how the user interface should *react*
    * More on React in a future lesson
    
6. Debugging through VS Code *to add*

7. **Try it** - NTs clone a sample repo with different data types and functions
    * To clone the sample, start in VS Code.
       1. From GitHub, copy the file path: Week 1/[ENGresource]Intro_TS.ts.
       2. In empty Explorer tab click the "Clone Repository" or in the command palette type `git: Clone`.
    * *todo - instructions for cloning and running*

### Review (10 minutes)

1. Poll the room - what went well, what didn't go well?
2. Walk through any blocking concepts, demo code snippets that cause confusion

### Fix and complete the code sample (35 minutes)

1. Open the file.
2. Read through the code comments and identify what the code is trying to do.
3. Try running the code, why isn't it working?
4. Fix the code and complete the sample.

## Stretch

* [TypeScript vs JavaScript pros and cons](https://www.youtube.com/watch?v=D6or2gdrHRE) - dig into the pros and cons of TypeScript compared to JavaScript.
* [TypeScript Playground](https://www.typescriptlang.org/play/index.html) - check out the online editor for quickly running and experimenting with TS.
* [What's the difference between a console, a terminal, and a shell](https://www.hanselman.com/blog/WhatsTheDifferenceBetweenAConsoleATerminalAndAShell.aspx)
