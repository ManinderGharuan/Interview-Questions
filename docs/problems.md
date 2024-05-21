## Write a program to print matrix

```js
1 2 3
4 5 6
7 8 9
```

## Write a program to print matrix

```js
1 5 9
2 6 10
3 7 11
4 8 12
```

## Write a function that returns boolean 'true'/'false' based on whether or not the argument passed to it is an Armstrong number.

```js
/* Definition of an Armstrong Number:
A number where the sum of its own digits raised to the power of number of digits (n) is equal to same number

Example : n = 153
The number of digits is 3 (n = 3) here.
So, the sum of digits raised to the power of 3=
1^3 + 5^3 + 3^3 = 1 + 125 + 27 = 153
sum is equal to input number 153.
So, in this case the function should return true*/
```

## Console output of code

```js linenums="1"
let a = true;
setTimeout( () => a = false, 100);
while(a) { console.log(a) }
console.log(“script ended”);
```

## Complete the function

```js linenums="1"
/*
ArrayAdditionI(arr) take the array of numbers stored in arr and return the string true if any combination of numbers in the array can be added up to equal the largest number in the array, otherwise return the string false.

For example:
if arr contains [4, 6, 23, 10, 1, 3] the output should return true because 4 + 6 + 10 + 3 = 23.
The array will not be empty, will not contain all the same elements, and may contain negative numbers
*/

function ArrayAdditionI(arr) {
  // Write code here...
}

console.log("-----");
console.log(ArrayAdditionI([1, 2, 3, 5, 4])); // ==> true
console.log(ArrayAdditionI([21, 10, 12, 9, 2])); // ==> true
console.log(ArrayAdditionI([4, 6, 23, 10, 1, 3])); // ===> true
console.log(ArrayAdditionI([5, 7, 16, 1, 2])); // ===> false
console.log(ArrayAdditionI([3, 5, -1, 8, 12])); // ===> true
```

## Node JS Age Counting Challenge

```js
// As per response of get call count the total number of ages who has age value above or equal to 50.

const https = require("https");
https.get("https://coderbyte.com/api/challenges/json/age-counting", (resp) => {
  // Write code here...
});
```

## Write a program to remove duplicates from an array?

```js
const removeDuplicates = (array) => {
  // Write code here...
};

removeDuplicates([1, 2, 1, 3, 4, 2, 2, 1, 5, 6]);
```
