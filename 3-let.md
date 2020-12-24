In 2015, ECMAScript 6 introduced the let and const variable. `let` is a JavaScript variable that is very similar to `var`; however, it gives you the luxury of declaring variables in a limited scope. The `let` variable is blocked scoped. A block is code bounded by curly braces {} (Examples of code blocks: If statements, loops, functions, etc.). If the `let` variable is declared within those curly braces, it is only available within that block (unlike `var`). 

Let compare `var` and `let` using Ciara’s hit song Level Up.

```JavaScript
let sayLevelUp = "Level Up! ";
let times = 5;

if (times >= 1) {
  let lyrics = sayLevelUp.repeat(times);
  console.log(lyrics); // Level Up! Level Up! Level Up! Level Up! Level Up! 
}

console.log(lyrics); // Uncaught ReferenceError: lyrics is not defined
```

Inside the code block (if statement), we are able to access the variable lyrics, but outside of the code block, we are told lyrics isn’t defined. This illustrates the point that `let` allows you to declare variables in a limited scope (block scope) instead of globally or within a function like `var`. This allows `let` to be updated but never re-declared.

(Homework: Change all the `let` variables to `var`, compare the console.log statements and tell me the difference between `let` and `var` in this example.)


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
