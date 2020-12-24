In 2015, ECMAScript 6 introduced the let and const variable. `let` is a JavaScript variable that is very similar to `var`; however, it gives you the luxury of declaring variables in a limited scope. 

Like `var`, a variable declared with `let` can be updated within its scope; however, unlike `var`, let cannot be redeclared within the same scope.

```JavaScript
let ciara = "My husband is Russell Wilson.";
let ciara = "I'm in love with Future." //Uncaught SyntaxError: Identifier 'ciara' has already been declared
```

With this particular scope, ciara was already defined! We can’t redefine ciara within that same scope…. she is a changed woman!


However, you can <strong>declare</strong> the same variable in different scopes and there will be no error.

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
