# Top 50 Popular JavaScript Interview Questions

> Curated from [sudheerj/javascript-interview-questions](https://github.com/sudheerj/javascript-interview-questions)  
> **Level:** Easy to Hard | **Total:** 50 Questions

---

## Table of Contents

### Part 1: Fundamentals (Questions 1-10)
1. [What is the difference between Client-side and Server-side JavaScript?](#1-what-is-the-difference-between-client-side-and-server-side-javascript)
2. [What are the data types in JavaScript?](#2-what-are-the-data-types-in-javascript)
3. [What is the difference between `var`, `let`, and `const`?](#3-what-is-the-difference-between-var-let-and-const)
4. [What is hoisting?](#4-what-is-hoisting)
5. [What is the difference between `null` and `undefined`?](#5-what-is-the-difference-between-null-and-undefined)
6. [What is the difference between `==` and `===`?](#6-what-is-the-difference-between--and-)
7. [What is the `typeof` operator?](#7-what-is-the-typeof-operator)
8. [What is `NaN` and how do you check for it?](#8-what-is-nan-and-how-do-you-check-for-it)
9. [What is a ternary operator?](#9-what-is-a-ternary-operator)
10. [What is the difference between slice and splice?](#10-what-is-the-difference-between-slice-and-splice)

### Part 2: Functions & Scope (Questions 11-20)
11. [What is a closure?](#11-what-is-a-closure)
12. [What are higher-order functions?](#12-what-are-higher-order-functions)
13. [What is Function Composition?](#13-what-is-function-composition)
14. [What is a callback function?](#14-what-is-a-callback-function)
15. [What is Inheritance in JavaScript?](#15-what-is-inheritance-in-javascript)
16. [What is `this` keyword in JavaScript?](#16-what-is-this-keyword-in-javascript)
17. [What are arrow functions and how do they differ from regular functions?](#17-what-are-arrow-functions-and-how-do-they-differ-from-regular-functions)
18. [What is IIFE (Immediately Invoked Function Expression)?](#18-what-is-iife-immediately-invoked-function-expression)
19. [What is Debouncing and Throttling?](#19-what-is-debouncing-and-throttling)
20. [What is the difference between Function Declaration and Function Expression?](#20-what-is-the-difference-between-function-declaration-and-function-expression)

### Part 3: Modern JavaScript & ES6+ (Questions 21-30)
21. [What is destructuring assignment?](#21-what-is-destructuring-assignment)
22. [What is the spread operator?](#22-what-is-the-spread-operator)
23. [What are template literals?](#23-what-are-template-literals)
24. [What are default parameters?](#24-what-are-default-parameters)
25. [What is Scope in JavaScript?](#25-what-is-scope-in-javascript)
26. [What are pure functions?](#26-what-are-pure-functions)
27. [What is an Iterator?](#27-what-is-an-iterator)
28. [What is Immutability?](#28-what-is-immutability)
29. [What are the differences between map, filter, and reduce?](#29-what-are-the-differences-between-map-filter-and-reduce)
30. [What is the difference between push, pop, shift, and unshift?](#30-what-is-the-difference-between-push-pop-shift-and-unshift)

### Part 4: Asynchronous Programming (Questions 31-40)
31. [What is a Promise?](#31-what-is-a-promise)
32. [What is `async/await`?](#32-what-is-asyncawait)
33. [What is the event loop?](#33-what-is-the-event-loop)
34. [What is the difference between synchronous and asynchronous code?](#34-what-is-the-difference-between-synchronous-and-asynchronous-code)
35. [What is a callback function and callback hell?](#35-what-is-a-callback-function-and-callback-hell)
36. [What is the difference between `setTimeout` and `setInterval`?](#36-what-is-the-difference-between-settimeout-and-setinterval)
37. [How do you handle errors in JavaScript?](#37-how-do-you-handle-errors-in-javascript)
38. [What are the Promise methods: `all`, `race`, `allSettled`, and `any`?](#38-what-are-the-promise-methods-all-race-allsettled-and-any)
39. [What are Cookies?](#39-what-are-cookies)
40. [What is RESTful API?](#40-what-is-restful-api)

### Part 5: DOM & Browser APIs (Questions 41-50)
41. [What is event delegation?](#41-what-is-event-delegation)
42. [What is `localStorage` and `sessionStorage`?](#42-what-is-localstorage-and-sessionstorage)
43. [What is JSON and how do you parse/stringify it?](#43-what-is-json-and-how-do-you-parsestringify-it)
44. [What is a Polyfill?](#44-what-is-a-polyfill)
45. [What is a regular expression and how do you use it?](#45-what-is-a-regular-expression-and-how-do-you-use-it)
46. [What is the difference between `innerText`, `innerHTML`, and `textContent`?](#46-what-is-the-difference-between-innertext-innerhtml-and-textcontent)
47. [How do you prevent default behavior of an event?](#47-how-do-you-prevent-default-behavior-of-an-event)
48. [How do you clone an object or array?](#48-how-do-you-clone-an-object-or-array)
49. [What are JavaScript modules?](#49-what-are-javascript-modules)
50. [What is the difference between shallow copy and deep copy?](#50-what-is-the-difference-between-shallow-copy-and-deep-copy)

---

## Questions & Answers

### 1. What is the difference between Client-side and Server-side JavaScript?

**Level:** 🟢 Easy

**Client-side JavaScript:**
- Runs in the browser
- Has access to DOM, window, document objects
- Cannot access backend resources directly
- Executed on user's machine
- Examples: DOM manipulation, event handling, form validation

**Server-side JavaScript:**
- Runs on the server (Node.js)
- No access to browser objects
- Can access databases and file systems
- Handles business logic and data processing
- Examples: API development, database operations, file operations

```javascript
// Client-side - DOM access
document.querySelector("button").addEventListener("click", () => {
  console.log("Button clicked!");
});

// Server-side (Node.js) - File system access
const fs = require("fs");
fs.readFile("file.txt", (err, data) => {
  console.log(data);
});
```

---

### 2. What are the data types in JavaScript?

**Level:** 🟢 Easy

JavaScript has **8 data types** divided into two categories:

**Primitive types (7):**
- `String`, `Number`, `BigInt`, `Boolean`, `undefined`, `null`, `Symbol`

**Non-Primitive (Reference) type (1):**
- `Object` (includes Arrays, Functions, Dates, etc.)

```javascript
typeof "hello"     // "string"
typeof 42          // "number"
typeof true        // "boolean"
typeof undefined   // "undefined"
typeof null        // "object" ← known quirk
typeof {}          // "object"
```

---

### 3. What is the difference between `var`, `let`, and `const`?

**Level:** 🟢 Easy

| Feature | `var` | `let` | `const` |
|---|---|---|---|
| Scope | Function-scoped | Block-scoped | Block-scoped |
| Hoisting | Yes (initialized as `undefined`) | Yes (TDZ) | Yes (TDZ) |
| Re-declaration | Allowed | Not allowed | Not allowed |
| Re-assignment | Allowed | Allowed | Not allowed |

```javascript
var x = 1;
let y = 2;
const z = 3; // z cannot be reassigned
```

---

### 4. What is hoisting?

**Level:** 🟢 Easy

Hoisting is JavaScript's default behavior of moving declarations to the top of their scope before code execution. Only the **declaration** is hoisted, not the initialization.

```javascript
console.log(name); // undefined (hoisted, not initialized)
var name = "Alice";

greet(); // "Hello!" — function declarations are fully hoisted
function greet() {
  console.log("Hello!");
}
```

---

### 5. What is the difference between `null` and `undefined`?

**Level:** 🟢 Easy

| | `null` | `undefined` |
|---|---|---|
| Meaning | Intentional absence of value | Variable declared but not assigned |
| Type | `object` | `undefined` |
| Set by | Developer explicitly | JavaScript engine |

```javascript
let a;
console.log(a); // undefined

let b = null;
console.log(b); // null
```

---

### 6. What is the difference between `==` and `===`?

**Level:** 🟢 Easy

- `==` (loose equality) — compares values after **type coercion**
- `===` (strict equality) — compares both **value and type**, no coercion

```javascript
0 == false   // true  (false coerces to 0)
0 === false  // false (different types)

null == undefined  // true
null === undefined // false
```

---

### 7. What is the `typeof` operator?

**Level:** 🟢 Easy

The `typeof` operator returns a string indicating the type of the unevaluated operand.

```javascript
typeof 42          // "number"
typeof "hello"     // "string"
typeof true        // "boolean"
typeof undefined   // "undefined"
typeof null        // "object"  ← historical bug
typeof {}          // "object"
typeof function(){} // "function"
```

---

### 8. What is `NaN` and how do you check for it?

**Level:** 🟢 Easy

`NaN` (Not a Number) is a special value representing an invalid or unrepresentable number. It is the only value in JavaScript that is **not equal to itself**.

```javascript
typeof NaN // "number" ← it's still of type number!

NaN === NaN  // false

// Correct ways to check for NaN:
isNaN("hello")       // true (coerces string first)
Number.isNaN("hello") // false (no coercion — recommended)
Number.isNaN(NaN)    // true
```

---

### 9. What is a ternary operator?

**Level:** 🟢 Easy

The ternary operator is a shorthand for `if-else` statements. It takes three operands: condition, value if true, and value if false.

```javascript
const age = 20;
const status = age >= 18 ? "Adult" : "Minor"; // "Adult"

// Nested ternary
const score = 85;
const grade = score >= 90 ? "A" : score >= 80 ? "B" : score >= 70 ? "C" : "F";
console.log(grade); // "B"
```

---

### 10. What is the difference between slice and splice?

**Level:** 🟢 Easy

| Method | Mutates | Returns | Use |
|---|---|---|---|
| `slice()` | No | New array | Extract portion |
| `splice()` | Yes | Removed elements | Add/remove elements |

```javascript
const arr = [1, 2, 3, 4, 5];

// slice - doesn't mutate
const sliced = arr.slice(1, 3); // [2, 3]
console.log(arr); // [1, 2, 3, 4, 5] unchanged

// splice - mutates original
const spliced = arr.splice(1, 2, 99); // Removes 2, inserts 99
console.log(arr); // [1, 99, 4, 5]
console.log(spliced); // [2, 3]
```

---

### 11. What is a closure?

**Level:** 🟡 Medium

A closure is a function that has access to its own scope, the outer function's scope, and the global scope — even after the outer function has returned.

```javascript
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}

const counter = outer();
counter(); // 1
counter(); // 2
counter(); // 3
```

---

### 12. What are higher-order functions?

**Level:** 🟡 Medium

A higher-order function is a function that either accepts another function as an argument or returns a function.

```javascript
// Example 1: Accepting a function
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map(n => n * 2); // [2, 4, 6, 8, 10]

// Example 2: Returning a function
function multiplier(factor) {
  return (number) => number * factor;
}
const triple = multiplier(3);
console.log(triple(5)); // 15
```

---

### 13. What is Function Composition?

**Level:** 🟡 Medium

Function composition is combining multiple functions to create a new function. Each function's output becomes the next function's input.

```javascript
// Simple composition
const add = (a, b) => a + b;
const multiply = (x) => x * 2;
const square = (x) => x * x;

// Manual composition
const result = square(multiply(add(2, 3))); // square(multiply(5)) = 100

// Compose utility function
const compose = (...fns) => (x) => fns.reduceRight((acc, fn) => fn(acc), x);

const composed = compose(square, multiply, add);
console.log(composed(2, 3)); // 100

// Pipe (left-to-right composition)
const pipe = (...fns) => (x) => fns.reduce((acc, fn) => fn(acc), x);
const piped = pipe(add, multiply, square);
console.log(piped(2, 3)); // 100
```

**Benefits:** Cleaner code, reusability, easier testing.

---

### 14. What is a callback function?

**Level:** 🟡 Medium

A callback function is a function that is passed as an argument to another function and is executed after some operation has been completed.

```javascript
function greet(name, callback) {
  console.log(`Hello, ${name}!`);
  callback();
}

function sayGoodbye() {
  console.log("Goodbye!");
}

greet("Alice", sayGoodbye);
// Output: Hello, Alice!
//         Goodbye!

// Example with Array.forEach
[1, 2, 3].forEach((num) => {
  console.log(num * 2);
});
// Output: 2, 4, 6
```

---

### 15. What is Inheritance in JavaScript?

**Level:** 🟡 Medium

Inheritance allows objects to acquire properties and methods from other objects. JavaScript uses prototype-based inheritance.

**Prototype-based inheritance:**
```javascript
function Animal(name) {
  this.name = name;
}

Animal.prototype.speak = function() {
  console.log(`${this.name} makes a sound`);
};

function Dog(name) {
  Animal.call(this, name); // Inherit properties
}

Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.bark = function() {
  console.log(`${this.name} barks`);
};

const dog = new Dog("Rex");
dog.speak(); // "Rex makes a sound"
dog.bark();  // "Rex barks"
```

**ES6 class inheritance:**
```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(`${this.name} makes a sound`);
  }
}

class Dog extends Animal {
  bark() {
    console.log(`${this.name} barks`);
  }
}

const dog = new Dog("Rex");
dog.speak(); // "Rex makes a sound"
dog.bark();  // "Rex barks"
```

---

### 16. What is `this` keyword in JavaScript?

**Level:** 🟡 Medium

`this` refers to the object on which a method is invoked. Its value depends on how the function is called.

```javascript
const obj = {
  name: "Alice",
  greet() {
    console.log(this.name); // "Alice"
  }
};

obj.greet(); // Method call: this = obj

function sayName() {
  console.log(this.name);
}
sayName(); // Function call: this = window (or global)

const boundSayName = sayName.bind(obj);
boundSayName(); // "Alice"
```

---

### 17. What are arrow functions and how do they differ from regular functions?

**Level:** 🟡 Medium

Arrow functions (`=>`) are concise and have lexically bound `this`.

| Feature | Regular | Arrow |
|---|---|---|
| Syntax | `function()` | `() =>` |
| `this` binding | Call time | Lexical (parent scope) |
| `arguments` | Available | Not available |
| Constructor | Yes | No |

```javascript
const add = (a, b) => a + b;

// No `this` binding
const obj = {
  name: "Alice",
  greet() {
    setTimeout(() => {
      console.log(this.name); // "Alice" (lexical this)
    }, 100);
  }
};
```

---

### 18. What is IIFE (Immediately Invoked Function Expression)?

**Level:** 🟡 Medium

An IIFE is a function that is defined and executed immediately. It creates its own scope.

```javascript
(function() {
  const secret = "I'm private!";
  console.log(secret);
})();

// Arrow function IIFE
(() => {
  console.log("Arrow IIFE!");
})();

// IIFE with arguments
(function(name) {
  console.log(`Hello, ${name}!`);
})("Alice"); // "Hello, Alice!"
```

---

### 19. What is Debouncing and Throttling?

**Level:** 🟡 Medium

**Debouncing** delays function execution until after a delay since last call. Used for events triggered frequently.

**Throttling** limits function execution to once per specified time interval.

```javascript
// Debouncing - search input
function debounce(fn, delay) {
  let timeout;
  return (...args) => {
    clearTimeout(timeout);
    timeout = setTimeout(() => fn(...args), delay);
  };
}

const searchAPI = debounce((query) => {
  console.log("Searching for:", query);
}, 300);

input.addEventListener("input", (e) => searchAPI(e.target.value));

// Throttling - scroll event
function throttle(fn, limit) {
  let inThrottle;
  return (...args) => {
    if (!inThrottle) {
      fn(...args);
      inThrottle = true;
      setTimeout(() => inThrottle = false, limit);
    }
  };
}

window.addEventListener("scroll", throttle(() => {
  console.log("Scrolling...");
}, 1000));
```

**Differences:**
- Debounce: Waits until user stops (good for search, resize)
- Throttle: Executes at regular intervals (good for scroll, mousemove)

---

### 20. What is the difference between Function Declaration and Function Expression?

**Level:** 🟡 Medium

| | Function Declaration | Function Expression |
|---|---|---|
| Syntax | `function name() {}` | `const name = function() {}` |
| Hoisting | Fully hoisted | Not hoisted |
| When callable | Before declaration | Only after assignment |
| Anonymous | Must have name | Can be anonymous |

```javascript
// Function Declaration - fully hoisted
console.log(add(2, 3)); // 5 (works!)
function add(a, b) {
  return a + b;
}

// Function Expression - not hoisted
console.log(subtract(5, 2)); // TypeError: subtract is not a function
const subtract = function(a, b) {
  return a - b;
};

// Named Function Expression
const multiply = function mul(a, b) {
  return a * b;
};
console.log(multiply(3, 4)); // 12
console.log(mul); // ReferenceError: mul is not defined (name only in scope)

// Arrow Function Expression
const divide = (a, b) => a / b;
console.log(divide(10, 2)); // 5
```

---

### 21. What is destructuring assignment?

**Level:** 🟡 Medium

Destructuring allows extracting values from arrays or properties from objects into distinct variables.

```javascript
// Array destructuring
const [a, b, c] = [1, 2, 3];
const [first, , third] = [1, 2, 3]; // Skip second

// Object destructuring
const { name, age } = { name: "Alice", age: 30 };
const { name: personName } = { name: "Bob" }; // Rename

// Default values
const { role = "User" } = {};
console.log(role); // "User"
```

---

### 22. What is the spread operator?

**Level:** 🟡 Medium

The spread operator (`...`) expands iterable elements where zero or more elements are expected.

```javascript
// Array spreading
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const combined = [...arr1, ...arr2]; // [1, 2, 3, 4, 5, 6]

// Object spreading
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3 };
const merged = { ...obj1, ...obj2 }; // { a: 1, b: 2, c: 3 }

// Function arguments
const numbers = [1, 2, 3];
Math.max(...numbers); // 3
```

---

### 23. What are template literals?

**Level:** 🟢 Easy

Template literals (backticks) allow string interpolation and multi-line strings using `${}` syntax.

```javascript
const name = "Alice";
const age = 30;

// String interpolation
const greeting = `Hello, ${name}! You are ${age} years old.`;
console.log(greeting);

// Multi-line strings
const message = `
  This is a
  multi-line
  string
`;

// Expression evaluation
const result = `2 + 2 = ${2 + 2}`;
console.log(result); // "2 + 2 = 4"
```

---

### 24. What are default parameters?

**Level:** 🟢 Easy

Default parameters allow setting default values for function parameters if no value or `undefined` is passed.

```javascript
function greet(name = "Guest", message = "Welcome") {
  console.log(`${message}, ${name}!`);
}

greet();                    // "Welcome, Guest!"
greet("Alice");             // "Welcome, Alice!"
greet("Bob", "Hello");      // "Hello, Bob!"

// With expressions
function getUserId(id = Math.random()) {
  return id;
}
```

---

### 25. What is Scope in JavaScript?

**Level:** 🟡 Medium

Scope defines where variables are accessible. JavaScript has three types of scope:

**1. Global Scope** - accessible everywhere
```javascript
const global = "I'm global";

function test() {
  console.log(global); // "I'm global"
}

test();
```

**2. Function Scope** - accessible within the function
```javascript
function outer() {
  const functionScoped = "I'm function scoped";
  console.log(functionScoped); // Works
}

console.log(functionScoped); // ReferenceError
```

**3. Block Scope** - accessible within the block (let/const only)
```javascript
if (true) {
  let blockScoped = "I'm block scoped";
  const alsoBlock = "Me too";
  var notBlockScoped = "I leak out";
}

console.log(blockScoped); // ReferenceError
console.log(notBlockScoped); // "I leak out"
```

**Lexical Scope** - inner functions can access outer function's variables
```javascript
function outer(x) {
  function inner(y) {
    console.log(x + y); // Can access x from outer
  }
  inner(5);
}

outer(10); // 15
```

---

### 26. What are pure functions?

**Level:** 🟡 Medium

A pure function always returns the same output for the same input and has no side effects.

```javascript
// Pure function
const add = (a, b) => a + b;

// Impure function - modifies external state
let total = 0;
const addToTotal = (n) => {
  total += n; // Side effect
  return total;
};

// Pure function - no side effects
const multiply = (a, b) => a * b;

// Benefits: easier to test, predictable, enables optimization
```

---

### 27. What is an Iterator?

**Level:** 🟡 Medium

An iterator is an object that implements two methods: `next()` which returns `{value, done}` and optionally `return()`.

```javascript
// Creating an iterator
const createIterator = (array) => {
  let index = 0;
  return {
    next() {
      if (index < array.length) {
        return { value: array[index++], done: false };
      }
      return { done: true };
    }
  };
};

const iterator = createIterator([1, 2, 3]);
console.log(iterator.next()); // { value: 1, done: false }
console.log(iterator.next()); // { value: 2, done: false }
console.log(iterator.next()); // { value: 3, done: false }
console.log(iterator.next()); // { done: true }
```

**Iterable vs Iterator:**
```javascript
// Iterable - has Symbol.iterator method
const iterable = {
  data: [1, 2, 3],
  [Symbol.iterator]() {
    let index = 0;
    return {
      next: () => {
        if (index < this.data.length) {
          return { value: this.data[index++], done: false };
        }
        return { done: true };
      }
    };
  }
};

for (const value of iterable) {
  console.log(value); // 1, 2, 3
}
```

**Built-in iterables:** Arrays, Strings, Maps, Sets, etc.

---

### 28. What is Immutability?

**Level:** 🟡 Medium

Immutability means an object or variable cannot be changed after creation. Immutable data promotes predictable code.

```javascript
// Mutable - state can change
let person = { name: "Alice" };
person.name = "Bob"; // Changed!

// Immutable - create new object instead
const person1 = { name: "Alice" };
const person2 = { ...person1, name: "Bob" }; // New object
console.log(person1.name); // "Alice" (unchanged)
console.log(person2.name); // "Bob"

// Immutable array operations
const arr = [1, 2, 3];
const newArr = [...arr, 4]; // Create new array
const doubled = arr.map(x => x * 2); // Create new array

// Object.freeze() - prevents mutation
const frozen = Object.freeze({ name: "Alice" });
frozen.name = "Bob"; // Silently fails (or error in strict mode)

// Deep immutability
const nested = { user: { name: "Alice" } };
const updated = {
  ...nested,
  user: { ...nested.user, name: "Bob" }
};

// Using structuredClone for deep copy
const deepCopy = structuredClone(nested);
```

**Benefits:**
- Easier debugging and testing
- Thread-safe operations
- Enables optimization
- Predictable state management

---

### 29. What are the differences between map, filter, and reduce?

**Level:** 🟡 Medium

| Method | Purpose | Returns |
|---|---|---|
| `map()` | Transform elements | New array (same length) |
| `filter()` | Select matching elements | New array (possibly shorter) |
| `reduce()` | Combine into single value | Single value |

```javascript
const numbers = [1, 2, 3, 4, 5];

// map - transform
const doubled = numbers.map(n => n * 2); // [2, 4, 6, 8, 10]

// filter - select
const evens = numbers.filter(n => n % 2 === 0); // [2, 4]

// reduce - combine
const sum = numbers.reduce((acc, n) => acc + n, 0); // 15
```

---

### 30. What is the difference between push, pop, shift, and unshift?

**Level:** 🟢 Easy

| Method | Action | Returns | Mutates |
|---|---|---|---|
| `push()` | Add to end | New length | Yes |
| `pop()` | Remove from end | Removed element | Yes |
| `shift()` | Remove from start | Removed element | Yes |
| `unshift()` | Add to start | New length | Yes |

```javascript
const arr = [1, 2, 3];

arr.push(4);      // [1, 2, 3, 4] - returns 4
arr.pop();        // [1, 2, 3] - returns 4
arr.unshift(0);   // [0, 1, 2, 3] - returns 4
arr.shift();      // [1, 2, 3] - returns 0
```

---

### 31. What is a Promise?

**Level:** 🟡 Medium

A Promise represents the eventual completion (or failure) of an asynchronous operation. It has three states: pending, fulfilled, or rejected.

```javascript
const promise = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Success!"), 1000);
});

promise
  .then(result => console.log(result))
  .catch(error => console.error(error))
  .finally(() => console.log("Done"));

// Promise chaining
Promise.resolve(1)
  .then(n => n * 2)
  .then(n => n + 10)
  .then(n => console.log(n)); // 12
```

---

### 32. What is `async/await`?

**Level:** 🟡 Medium

`async/await` is syntactic sugar over Promises that makes asynchronous code look synchronous. An `async` function always returns a Promise.

```javascript
async function fetchData() {
  try {
    const response = await fetch("https://api.example.com/data");
    const data = await response.json();
    return data;
  } catch (error) {
    console.error("Error:", error);
  }
}

fetchData();

// Key: await can only be used inside async functions
```

---

### 33. What is the event loop?

**Level:** 🟡 Medium

The event loop executes code, collects events, and processes queued tasks. It enables asynchronous programming in single-threaded JavaScript.

**Order:**
1. Call stack (synchronous code)
2. Microtask queue (Promises, async/await)
3. Macrotask queue (setTimeout, setInterval)

```javascript
console.log("Start");
setTimeout(() => console.log("setTimeout"), 0);
Promise.resolve().then(() => console.log("Promise"));
console.log("End");

// Output: Start → End → Promise → setTimeout
```

---

### 34. What is the difference between synchronous and asynchronous code?

**Level:** 🟡 Medium

| | Synchronous | Asynchronous |
|---|---|---|
| Execution | Line by line, blocks | Non-blocking |
| Waiting | Waits for completion | Continues immediately |
| Use | Simple operations | I/O, timers, requests |

```javascript
// Synchronous - blocks
const data = readFileSync("file.txt");
console.log(data); // Waits for file read

// Asynchronous - doesn't block
readFile("file.txt", (error, data) => {
  console.log(data); // Executes when ready
});
console.log("Next"); // Executes immediately
```

---

### 35. What is a callback function and callback hell?

**Level:** 🟡 Medium

A callback is a function passed to another function. Callback hell occurs with deeply nested callbacks.

```javascript
// Callback
function loadData(callback) {
  setTimeout(() => callback("Data"), 1000);
}

loadData((data) => console.log(data));

// Callback Hell - pyramid of doom
loadData((data) => {
  processData(data, (result) => {
    saveData(result, (saved) => {
      notifyUser(saved, (notified) => {
        console.log("Done");
      });
    });
  });
});

// Solution: Use Promises or async/await
loadDataAsync()
  .then(processDataAsync)
  .then(saveDataAsync)
  .then(notifyUserAsync)
  .then(() => console.log("Done"));
```

---

### 36. What is the difference between `setTimeout` and `setInterval`?

**Level:** 🟢 Easy

| | `setTimeout` | `setInterval` |
|---|---|---|
| Execution | Once after delay | Repeatedly at interval |
| Cancel | `clearTimeout(id)` | `clearInterval(id)` |

```javascript
// setTimeout - runs once
const t = setTimeout(() => console.log("Once!"), 2000);
clearTimeout(t); // Cancel

// setInterval - runs repeatedly
const i = setInterval(() => console.log("Tick!"), 1000);
clearInterval(i); // Cancel
```

---

### 37. How do you handle errors in JavaScript?

**Level:** 🟡 Medium

Use `try-catch-finally` for synchronous code and `.catch()` for Promises.

```javascript
// Synchronous error handling
try {
  riskyOperation();
} catch (error) {
  console.error("Error:", error.message);
} finally {
  console.log("Cleanup");
}

// Promise error handling
fetchData()
  .then(data => processData(data))
  .catch(error => console.error("Error:", error))
  .finally(() => console.log("Done"));

// Async/await error handling
async function getData() {
  try {
    const response = await fetch("url");
    return await response.json();
  } catch (error) {
    console.error("Error:", error);
  }
}
```

---

### 38. What are the Promise methods: `all`, `race`, `allSettled`, and `any`?

**Level:** 🟡 Medium

| Method | Resolves | Rejects |
|---|---|---|
| `all()` | All resolve | Any rejects |
| `race()` | First settles | First settles |
| `allSettled()` | Always (all settle) | Never |
| `any()` | Any resolves | All reject |

```javascript
const p1 = Promise.resolve(1);
const p2 = Promise.resolve(2);
const p3 = Promise.reject("Error");

Promise.all([p1, p2]) // Waits for all
  .then(console.log); // [1, 2]

Promise.race([p1, p2]) // Returns first
  .then(console.log); // 1

Promise.allSettled([p1, p2, p3])
  .then(console.log); // All results with status

Promise.any([p1, p2])
  .then(console.log); // 1
```

---

### 39. What are Cookies?

**Level:** 🟢 Easy

Cookies are small text files stored on the client's browser that persist across sessions. They're sent with every HTTP request to the server.

```javascript
// Setting a cookie
document.cookie = "name=Alice; path=/; max-age=3600"; // Expires in 1 hour
document.cookie = "theme=dark; expires=" + new Date(Date.now() + 86400000).toUTCString();

// Reading cookies
console.log(document.cookie); // "name=Alice; theme=dark"

// Parsing cookies
function getCookie(name) {
  const nameEQ = name + "=";
  const cookies = document.cookie.split(';');
  for (let cookie of cookies) {
    cookie = cookie.trim();
    if (cookie.indexOf(nameEQ) === 0) {
      return cookie.substring(nameEQ.length);
    }
  }
  return null;
}

const userName = getCookie("name"); // "Alice"

// Deleting a cookie
document.cookie = "name=; max-age=0"; // Set expiry to past
```

**Differences from localStorage/sessionStorage:**

| | Cookies | localStorage | sessionStorage |
|---|---|---|---|
| Size | ~4KB | ~10MB | ~10MB |
| Sent with requests | Yes | No | No |
| Server access | Yes | No | No |
| Expiry | Set by server | Manual delete | Tab close |

**Security considerations:**
- Use `Secure` flag for HTTPS only
- Use `HttpOnly` flag to prevent JS access
- Be cautious with sensitive data

```javascript
// Secure cookie (HTTPS only, no JS access)
document.cookie = "auth=token123; Secure; HttpOnly; path=/";
```

---

### 40. What is RESTful API?

**Level:** 🟡 Medium

REST (Representational State Transfer) is an architectural style using HTTP methods on resources.

```javascript
// GET - Retrieve data
fetch("https://api.example.com/users")
  .then(response => response.json())
  .then(data => console.log(data));

// POST - Create data
fetch("https://api.example.com/users", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ name: "Alice", age: 30 })
})
  .then(response => response.json());

// PUT - Update data
fetch("https://api.example.com/users/1", {
  method: "PUT",
  body: JSON.stringify({ name: "Bob" })
});

// DELETE - Delete data
fetch("https://api.example.com/users/1", {
  method: "DELETE"
});
```

---

### 41. What is event delegation?

**Level:** 🟡 Medium

Event delegation attaches a single listener to a parent element instead of multiple listeners on children.

```javascript
// Without delegation - inefficient
document.querySelectorAll("li").forEach(li => {
  li.addEventListener("click", handleClick);
});

// With delegation - efficient
document.querySelector("ul").addEventListener("click", (e) => {
  if (e.target.tagName === "LI") {
    console.log("Clicked:", e.target.textContent);
  }
});

// Benefits: fewer listeners, works with dynamic elements
```

---

### 42. What is `localStorage` and `sessionStorage`?

**Level:** 🟢 Easy

Both store client-side data but differ in scope and duration:

| | `localStorage` | `sessionStorage` |
|---|---|---|
| Duration | Until manually deleted | Until tab closes |
| Scope | Entire domain | Single tab |
| Size | ~10MB | ~10MB |

```javascript
// localStorage
localStorage.setItem("name", "Alice");
const name = localStorage.getItem("name"); // "Alice"
localStorage.removeItem("name");
localStorage.clear();

// sessionStorage
sessionStorage.setItem("tempData", "value");
const data = sessionStorage.getItem("tempData");
```

---

### 43. What is JSON and how do you parse/stringify it?

**Level:** 🟢 Easy

JSON (JavaScript Object Notation) is a lightweight data format for data exchange.

```javascript
// Object to JSON string
const obj = { name: "Alice", age: 30 };
const jsonString = JSON.stringify(obj);
console.log(jsonString); // '{"name":"Alice","age":30}'

// JSON string to Object
const jsonStr = '{"name":"Bob","age":25}';
const parsed = JSON.parse(jsonStr);
console.log(parsed.name); // "Bob"

// With formatting
const formatted = JSON.stringify(obj, null, 2);
console.log(formatted);
/* 
{
  "name": "Alice",
  "age": 30
}
*/

// Custom replacer
const filtered = JSON.stringify(obj, ['name']);
console.log(filtered); // '{"name":"Alice"}'
```

---

### 44. What is a Polyfill?

**Level:** 🟡 Medium

A polyfill is code that provides functionality for older browsers that don't have native support for modern JavaScript features.

```javascript
// Example 1: Polyfill for Array.includes() (ES6)
if (!Array.prototype.includes) {
  Array.prototype.includes = function(searchElement) {
    return this.indexOf(searchElement) !== -1;
  };
}

// Now works in older browsers
[1, 2, 3].includes(2); // true

// Example 2: Polyfill for String.startsWith() (ES6)
if (!String.prototype.startsWith) {
  String.prototype.startsWith = function(search, pos) {
    return this.substr(!pos || pos < 0 ? 0 : +pos, search.length) === search;
  };
}

"hello".startsWith("he"); // true

// Example 3: Polyfill for Promise (ES6)
if (typeof Promise === "undefined") {
  window.Promise = function(executor) {
    // Simple Promise implementation
  };
}

// Example 4: Polyfill for fetch API
if (!window.fetch) {
  window.fetch = function(url, options) {
    return new Promise((resolve, reject) => {
      const xhr = new XMLHttpRequest();
      xhr.open((options && options.method) || "GET", url);
      xhr.onload = () => resolve(xhr.responseText);
      xhr.onerror = () => reject(xhr.statusText);
      xhr.send();
    });
  };
}
```

**Popular polyfill libraries:**
- **Babel** - Transpiles modern JavaScript to ES5
- **core-js** - Large collection of polyfills
- **polyfill.io** - Service that delivers polyfills

**When to use:**
- Support older browsers
- Use modern features without compilation
- Gradual enhancement

---

### 45. What is a regular expression and how do you use it?

**Level:** 🟡 Medium

Regular expressions (regex) are patterns for matching and manipulating strings.

```javascript
// Creating regex
const pattern = /hello/i; // i = case-insensitive
const pattern2 = new RegExp("hello", "i");

// Testing pattern
console.log(/test/.test("This is a test")); // true

// Finding matches
const str = "apple, apricot, avocado";
console.log(str.match(/a\w+/g)); // ["apple", "apricot", "avocado"]

// Replacing
const result = str.replace(/a/, "A");
console.log(result); // "Apple, apricot, avocado"

// Common patterns
/\d+/        // One or more digits
/[a-z]+/     // One or more letters
/\w+/        // Word characters
/\s+/        // Whitespace
/^start/     // Starts with
/end$/       // Ends with
/a|b|c/      // OR operator
```

---

### 46. What is the difference between `innerText`, `innerHTML`, and `textContent`?

**Level:** 🟢 Easy

| Property | Returns | Includes HTML | Visible Only |
|---|---|---|---|
| `textContent` | Text content | No | No |
| `innerText` | Rendered text | No | Yes |
| `innerHTML` | Full HTML | Yes | N/A |

```javascript
const div = document.querySelector("div");
div.innerHTML = "<p>Hello <strong>World</strong></p>";

console.log(div.textContent);  // "Hello World"
console.log(div.innerText);    // "Hello World"
console.log(div.innerHTML);    // "<p>Hello <strong>World</strong></p>"

// Setting values
div.textContent = "Safe text";    // Safe, no HTML parsing
div.innerHTML = "<p>HTML</p>";    // Parses HTML, potential XSS
```

---

### 47. How do you prevent default behavior of an event?

**Level:** 🟢 Easy

Use `preventDefault()` to stop the default event action.

```javascript
// Prevent form submission
const form = document.querySelector("form");
form.addEventListener("submit", (e) => {
  e.preventDefault();
  console.log("Form submission prevented");
});

// Prevent link navigation
const link = document.querySelector("a");
link.addEventListener("click", (e) => {
  e.preventDefault();
  console.log("Link navigation prevented");
});

// Stop event propagation
element.addEventListener("click", (e) => {
  e.stopPropagation(); // Prevents bubbling
});

element.addEventListener("click", (e) => {
  e.stopImmediatePropagation(); // Prevents all listeners
});
```

---

### 48. How do you clone an object or array?

**Level:** 🟡 Medium

Clone objects or arrays using spread operator, Object.assign(), or structuredClone().

```javascript
// Shallow copy - spread operator
const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1 }; // Shallow copy

const arr1 = [1, 2, 3];
const arr2 = [...arr1]; // Shallow copy

// Shallow copy - Object.assign()
const obj3 = Object.assign({}, obj1);
const arr3 = Array.from(arr1);

// Shallow copy - concat/slice
const arr4 = arr1.concat();
const arr5 = arr1.slice();

// Deep copy - structuredClone()
const deepCopy = structuredClone(obj1);

// Deep copy - JSON (limitations: no functions, Date, etc)
const deepCopy2 = JSON.parse(JSON.stringify(obj1));

// Problem with shallow copy
const nested = { a: { b: 1 } };
const shallow = { ...nested };
shallow.a.b = 2;
console.log(nested.a.b); // 2 (shared reference!)
```

---

### 49. What are JavaScript modules?

**Level:** 🟡 Medium

Modules allow organizing code into reusable files. Use `import`/`export` for ES6 modules.

```javascript
// Exporting - math.js
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;
export default function multiply(a, b) {
  return a * b;
}

// Importing
import multiply, { add, subtract } from "./math.js";

console.log(add(2, 3));      // 5
console.log(subtract(5, 2)); // 3
console.log(multiply(4, 5)); // 20

// CommonJS (Node.js)
// Exporting
module.exports = { add, subtract };
module.exports.multiply = multiply;

// Importing
const { add, subtract } = require("./math.js");
const multiply = require("./math.js").multiply;
```

---

### 50. What is the difference between shallow copy and deep copy?

**Level:** 🟡 Medium

| | Shallow Copy | Deep Copy |
|---|---|---|
| Top level | Copied | Copied |
| Nested objects | Shared reference | Copied |
| Performance | Fast | Slower |
| Use case | Simple objects | Complex nested data |

```javascript
const original = {
  name: "Alice",
  address: { city: "NYC", zip: "10001" }
};

// Shallow copy
const shallow = { ...original };
shallow.address.city = "Boston"; // Affects original!
console.log(original.address.city); // "Boston"

// Deep copy - structuredClone()
const deep = structuredClone(original);
deep.address.city = "LA"; // Doesn't affect original
console.log(original.address.city); // "Boston"

// Deep copy - recursive function
function deepClone(obj) {
  if (obj === null || typeof obj !== "object") return obj;
  if (Array.isArray(obj)) return obj.map(deepClone);
  
  const clone = {};
  for (const key in obj) {
    clone[key] = deepClone(obj[key]);
  }
  return clone;
}
```

---

## Quick Reference Summary

| # | Question | Level |
|---|---|---|
| 1 | Client-side vs Server-side JS | 🟢 Easy |
| 2 | Data types | 🟢 Easy |
| 3 | `var` vs `let` vs `const` | 🟢 Easy |
| 4 | Hoisting | 🟢 Easy |
| 5 | `null` vs `undefined` | 🟢 Easy |
| 6 | `==` vs `===` | 🟢 Easy |
| 7 | `typeof` operator | 🟢 Easy |
| 8 | `NaN` checking | 🟢 Easy |
| 9 | Ternary operator | 🟢 Easy |
| 10 | `slice` vs `splice` | 🟢 Easy |
| 11 | Closures | 🟡 Medium |
| 12 | Higher-order functions | 🟡 Medium |
| 13 | Function Composition | 🟡 Medium |
| 14 | Callback functions | 🟡 Medium |
| 15 | Inheritance in JavaScript | 🟡 Medium |
| 16 | `this` keyword | 🟡 Medium |
| 17 | Arrow functions | 🟡 Medium |
| 18 | IIFE | 🟡 Medium |
| 19 | Debouncing and Throttling | 🟡 Medium |
| 20 | Function Declaration vs Expression | 🟡 Medium |
| 21 | Destructuring | 🟡 Medium |
| 22 | Spread operator | 🟡 Medium |
| 23 | Template literals | 🟢 Easy |
| 24 | Default parameters | 🟢 Easy |
| 25 | Scope in JavaScript | 🟡 Medium |
| 26 | Pure functions | 🟡 Medium |
| 27 | Iterator | 🟡 Medium |
| 28 | Immutability | 🟡 Medium |
| 29 | `map` vs `filter` vs `reduce` | 🟡 Medium |
| 30 | Array methods | 🟢 Easy |
| 31 | Promises | 🟡 Medium |
| 32 | `async/await` | 🟡 Medium |
| 33 | Event loop | 🟡 Medium |
| 34 | Synchronous vs asynchronous | 🟡 Medium |
| 35 | Callback hell | 🟡 Medium |
| 36 | `setTimeout` vs `setInterval` | 🟢 Easy |
| 37 | Error handling | 🟡 Medium |
| 38 | Promise methods | 🟡 Medium |
| 39 | Cookies | 🟢 Easy |
| 40 | RESTful API | 🟡 Medium |
| 41 | Event delegation | 🟡 Medium |
| 42 | `localStorage` vs `sessionStorage` | 🟢 Easy |
| 43 | JSON parsing/stringify | 🟢 Easy |
| 44 | Polyfill | 🟡 Medium |
| 45 | Regular expressions | 🟡 Medium |
| 46 | `innerText` vs `innerHTML` vs `textContent` | 🟢 Easy |
| 47 | Prevent default behavior | 🟢 Easy |
| 48 | Cloning objects/arrays | 🟡 Medium |
| 49 | JavaScript modules | 🟡 Medium |
| 50 | Shallow vs deep copy | 🟡 Medium |

---

**Source:** [sudheerj/javascript-interview-questions](https://github.com/sudheerj/javascript-interview-questions)

**Difficulty Distribution:**
- 🟢 **Easy:** 18 questions
- 🟡 **Medium:** 32 questions

These 50 questions represent the most popular and essential JavaScript concepts for technical interviews. Mastering them will provide comprehensive coverage of core JavaScript fundamentals!
