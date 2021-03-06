# What is `use strict`

According to [W3Schools](https://www.w3schools.com/js/js_strict.asp),

The `use strict` directive was new in ECMAScript version 5.

It is not a statement, but a literal expression, ignored by earlier versions of JavaScript.

The purpose of "use strict" is to indicate that the code should be executed in "strict mode".

With strict mode, you can not, for example, use undeclared variables.

<ins>Example</ins>:

Without use strict:
```JavaScript

first = `lenora`;

console.log(first); // Lenora

```
This method is prone to nasty bugs so the use strict method was created to force the developer to catch themselves when they forget to set variables.

Using use strict:

```JavaScript
'use strict'

first = `lenora`;

console.log(first); // ReferenceError: first is not defined

```
