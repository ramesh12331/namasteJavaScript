Shortest JS Program, Global Object & this Keyword
📌 Overview

Even an empty JavaScript file does a lot behind the scenes. The JS engine automatically sets up:

Global Execution Context (GEC) – Memory allocation and execution environment.

Global Object – In browsers, this is window; in Node.js, it’s global.

this keyword – At the global level, this points to the global object.

📌 Key Points

Global Object contains many built-in functions and variables accessible anywhere.

Global Variables declared using var are attached to the global object.
```js
var x = 10;

console.log(x);         // 10
console.log(this.x);    // 10
console.log(window.x);  // 10
```

At the global level:

this === window // true (in browser)


In Node.js, the global object is global instead of window.
📌 Summary

| Concept             | Explanation                                                                       |
| ------------------- | --------------------------------------------------------------------------------- |
| Shortest JS program | Can be an empty file. JS engine creates GEC, global object, and `this`.           |
| Global Object       | Holds all global variables and functions. Browser → `window`, Node.js → `global`. |
| `this` keyword      | Refers to the global object in the global scope.                                  |
| Global Variables    | Declared with `var` and automatically attached to the global object.              |

📌 Interview Q&A

Q1: What is the shortest JS program?
A: An empty file. Even then, JS engine creates GEC, global object, and this.

Q2: What is the global object in JavaScript?
A: A built-in object that holds global variables and functions. window in browsers, global in Node.js.

Q3: What does this refer to at the global level?
A: It points to the global object (window in browsers).

Q4: Are global variables attached to the global object?
A: Yes, variables declared using var in the global scope become properties of the global object.

Q5: Does let or const attach variables to the global object?
A: No, only var attaches variables to the global object at the global scope.

