# Debugging

### Console Methods
```JavaScript
const people = [
  { name: 'Lenora', cool: true, country: 'United States' },
  { name: 'Ireland', cool: true, country: 'Ireland' },
  { name: 'Abeni', cool: false, country: 'Nigeria' },
];

function doctorize(name) {
 console.count(`Running doctorize for ${name}`);
 return `Dr. ${name}`;
}

function doAlotOfStuff() {
  console.groupCollapsed('Start doing things');
  console.warn('Warn me about things');
  console.error('Watch out for all errors');
  console.log('Done!');
  console.groupEnd();
}

console.info('See some info'); // Info mark
console.error('See an error'); // Red Error
console.warn('See a warning'); // Yellow warning
console.table(people); // Puts object in a table
console.count(); // Run the doctorize function and see how it maintains how many time a particular function was run.
console.group(); // Running a group of console methods
```


## Call Stack or Stack Tracing

```JavaScript
function doctorize(name) {
  return `Dr. ${name}`;
}

function greet(name) {
  doesntExist(); // Cause an error
  return `Hello ${name}`;
}

function go() {
  const name = doctorize(greet('Wes'));
  console.log(name);
}
```

<img src="stack-tracing.png" />

If you want to know what went wrong in your code, you have to get good at reading the call stack.

Let's read the stack trace above:

The error happened at `greet` in the file `debugging-FINISH.js` on line 32.

Well, who called `greet`?

Let's keep reading. `go` called `greet` in the file `debugging-FINISH.js` on line 37.

Then it says `<anonymous>:1:1`. What does that mean?

Just means I ran it from Google Dev Tools Console. However, if I run it in the code, the error would look like this.

<img src="stack-tracing-2.png" />



