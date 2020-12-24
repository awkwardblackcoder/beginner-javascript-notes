In 2015, ECMAScript 6 introduced the let and const variable. `let` is a JavaScript variable that is very similar to `var`; however, it gives you the luxury of declaring variables in a limited scope. 

Like `var`, a variable declared with `let` can be <strong>updated</strong> within the same scope; however, unlike `var`, let cannot be <strong>redeclared</strong> within the same scope. Here's an example of updating versus redeclaring.

```JavaScript
let ciara = "My husband is Russell Wilson.";
let ciara = "I'm in love with Future."

console.log(ciara); //Uncaught SyntaxError: Identifier 'ciara' has already been declared
```

However, if you change `let` to `var`, `var` variables will let you redeclare your variables within the same scope.

```JavaScript
var ciara = "My husband is Russell Wilson.";
var ciara = "I'm in love with Future." 

console.log(ciara); //I'm in love with Future.
```
Potential bugs can ensue if the developer isn't aware that they've redeclared a variable or used `ciara` as a variable name earlier in their code. `let` allows the developer to get a nifty Syntax Error and clearly states the potential risk before it happens.

When using `let`, the syntax error lets us know `ciara` was already defined! We can’t redefine `ciara` within that same scope…. she is a changed woman!


However, you can <strong>update</strong> the same variable in different scopes and there will be no error.

``` JavaScript

let ciara = "My husband is Russell Wilson.";
let currentYear = 2019;

if (currentYear <= 2015 && currentYear >= 2013) {
  let ciara = "I'm in love with Future."
  console.log(ciara);
}
console.log(ciara);
```

In 2013-2015, Ciara was ALL about Future but in `currentYear` 2019, her husband is Russell Wilson. Ciara is only in love with future within the scope of 2013-2015.
