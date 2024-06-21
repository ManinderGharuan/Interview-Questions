## Javascript

### What is functional programming?

#### First class functions?

- Functions that treaded as other variable, passed as an argument or return by another function.

#### What is a pure function?

- Pure functions are the functions which will return same output for the same arguments passed to the function.
- This is not have any side effects that modify
  - Global variables
  - Writing to files
  - Printing to the console
  - Making network calls
- We can predict the output of pure function.
- Pure functions are easier to test.

```js linenums="1"
// Pure function
const add = (x, y) => x + y;

add(2, 4); // 6
add(2, 4); // 6

// Impure function
let x = 2;

const add = (y) => {
  x += y;
};

add(4); // x === 6 (the first time)
add(4); // x === 10 (since the global x was incremented in the previous call)
```

#### What are higher order functions?

- Function that accepts functions as parameters and/or returns a function.
- Callback functions can be passed as a parameter in higher order function.
- It is usefull to create reusable code.

```js linenums="1"
const radius = [1, 2, 3];

// logic to clculate area
const area = function (radius) {
  return Math.PI * radius * radius;
};

// logic to calculate diameter
const diameter = function (radius) {
  return 2 * radius;
};

// a reusable function to calculate area, diameter, etc
const calculate = function (radius, logic) {
  const output = [];
  for (let i = 0; i < radius.length; i++) {
    output.push(logic(radius[i]));
  }
  return output;
};

console.log(calculate(radius, area));
console.log(calculate(radius, diameter));

// logic to calculate circumeference
const circumeference = function (radius) {
  return 2 * Math.PI * radius;
};

console.log(calculate(radius, circumeference));
```

### Difference between regular function and arrow function?

#### Arrow functions

- Simple and shorter way to create functions.
- Cannot access before they are initialised.
- Not have their own ==this== context. Capture this value from his parent in which arrow function created.
- Cannot used as contructor.

#### Regular functions

- Hoisted to the top. You can access and call them even before they are declared.
- Have their own ==this== context.
- Can create new instance using ==new== keyword.

### What is difference between map() and forEach()?

- ap method will return a new array with transformed values.
- forEach method does not return a new array.

### What are the differences between call(), apply() and bind()?

- Call and Apply method will invokes function immediately with given this value.
- Call method allow us to pass arguments with comma separator (one by one).
- Apply method allow us to pass the arguments as an array.
- Bind method will return a new function with given this value and arguments which can be invoked later.

### What is spread operator?

- Spread operator is used to expand the elements of an array into individual elements.

```js linenums="1"
// Concatenation arrays
let x = [1, 2];
let y = [3, 4];

let z = [...x, ...y]; // [1, 2, 3, 4]

// Copy arrays of objects
let a = [...x]; // [1, 2]

let obj = { x: 1, y: 2 };

let obj_copy = { ...obj }; // { x: 1, y: 2 }

// Pass array of values as function arguments
function example(arg1, arg2) {
  console.log(arg1, arg2);
}

createExample(...a);
```

### What is rest operator?

- Rest operator is used to pass multiple elements into single array or object.
- This is used when we don't know how many parameters a function may receive and you can capture all of them as an array.

```js
function example(...args) {
  console.log(args);
}

example(1, 2, 3, 4); // [1, 2, 3, 4]
```

### What is destructuring?

- It is introduced in es6.
- It allows us to assign the object properties and array values to variables.

```js linenums="1"
const user = {
    "age": 10,
    "name": "Maninder"
}

const { age, name as firstName } = user;
console.log(age, firstName); // 10, Maninder

const [a, b] = [1, 2];
console.log(a, b); // 1, 2
```

### What is a closure?

- Closure is a function which will return another function along with outer function environment.

```js linenums="1"
function Outer() {
  var a = 10;
  function Inner() {
    console.log(a);
  }
  return Inner;
}

var Close = Outer();
Close();
```

## OOPS

###
