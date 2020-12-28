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
  console.group('Start doing things');
  console.warn('Warn me about things');
  console.error('Watch out for all errors');
  console.groupEnd();
}

console.info('See some info'); // Info mark
console.error('See an error'); // Red Error
console.warn('See a warning'); // Yellow warning
console.table(people); // Puts object in a table
console.count(); // Run the doctorize function and see how it maintains how many time a particular function was run.
console.group(); // Running a group of console methods
```


