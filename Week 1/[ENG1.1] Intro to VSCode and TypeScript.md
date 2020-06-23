# Intro to VS Code and TypeScript

This lesson introduces Visual Studio Code and TypeScript including why this set of technology is important, a tour and basics of using the IDE, and TypeScript fundamentals.

[TypeScript](https://www.typescriptlang.org) is a typed superset of JavaScript. It permits, in particular, to define classes, modules and interfaces. 

## Learning objectives

* TNTs will be able to navigate Visual Studio Code.
* TNTs will be able to create new and run TypeScript file.
* TNTs will learn the basics of TypeScript datatypes, functions, classes etc.

## Time required and pace

Total time: 1 hour 30 min

* 30 minutes - explain and explore: VS Code tour, create and run first TS code
* 35 minutes - explain and explore: introduction to TS datatypes, functions, classes etc.
* 10 minutes - elaborate: review
* 35 minutes - evaluate: fix and complete the code sample

## Background / review

* Watch the video: https://www.youtube.com/watch?v=g8SCdMvUH2A
* [Getting started with VS](https://code.visualstudio.com/docs)
* [TypeScript in VS Code](https://code.visualstudio.com/docs/languages/typescript)
* [VS Code User Interface Guide](https://code.visualstudio.com/docs/getstarted/userinterface)
* [VS Code User Shortcuts](https://code.visualstudio.com/docs/getstarted/keybindings)
* [Debugging in VS](https://code.visualstudio.com/docs/editor/debugging)
* [TS Hello World](https://code.visualstudio.com/docs/typescript/typescript-tutorial)
* [Basic TS datatypes, functions and more](https://www.typescriptlang.org/docs/handbook/basic-types.html)

Pre-reqs

* [Visual Studio Code](https://code.visualstudio.com/)
* [Node.js Package Manager](https://www.npmjs.com/)

## Lesson details

### Visual Studio Code Tour, create and run TypeScript (30 minutes)

1. Open VS Code, without a workspace folder open.
    * Highlight the activity bar, status bar, and side bar.
    * Highlight the terminal.
    * Highlight the "Help" option in the toolbar for quick access to references.
    * Call out that "Learn" is in the landing page. It takes time to get to adopt VS Code, for everyone.

2. Install the TypeScript compiler `tsc`.
     * TypeScript language is supported out of the box. But the TypeScript compiler must be installed.
     * `npm install -g typescript`, the `-g` installs it globally
     * Checked that it installed correctly by checking the version `tsc --version`
     * Review using the terminal - integrated in VS Code for command line tasks like installation and execution. The terminal can be opened from "View" in the toolbar or Ctrl+` or the side bar
     * Review npm - an online repository for publishing open-source node.js projects and a command line utility for interacting with the repo for package installation, version management, and dependency management.
         * [What is node?](https://nodejs.org/en/knowledge/getting-started/npm/what-is-npm/).
         * It makes it easy to install and maintain packages. 
         * A package contains all the files needed for a module.
         * A module is a file that's re-used throughout an application.

3. **Demo** - Hello World tutorial [instructions](https://code.visualstudio.com/docs/typescript/typescript-tutorial)
    1. Create a new folder, workspace, for the project using the terminal command line, and launcch VS code using `code .`.
    2. Create a file in workspace and rename it as `hellworld.ts`.
    3. Write the following TS code that declares and prints the string message.

    ```typescript
    let message: string = 'Hello World';
    console.log(message);
    ```

    4. Compile the TS code. TS compiles to JS and runs as JS. In the terminal type `tsc filename.ts`. `filename.js` is created. 
    5. Run the code. Enter `node helloworld.js` in the command line.
    6. Create a file called `tsconfig.json` in the same folder. This indicates the root of a TS file and defines how the project is compiled.
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

    Run `tsc` (no parameters). JS files are now in the directory `out`.
    
    8. While in your TS file, click on the debug/run icon in the activity bar or on Run / Start Debugging in the menu.
        * Create a `launch.json` configuration file. Select Node.js as the environment. This allows you to run the TS file in debug mode. 
        * You can set breakpoints/logpoints/debug the file. 
        * Running switches to debug in the side bar. Check the debug console.
        * Once you have a debug breakpoint or other, the debug toolbar will appear with different options (Continue/Pause, Step over/into/out, Restart, Stop).
        * Click the top 'Explorer' icon to get back to the folder view.

4. VS Code TS language support features
    * Introduce and demo - IntelliSense and Code Snippets.
    * Here to help but you need to drive and understand the road.
    * IntelliSense - code completion, hover info, and signature information.
    * Snippets - chunks of TS.

5. **Try it** - NTs create and run HelloWorld.ts

### Introduction to TS datatypes, functions, classes etc. (35 minutes) 

Samples for datatypes, functions, objects, and classes are available here: [Intro_TS.ts]([ENGresource]Intro_TS.ts). Open the file in VS Code to talk through it with the descriptions that follow.

1. Datatypes - [overview of the datatypes](https://www.typescriptlang.org/docs/handbook/basic-types.html), [overview of variable declarations](https://www.typescriptlang.org/docs/handbook/variable-declarations.html)
    * Datatypes - what type of value can be assigned to a variable depends on the datatype. Boolean for true false statements, numbers, strings for text...
    * TS uses types to describe data (get it, *Type*Script), JS doesn't
    * There are three different ways to define a variable.
       * `var` - scope, where it can be used from, is global or function/locally making it easy to accidently re-define.
       * `let` - block, scoped. Block in TS is a chunk of code bounded by {}. Let makes it easier to manage variables
       * `const` - maintain the same value, cannot be updated, can only be accessed within the block it was declared.
    * `let` is used to define variables inside a scope and var can be accessed outside a scope

2. Functions - [overview of functions](https://www.typescriptlang.org/docs/handbook/functions.html#functions)
    * Functions are building blocks of applications in JS.
    * They're used for abstraction. TS also has classes, name spaces, and modules.
    * Functions can be named or anonymous.
       * *Why is it important at this stage?*
    * Functions can have types and optional default parameters
      * Types define the datatypes of the variables passed into and returned from the function.
      * Parameters are what's passed into the function.

   ```typescript
   function mult2(x: number): number {
      return 2*x;
   }
   ```

3. Objects - [overview of objects](https://www.tutorialspoint.com/typescript/typescript_objects.htm)
   * An object represents key value pairs that describe something. For example, a rectangle has length and width. A contact may have name, phone number and address.
   * Reference - creates an additional name for the same object. Changing a value in the reference object, changes the original object.
   * Copy - creates a copy (clone) of the object. Changing the copy object will not impact the original object.
   * An [interface](https://www.typescriptlang.org/docs/handbook/interfaces.html) represents one of TS core principles, type checking the shape values have. Interfaces name the types.

   ```typescript
   // Object
   let boss = {
       name:"Michael Scott",
       phone:"555-555-5555",
       address: "Scranton, PA"
   }
   
   // Interface
   interface Bosses {
    name: string;
    phone: number;
    address: string;
    bossrank: number;
   }

   const michaelScott:Bosses = {
    name:"Michael Scott",
    phone:555555555,
    address: "Scranton, PA",
    bossrank: 1
   }
   ```   

4. Class - [overview of classes](https://www.typescriptlang.org/docs/handbook/classes.html#classes)
   * A class in object-oriented programming languages, like TS, is a template for creating objects. Classes are a feature of TS, only available in more recent versions of JS (from 2015 onwards).
   * A class contains properties, constructors, and methods. Constructors are methods automatically invoked when an instance of the class is created.
   * In a class, `this.` denotes that it's referring to one of the members in the class.
   * `new` is used to construct an instance of the class.
   * TS also introduces inheritance. Inheritance extends classes.
      * Classes inherit properties and methods from the base class.
      * View the [animal class example](https://www.typescriptlang.org/docs/handbook/classes.html#inheritance).
   
 5. Arrow functions - [overview of arrow functions](https://www.typescriptlang.org/docs/handbook/functions.html)
   * Fat arrow notation (`=>`) is used for anonymous functions. They are also called lambda functions.
   * We drop the need of the `function` keyword and use `let`.
   * This notation separates the parameters (left-hand side) from the function body (right_hand side).
   * If the function does not return anything, use `void`.

   ```typescript
   let sayHi = (): string => {return "Hello!!!"};
   
   // TS syntax without =>
   function mult2_ts(x: number): number {
     return 2*x;
   }
   
   // TS with => and without types
   let mult2_b = x => 2*x;
   
   // TS with => and with types
   let mult2_e: (number) => number = x => 2*x;
   
   // using =>, types and return
   let mult2_a = (x:number):number => {
     return 2*x;
   }
   ```

6. Generics - [overview of generics](https://www.typescriptlang.org/docs/handbook/generics.html)
   * Generics permit components to work on a variety of types rather a single one. They also constraint the component.
   * Types are declared with `<>`, e.g., <string>.
      
   ```typescript
   // array of strings
   let myarray:Array<string> = ["Microsoft", "TNTs"];
   
   // using the type any
   function fun(args: any): any {
    return args;
   }

   // using generics
   function fun_g<T>(args:T):T {
    return args;
   }
   
   // custom array class - array of Ts
   class customArray<T> {
    items: T[];

    constructor() {
        this.items = []
    }
  
    getItems(): T[] {
      return this.items;
    }

    addItem(item:T):void {
        this.items.push(item);
    }
   }
   ```

7. **Try it** - NTs clone a sample repo with different data types and functions
    * To clone the sample, start in VS Code.
       1. In the command palette (CTRL+SHIFT+P) type `git: Clone`. Click on Clone from GitHub and enter your GitHub credentials.
       2. Enter tnt-summer-academy to search for the tnt-summer-academy/Samples repository and select the local directory you want to clone. 
       3. Find IntroTS.ts in the clone repository.
    
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
