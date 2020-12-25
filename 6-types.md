# Types

## Strings
1. Single Quotes
```JavaScript
const design = 'Heroku Design Team';
```

Adding an additional `'` by escaping using `/`
```JavaScript
const sentence = 'She/'s our manager.'
```

2. Double Qoutes
```JavaScript
const product = "Heroku Product Design";
```
3. Backticks
```JavaScript
const development = `Heroku Frontend Design`;
```


## Numbers

Unlike other programming languages, JavaScript only has one type of number.

Although we have floats, whole numbers, etc. are all the `typeOf` number.

```JavaScript
const age = 10.5;
typeof age; // number
```
### [Arithmetic Operators](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Math#Arithmetic_operators)
There is multiplication, addition, subtraction, division, exponents and modulo a.k.a remainder.

|  Operator  |      Name      |                                                                         Purpose                                                                        |  Example  |
|------------|:--------------:|-------------------------------------------------------------------------------------------------------------------------------------------------------:|----------:|
|     +      |    Addition    |                                                                   Adds two numbers together.                                                           |   6 + 9   |
|     -      |   Subtraction  |                                                  Subtraction	Subtracts the right number from the left.                                                |  20 - 15  |
|     *      | Multiplication |                                                       Multiplication	Multiplies two numbers together.                                                 |   3 * 7   |
|     /      |     Division   |                                                             Divides the left number by the right.                                                      |  10 / 5   |
|     %      |     Modulo     |         Returns the remainder left over after you've divided the left number into a number of integer portions equal to the right number.              |   8 % 3   |
|     **     |    Exponent    | Raises a base number to the exponent power, that is, the base number multiplied by itself, exponent times. It was first Introduced in EcmaScript 2016. |  5 ** 2   |
    
### Most popular Math helpers

```JavaScript
Math.round(20.5); // 21
Math.floor(30.6); // 30
Math.ceil(100.2); // 101
Math.random(); // 0.5037997751582997
```

More Math helpers [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math).

Let's say we have 3 children and 25 pieces of oxtails in the pot. How would we split them up evenly so that no kid feels like the other has more?

```JavaScript
const oxtails = 25;
const children = 3;
const eachChildGets = Math.floor(oxtails / children);
const eldersGet = oxtails % children;
console.log(`Each child gets ${eachChildGets} while the elders are left with ${eldersGet}`); // Each child gets 8 while the elders are left with 1
```

JavaScript is a bit weird in this particular case.

```Javascript
0.1 + 0.2; // 0.30000000000000004
```

If you visit [https://0.30000000000000004.com/](https://0.30000000000000004.com/), you will see exactly how this works.

## Objects

JavaScript objects are containers for named values called properties or methods. Objects are variables too. But objects can contain many values.

The values are written as `name: value` pairs (name and value separated by a colon).

This code assigns many values (name, stageName, Children) to a variable named theeStallionProfile:

```JavaScript
    const theeStallionProfile = {
        name: "Megan Pette",
        stageName: "Megan Thee Stallion",
        children: {
          human: 0,
          pets: {
            name: "4oe",
            breed: "French Bulldog"
        }
      }
    }
```

To accessproperties, we use the dot notation.
```Javascript
theeStallionProfile.name // Megan Pete
```

## Null and Undefined
There are two ways to express nothing in JavaScript: null and undefined. 

Undefined comes about when you try to access a variable that is created but not set. (No value)

```JavaScript
    let dog;
    console.log(dog); // undefined
```            
Null comes about when your value is set to null.

```JavaScript
    let dog = null;
    console.log(dog); // null
```



## Booleans and Equality

Boolean is something either true or false.

```JavaScript
let goodWashAndGo = false;
let needHairDone = true;
```

What is the difference between double equals `==` and triple equals `===`?
`=` to set a value
`==` Checks value and not type
`===` Checks the value of the first and second to make sure the values are the same && check the type!

```JavaScript
"10" == 10 // true
"10" === 10 // false
```

## Symbols

