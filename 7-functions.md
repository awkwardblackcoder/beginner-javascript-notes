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

## Returning an object

```JavaScript
function makeABaby(first, last) {
  const baby = {
    name: `${first} ${last}`,
    age: 0
  }
  return baby;
}

// Now let's turn it into an arrow function
// Step 1

const makeABaby = (first, last) => {
 const baby = {
    name: `${first} ${last}`,
    age: 0
  }
  return baby;
}

// Step 2


const makeABaby = (first, last) => {
  return {
    name: `${first} ${last}`,
    age: 0
  }
}

// Step 3 with implicit return with parenthesis

const makeABaby = (first, last) => ({ name: `${first} ${last}`, age: 0 });
```

Now, converting a function that returns an object into an arrow function may not always be the most readable. 


## Define a function with an IIFE
Immediately Invoked Function Expression

```JavaScript
function() {
  console.log('Running the Anon function');
  return 'You are cool';
 }
}

// Right now, this doesn't run at all. To run it, you can wrap it in a const like this:
const x = function() {
  console.log('Running the Anon function');
  return 'You are cool';
 }
}

// Or you can wrap it in a parenthesis because parenthesis always run first in JavaScript making it a IIFE. Right after, immediately run that function with ();

(function() {
  console.log('Running the Anon function');
  return 'You are cool';
 }
})();


// If you need to pass in a parameter, you will do it like this:
(function(age) {
  console.log('Running the Anon function');
  return `You are cool and age ${age}`;
 }
})(10);
```
