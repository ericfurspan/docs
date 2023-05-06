
**JavaScript is synchronous & single-threaded**

- Single threaded: one command at a time.
- Synchronous: everything is paused until the wait is over (the command has returned).
- Said another way, if some JavaScript code is being executed, then no other JavaScript can be executed at the same time. Commands are processed one at a time in a single thread.

**JavaScript is a dynamically typed language**

- Data types (string, integer, Boolean, etc) are not defined explicitly but rather they are determined at runtime. This is as opposed to a statically typed language, where the data type must be explicitly defined when the data structure/variable is first declared.

**JavaScript implements a Prototype chain via Inheritance**

- Every data structure within JavaScript has a prototype from which it inherits properties and methods. If a property or method is not found on the source object itself, it will look upwards to its prototype for that property. And that upward check goes on until it either finds the desired property/method or has reached the base prototype. This process is called the prototype chain. All data structures (by default) inherit from the base prototype which in javascript is Object.
- [Learn more](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes#a_prototype-based_language)

**Promises (working with asynchronous behavior)**

- A "Promise" is a proxy for a value not known immediately but which will eventually be resolved (fulfilled or rejected) into a value. It allows you to write asynchronous/non-blocking code for expensive operations like I/O and HTTP requests.
- In javascript we use promises when working with values that cannot be immediately read. For example, making an HTTP request takes a certain amount of time, therefore a promise is often immediately typically returned in lieu of the value, which allows for a consistent pattern for waiting for that value to "resolve" on the frontend. For more, read about async/await in javascript and its advantages over callbacks.
- The three possible states of a promise are: Pending, Fulfilled, Rejected.
- [Learn more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

**CORS (cross origin resource sharing)**

- The same-origin policy prevents JavaScript from making requests across domain boundaries.
- This prevents malicious scripts on one page from obtaining access to data on another page through the DOM.
- [Learn more](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)

**Event Loop**

- The event loop is a single-threaded loop that monitors the call stack and checks if there is any work to be done in the task queue. If the call stack is empty and there are callback functions in the task queue, a function is dequeued and pushed onto the call stack to be executed.
- [Learn more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)

**First-class functions**

- Functions that take other functions as arguments or return functions as their results.
- Meant to abstract some operation that is performed repeatedly.
- [Learn more](https://developer.mozilla.org/en-US/docs/Glossary/First-class_Function)

**Closure**

- A mechanism for containing state. A closure is created anytime a function accesses a variable defined outside its immediate scope.
- Usefulness: Data privacy
- [Learn more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)

**Event Delegation**

- A technique involving adding event listeners to a parent element instead of adding them to the descendant elements. The listener will fire whenever the event is triggered on the descendant elements due to event bubbling up the DOM.
- Beneficial if we have several elements handled in a similar way, instead of assigning a handler to each one, we can assign ONE handler to their parent.
- [Learn more](https://davidwalsh.name/event-delegate)

**Scoping**

- Scoping is javascripts way of controlling accessibility to variables within code. It is an important feature to understand because proper implementation of scope will prevent unwanted cases of variables clashing with each other. The two types of scope are global and local.
- Global scope refers to variables that are defined at the top level of a javascript file - i.e not within any function or object. Local scope refers to the variables defined within a specific function block. These variables are bound to the function itself and are not accessible from another scope. This allows for multiple functions to have the same variable names and for them not to clash.
    - Global scope should be avoided because global variables can be accessed and/or modified from any location within your code - be it other functions or another point in the global scope, and this can often lead to negative unwanted side effects.
- [Learn more](https://developer.mozilla.org/en-US/docs/Glossary/Scope)

**What are side effects, and what is a pure function?**

- **Side effects** are when a function moves up the scope chain (outside its own execution context) to look for or make changes to variables outside its own local scope.
- A **pure function** is one which does not alter or depend on variables outside its own local scope. Pure functions ALWAYS return the same result when given the same parameters

**The 'this' keyword**

- In Arrow functions, the 'this' reference is bound to the enclosing scope which is different compared to regular functions where the this is determined by the object calling it
- Can use call(), apply(), or bind() to change what 'this' refers to

**Type Coercion**

- The act of changing a value to another data type

**Statements vs Expressions**

- Statement: does something, i.e assignment, logging
- Expression: A unit of code that results in a value

**Variable declaration (Let vs Const)**

- Const: A constant variable which is block scoped and cannot be reassigned or redeclared
- Let: A variable which is block scoped and cannot be redeclared but CAN be reassigned

**Strict Mode**

- Strict mode is a feature of javascript that forces you to write cleaner code by throwing errors/warnings when using global variables or doing other non-recommended things. Strict mode is enabled by typing 'use strict' at the top of the js file OR at the top of a function. It is best to use strict mode by default and only remove it if you are consciously making the choice of using global variables.

### References & Further Reading

- [https://github.com/tomquinonero/JSTheWeirdParts](https://github.com/tomquinonero/JSTheWeirdParts)
- [https://developer.mozilla.org/en-US/docs/Web/JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [https://github.com/airbnb/javascript#airbnb-javascript-style-guide-](https://github.com/airbnb/javascript#airbnb-javascript-style-guide-)
- [https://www.youtube.com/watch?v=Tn6-PIqc4UM](https://www.youtube.com/watch?v=Tn6-PIqc4UM)
