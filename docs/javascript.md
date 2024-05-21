## Javascript

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

- Closure is a funcation which will return another function along with outer function environment.

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
