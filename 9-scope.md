# Scope

In JavaScript there are two types of scope:

- Local scope
- Global scope

JavaScript has function scope: Each function creates a new scope.

Scope determines the accessibility (visibility) of these variables.

Variables defined inside a function are not accessible (visible) from outside the function.

## Local Variables

Variables declared within a JavaScript function, become LOCAL to the function.

Local variables have Function scope: They can only be accessed from within the function.

## Global Variables

A variable declared outside a function, becomes GLOBAL.

A global variable has global scope: All scripts and functions on a web page can access it.


## Function Scope

```JavaScript
const goodWashAndGo = true;

function badWashAndGo() {
  const products = 'Cantu';
}

console.log(goodWashAndGo); // true
console.log(products); // Uncaught ReferenceError: products is not defined


```
