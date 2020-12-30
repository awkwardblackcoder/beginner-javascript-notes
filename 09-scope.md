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

`products` has only been defined in the function scope so we are not allowed to access that variable globally. However, we can access global variables inside the function scope.

```JavaScript
const goodWashAndGo = true;

function badWashAndGo() {
  const products = 'Cantu';
  
  console.log(goodWashAndGo); // true
  console.log(products); // Cantu
}

badWashAndGo();
```

## Var, Let, and Const variables are scoped differently

```JavaScript
if (1 === 1) {
  let greatDay = true;
}

console.log(greatDay); // Uncaught ReferenceError: greatDay is not defined
```


```JavaScript
if (1 === 1) {
  const greatDay = true;
}

console.log(greatDay); // Uncaught ReferenceError: greatDay is not defined
```

```JavaScript
if (1 === 1) {
  var greatDay = true;
}

console.log(greatDay);  // true 
```

`var` variables are not block scope. They are function scope. `let` and `const` is block scope.


## Lexically Scoped
