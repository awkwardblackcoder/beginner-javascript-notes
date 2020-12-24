# Variables and Statements


    var first; 



    var first = 'lenora';
    

Before ES6, `var` was the way to create variable declarations. Scope:  `var` declarations are globally scoped or function/locally scoped. It is globally scoped when `var` is declared outside a function; however, if `var` is declared within a function it is function scoped. 

To understand this further, look at the example below.


    var beyonce = "Hi, I'm Beyonce!"; // Globally Scoped
    
    function onStage() {
      beyonce = “I am... Sasha Fierce”;
      var JayZ = "I am out of breath!"; // Functionally Scoped
    }

Here, `beyonce` is globally scoped and it is currently sitting outside the function. `JayZ` is function scoped and it sits inside the function. So, if we do something like this:



    var beyonce = "Hi, I'm Beyonce!";
    
    function onStage() {
      beyonce = “I am... Sasha Fierce”;
      var JayZ = "I am out of breath!";
    }
    console.log(JayZ); // error: JayZ is not defined
    console.log(beyonce); // Hi, I'm Beyonce!

We will get an error because `JayZ` is not available outside the function and also `JayZ` has no business being out of breath off stage. Keep up Jay Z, geesh! `JayZ` would be available only when the `onStage()` function is called.

As you can see within the above variable, `var` can be re-declared and updated.

That means we can do something like this:


    var beyonce = "Hi, I'm Beyonce Knowles.";
    var beyonce = "Hi, I'm Beyonce Carter.";

or:

    var beyonce = "Hi, I'm Beyonce Knowles.";
    beyonce = "Hi, I'm Beyonce Carter.";

For JavaScript, this throws no error. However, for the programmer this can be problematic. We expect `beyonce` to equal `Hi, I``'``m Beyonce Knowles.` but later in our JavaScript code, we redefined it and JavaScript said nothing! This is can unintended side-effects and we should be very careful when using `var` to declare variables.

This is why the `let` and `const` variable is an important addition to our JavaScript arsenal!
