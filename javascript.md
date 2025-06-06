# JAVASCRIPT-INTERVIEW_QUESTION

## What is JavaScript, and how is it different from Java?

**Answer:**  
JavaScript is a lightweight, interpreted programming language primarily used for web development to create interactive web pages. It differs from Java in syntax, use cases, and its execution environment. JavaScript runs in the browser, while Java is typically compiled and runs on the JVM.

---

## What are the data types in JavaScript?

**Answer:**

**Primitive Types:**  
String, Number, BigInt, Boolean, Symbol, Undefined, Null.

**Non-Primitive Types:**  
Object (includes Arrays, Functions, etc.).

---

## What is the difference between `==` and `===`?

**Answer:**

- `==` performs type coercion before comparison.  
- `===` checks both value and type, without coercion.

**Example:**

```javascript
5 == '5';  // true
5 === '5'; // false

```


## What is the difference between let, const, and var?

Answer:

var: Function-scoped, can be re-declared and updated.

let: Block-scoped, cannot be re-declared but can be updated.

const: Block-scoped, cannot be re-declared or updated

## What are template literals?

Answer: Template literals are string literals allowing embedded expressions using backticks (`). Example:

```
const name = "Alice";
console.log(`Hello, ${name}!`); // Hello, Alice!

```

---

## What is the difference between undefined and null?

Answer:

undefined: A variable is declared but not assigned a value.

null: Represents an intentional absence of value.

## Explain scope and its types in JavaScript.

Answer:

Global Scope: Accessible throughout the code.

Function Scope: Accessible only within the function.

Block Scope: Accessible only within the block (let, const).


---


What is a closure?

Answer: A closure is a function that retains access to its lexical scope, even after the outer function has finished execution.

Example:

```
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
```
---


### Intermediate JavaScript Questions
## What are Arrow Functions?

Answer: A concise syntax for writing functions. They do not have their own this and are not suitable for methods.

```
const add = (a, b) => a + b;
console.log(add(2, 3)); // 5
```

## What are Promises, and how do they work?

Answer: Promises are used for asynchronous operations, representing a value that may be available now, in the future, or never.

```
const promise = new Promise((resolve, reject) => {
  if (true) resolve('Success');
  else reject('Error');
});
```

## What is the this keyword in JavaScript?

Answer: this refers to the object that is currently executing the function. It varies based on the context.

## What is the difference between call, apply, and bind?

Answer:
```
call: Invokes a function with a specified this and arguments.

apply: Similar to call, but arguments are passed as an array.

bind: Returns a new function with this bound to the specified object.
```

## What is the event loop?

Answer: The event loop handles asynchronous code execution by continuously checking the call stack and the message queue to execute functions.

Explain async and await.

Answer: They simplify Promises, allowing asynchronous code to be written like synchronous code.
```
async function fetchData() {
  const data = await fetch('https://api.example.com');
  console.log(data);
}
```
## What is destructuring in JavaScript?

Answer: A syntax to unpack values from arrays or properties from objects.

```
const [a, b] = [1, 2];
const { name, age } = { name: 'Alice', age: 25 };
```


---

### Advanced JavaScript Questions
## What is the difference between deep copy and shallow copy?

Answer:

Shallow Copy: Copies only the first level.

Deep Copy: Recursively copies all levels.

## What are Higher-Order Functions?

Answer: Functions that take other functions as arguments or return them.

## What are modules in JavaScript?

Answer: ES6 modules allow code to be split into reusable pieces. export and import are used for sharing code.

## What is the purpose of Object.freeze() and Object.seal()?

Answer:

```
Object.freeze(): Prevents adding, removing, or modifying properties.

Object.seal(): Prevents adding or removing but allows modification of existing properties.
```

## What is Currying?

Answer: Breaking a function with multiple arguments into a series of functions taking one argument each.


```
const multiply = a => b => a * b;
console.log(multiply(2)(3)); // 6
```

## What is Debouncing?

Answer: Ensures a function is executed only after a certain period of inactivity.

```
function debounce(func, delay) {
  let timeout;
  return (...args) => {
    clearTimeout(timeout);
    timeout = setTimeout(() => func(...args), delay);
  };
}
```


## What is Hoisting?

Answer: JavaScript's default behavior of moving declarations to the top of the scope.

## What are Prototypes?

Answer: Prototypes are the mechanism by which JavaScript objects inherit features from one another.

## What is the difference between setTimeout and setInterval?

Answer:

setTimeout: Executes a function once after a delay.

setInterval: Executes a function repeatedly at regular intervals.

## What is the spread operator?

Answer: Expands arrays or objects into individual elements or properties.


``` 
const arr = [1, 2, 3];
console.log([...arr, 4]); // [1, 2, 3, 4]
```

### Scenario-Based/Practical Questions

## How do you remove duplicates from an array?

Answer:
```
const uniqueArray = [...new Set([1, 2, 2, 3])];

```

## How to check if a number is an integer?

Answer:

```
Number.isInteger(5); // true
```
## Explain how you can handle errors in JavaScript.

Answer: Using try-catch blocks:

```
try {
  throw new Error('Error occurred');
} catch (e) {
  console.log(e.message);
}
```

## What are IIFEs (Immediately Invoked Function Expressions)?

Answer: Functions executed immediately after declaration.

```
(function() {
  console.log('IIFE');
})();
```
## How can you optimize performance in JavaScript applications?

Answer:

Minimize DOM manipulations.

Use requestAnimationFrame for animations.

Use throttling and debouncing for event handling.

Use lazy loading for images.

---
