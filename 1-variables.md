# Variables and Statements

JavaScript variables are containers for storing data values. Before ES6, `var` was the only way to create variable declarations.

### <ins>How to create a variable?</ins>

Creating a variable in JavaScript is called "declaring" a variable.

You declare a JavaScript variable with the `var`, `let`, or `const` keyword. (Today, we will focus on `var`.)

Here's an example of declaring a variable:
```JavaScript
    var firstName;
```

After the declaration, the variable has no value (Technically, it has the value of `undefined`).

To <strong>assign</strong> a value to the variable, use the equal sign:
```JavaScript
    var firstName = 'lenora';
```

<ins>The structure of the [Javascript statement](https://www.w3schools.com/js/js_statements.asp) above</ins>:

1. The word `var` lets our computer know what type of variable we're creating (Remember, there are 3 types: `var`, `let`, and `const`)
2. `firstName` lets our computer know the name of the variable
3. `=` lets our computer know we are setting this variable to whatever that follows it
4. `'lenora'` is the string we are setting the variable to
5. The `;` lets our computer know we have ended the statement

### <ins>Var declarations are global scope or function/local scope</ins> 

<strong>Global Scope:</strong> All scripts and functions on a web page can access it. 

<strong>Function/Local scope:</strong> They can only be accessed from within the function.


To understand this further, look at the example below:

```JavaScript
    var beyonce = "Hi, I'm Beyonce!"; // Globally Scoped
    
    function onStage() {
      beyonce = “I am... Sasha Fierce”;
      var jayZ = "I am out of breath!"; // Functionally Scoped
    }
```

Here, the variable `beyonce` has a global scope and it is currently sitting outside the function. The `jayZ` variable has a function scope and it sits inside the function. So, if we do something like this:


```JavaScript
    var beyonce = "Hi, I'm Beyonce!";
    
    function onStage() {
      beyonce = “I am... Sasha Fierce”;
      var jayZ = "I am out of breath!";
    }
    
    console.log(jayZ); // error: jayZ is not defined
    console.log(beyonce); // Hi, I'm Beyonce!
```
We will get an error because `jayZ` is not available outside the function and also Jay Z has no business being out of breath off stage. Keep up Jay Z, geesh! `jayZ` would only be available when the onStage() function is called.

Also, the `beyonce` variable inside the onStage() function can only be accessed inside the function. Outside of the function, `beyonce`'s value is "Hi, I'm Beyonce!". She can't be Sasha Fierce until she's onStage() or until onStage() function is called.

<ins>As you can see within the above variable, var can be <strong>re-declared</strong> and <strong>updated</strong>.</ins>


That means we can do something like this:

```JavaScript
    var beyonce = "Hi, I'm Beyonce Knowles.";
    var beyonce = "Hi, I'm Beyonce Carter.";
```
or:
```JavaScript
    var beyonce = "Hi, I'm Beyonce Knowles.";
    beyonce = "Hi, I'm Beyonce Carter.";
```
For JavaScript, this throws no error. However, for the programmer this can be problematic. We expect beyonce to equal `"Hi, I'm Beyonce Knowles."`, but later in our JavaScript code, we redefined it and JavaScript said nothing! This can lead to unintended side-effects and we should be very careful when using `var` to declare variables.


This is why the <strong>let</strong> and <strong>const</strong> variable is an important addition to our JavaScript arsenal!
