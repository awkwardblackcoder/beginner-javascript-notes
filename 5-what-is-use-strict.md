# What is `use strict`

According to W3Schools

The "use strict" directive was new in ECMAScript version 5.

It is not a statement, but a literal expression, ignored by earlier versions of JavaScript.

The purpose of "use strict" is to indicate that the code should be executed in "strict mode".

With strict mode, you can not, for example, use undeclared variables.

<ins>Example</ins>:

Without use strict:
```JavaScript
<script>
'use strict'

first = `lenora`;

console.log(first); // Lenora

</script>
```


Using use strict:

```JavaScript
<script>
'use strict'

first = `lenora`;

console.log(first); // ReferenceError: first is not defined

</script>
```
