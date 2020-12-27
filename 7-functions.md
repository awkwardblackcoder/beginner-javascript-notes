# Functions
A JavaScript function is a block of code designed to perform a particular task.

## [<ins>Built-In Functions</ins>](https://www.tutorialspoint.com/javascript/javascript_builtin_functions.htm)
```JavaScript
console.log()
parseFloat()
parseInt()
Date.now()
querySelector()
navigator.vibrate()
scrollTo()
```

## Writing custom functions

Functions are created or defined then later called.

A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().

Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).

The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: {}

```JavaScript

// This is a function definition
function bombAssWashAndGo(param1) { // The open curly bracket starts the function block
// Inside here is the function body
}

// Function Call
bombAssWashAndGo();
```

Realistic Example:

```JavaScript
function calculateBill(billAmount, taxRate) {
  const total = billAmount * ( 1 + taxRate );
  return total
}

const myTotal = calculateBill(350, 0.15); 
console.log(myTotal) // $402.49999999999994
```

## Different Ways to Declare Functions

```JavaScript
// With the function keyword
// Hoisted function -> Pulls things to the top
function bombAssWashAndGo(param1) {
  return 'Congratulations on your amazing wash and go!'
};

// Anonymous Functions
function (param1) {
  return 'Congratulations on your amazing wash and go!'
};

// Function Expression
const washAndGo = function(param1) {
  return 'Congratulations on your amazing wash and go!'
};


//Another Example

// Anonymous function
const inchToCM = function(inches) {
  return inches * 2.54;
}

// Regular Function
function inchToCM(inches) {
  const cm = inches * 2.54;
  return cm;
}

// Arrow Function
// Way 1 with Explicit Return
const inchToCM = (inches) => {
  return inches * 2.54;
};

// Way 2 with Implicit Return
const inchToCM = (inches) => inches * 2.54;

// One last conversion 

function add(a, b = 3) {
  const total = a + b;
  return total;
}

const add = (a, b = 3) => a + b;

```
