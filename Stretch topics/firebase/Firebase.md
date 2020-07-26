# Using Firebase In A React App



## Learning objectives

* TNTs will understand what a document-oriented database is (e.g., Cosmos DB, MongoDB, Firebase)
* TNTs will be able to create a new 'app' in Firebase
* TNTs will be able to create, read, update, and delete information in their Firebase database using the Firebase website
* TNTs will be able to access their Firebase database programmatically, including the normal CRUD operations

## Instructional session (60 minutes)

### Lesson Overview

1. Let's look at what a JSON 'database' is by looking at Firebase
   1. Let's look at Firebase
   2. Let's look at what JSON is
2. What *should* you put in a DB?
3. How do we access the database from code?
   1. Setting up your app
   2. How to get your app's database configuration info
   3. Configuring your app to connect to the DB
   4. get a reference to the place in the JSON doc that you want to modify
   5. call set / once / update / remove / push on the ref
   6. if you want to know whether it worked or not use Promise.then to run code once it's finished
       (or skip it)

### Let's look at Firebase:

1. [Sign up for Firebase on their website.](https://firebase.google.com/)
   (It's free)
   
2. Set up a Firebase project
   [Step-by-step guide](https://www.robinwieruch.de/firebase-tutorial)
   
   - Pick a name
   - Say 'No' to Google Analytics :)
   
3. Next, the left-hand column open up the 'Develop' tab and click on 'Database':
   ![image-20200725213338671](images/Firebase/image-20200725213338671.png)
   
4. Next, you'll need to create a new database.  
   We're going to use the "Realtime Database", NOT Cloud Firestore:
   <img src="images/Firebase/image-20200725214151388.png" alt="image-20200725214151388" style="zoom:33%;" />


   <img src="images/Firebase/image-20200725214631721.png" alt="image-20200725214631721" style="zoom:67%;" />

5. For now let's use "test mode", since it will be easier to connect to.  (You can change this later on if you'd like)
   <img src="images/Firebase/image-20200725214833974.png" alt="image-20200725214833974" style="zoom: 67%;" />

6. Your database will start out empty, if you move the mouse over an element you'll be given the option to add sub-items or to remove the item:
   <img src="images/Firebase/image-20200725213531805.png" alt="image-20200725213531805" style="zoom:67%;" />

### Exercise:

Try to re-create the picture above.  Instead of using the values "MD71v0ibmwQZcgjZllF" and "MD720Xu3P31HxCJ80Oh" feel free to use something that's easier to type, such as "2" and "3"

### Let's look at what JSON is

There's a [rather lengthy article in Wikipedia about JSON which includes a lot of solid examples to browse through](https://en.wikipedia.org/wiki/JSON).  
The 'tree view' of the document (in our document database) is a typical example of how to think about JSON files.  

There's a couple of important points to remember when working with JSON files:

1. JSON files are very similar to object literals in JavaScript (and therefore similar-ish to object literals in TypeScript) but there are differences.  For example, and object literal in JS/TS does not need to put quotes around the field names...

   ```typescript
   let objectLiteral = {
     name: "A",
     email: "A@A.com"
   }
   ```

   ...but JSON files do need the quotes::

   ```json
   {
     "name": "A",
     "email": "A@A.com"
   }
   ```

2. There's no rules enforcing a certain structure, nor limiting what you can do with this.

   - On the one hand this is nice because you can add extra information or fields to any given part of the document, which can be handy (especially in web application development, because the browser will send the server a bunch of strings and these strings may or may not be consistent each time).
   - On the other hand computers are best at doing the exact same thing over and over, so when you've got a document that may have variations in the structure that may complicate your code

3. You CANNOT have circular references in the document

   - There are ways around this.  For example, instead of a reference you could put in an ID number, and then put stuff into the document in way that allows you to look up objects by ID number.

4. You CANNOT put comments into JSON files (at least officially)
   Because this was intended as a format for one program to send information to another program there's no way to add comments.  :(

### What *should* you put in a DB?

# NOT DONE YET

Let's talk briefly about what to put in here

For AppPrototype, maybe just put all of this.state into it?

Normally you'd only store data that you want to persist across runs of your program

### How do we access the database from code?

#### Setting up your app

1. Let's start by looking at your app (or [the sample project in the Samples repo](https://github.com/tnt-summer-academy/Samples/tree/main/Stretch/firebase))

2. You can install the Firebase support by typing in:
   `npm install firebase`

   - Note: you do NOT need `npm install @types/firebase` - the firebase package includes type defitions for TypeScript (I believe the Firebase JavaScript API itself is written in TypeScript)

3. Copy this into a new file (named, say, `myFirebase.tsx`) in your project:

   ```typescript
   const config = {
       apiKey: YOUR_API_KEY,
       authDomain: YOUR_AUTH_DOMAIN,
       databaseURL: YOUR_DATABASE_URL,
       projectId: YOUR_PROJECT_ID,
       storageBucket: '',
       messagingSenderId: YOUR_MESSAGING_SENDER_ID,
   };
   ```

   -  Note: Checking all this info into GitHub isn't particularly secure.
     There are ways to store this information in other files (for example, .env files, which are loaded into environment variables); you can then store those files outside of source control

4. Next we'll need to get the config info for our app.

#### How to get your app's database configuration info

1. We'll need to create an 'app' before we can have our code use the database.  There are multiple ways to find this, but we'll start by clicking on the Project Overview link in the top-left:
   <img src="images/Firebase/image-20200725225045730.png" alt="image-20200725225045730"  />

2. Notice that there's an option for iOS and another for Android - we'll use the web application option:
   <img src="images/Firebase/image-20200725225205901.png" alt="image-20200725225205901" style="zoom:67%;" />

3. When Firebase asks make sure that you do give it a name but do NOT host your solution on Firebase

4. Once you've done that it'll show you a Wall of Code.  Copy it and paste it into a new file (just so you don't lose it on the clipboard)

   - If you need this again you can find it in your Project Overview > Project Settings page:
     ![image-20200725225541750](images/Firebase/image-20200725225541750.png)

   - On the 'General' tab (which opens by default) scroll down to the 'Your Apps' section, and you'll find that same info (clicking on the 'Config' button will even give you usable JavaScript/TypeScript):

     <img src="images/Firebase/image-20200725225822787.png" alt="image-20200725225822787" style="zoom:67%;" />

#### Configuring your app to connect to the DB

The approach we're going to use is to create a class that all your components can use

Add a method to that class for each action you want to do on the DB (each time you query for information, or add / update / remove something, etc)



1. Next, plug the configuration info (that you just got from the Firebase web page) into the `myFirebase.tsx` file:
   (Note the <> after createContext!!!)

   ```typescript
   export class Firebase {
       constructor() {
           app.initializeApp(firebaseConfig);
       }
   }
   
   export const FirebaseContext = React.createContext<Firebase | null>(null);
   ```

2. In index.tsx make sure that you import these

   ```typescript
   import { Firebase, FirebaseContext } from './firebase';
   ```

3. Update ReactDOM.render like so:

   ```typescript
   ReactDOM.render(
     <FirebaseContext.Provider value={new Firebase()}>
       <App />
     </FirebaseContext.Provider>,
     document.getElementById('root'),
   );
   ```

4. 

#### get a reference to the place in the JSON doc that you want to modify

#### call set / once / update / remove / push on the ref

#### if you want to know whether it worked or not use Promise.then to run code once it's finished

 (or skip it)

# UNUSED

[Useful tutorial on React Context](https://www.robinwieruch.de/react-context)

[Typescript and React Context](https://www.carlrippon.com/react-context-with-typescript-p1/)

Much of what I've got here was [simplified from this blog post](https://www.robinwieruch.de/complete-firebase-authentication-react-tutorial#react-application-setup-create-react-app) - this post was terrible.  There's too many concepts thrown in and the author is very, very verbose (both in terms of their writing and their code - they routinely have separate files with like a couple lines of actual code)

1. TODO: The listener / promise thing - we're going to try and ignore it :)
2. TODO: Basic API
3. TODO: Do we need to avoid doing the appInit more than once per run?

// The official docs:
// https://firebase.google.com/docs/web/setup?authuser=0#node.js-apps

// Read from / write to DB:
// https://firebase.google.com/docs/database/web/read-and-write?authuser=0



Change #1

Change #2

Change #3

FINISHED