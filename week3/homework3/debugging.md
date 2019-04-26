## Exercise 1

```js 
let a = 5;
let b = 1;
a++;
console.log(a);

let sumAB = a + b;
console.log(sumAB);
```
---


## Exercise 2

```js 
// Open your browser console
let outputTwo = "This will print to the browser console 2 times";
// Use console.log() to print the outputTwo variable
console.log(outputTwo);

let outputOne = "Try to get this to log only once to the browser console";
// Use console.clear() in the next line to print the outputOne only once
console.clear();

// Use console.log() to print the outputOne variable
console.log(outputOne);

```
---

## Exercise 3

```js 
let seven = 7;
let three = "3";
console.log(seven + three);
// Add your code below this line
console.log(typeof seven);
console.log(typeof three);

```
---

## Exercise 4

```js 
let receivables = 10;
let payables = 8;
let netWorkingCapital = receivables - payables;
console.log(`Net working capital is: ${netWorkingCapital}`);

```
---

## Exercise 5

```js 
let myArray = [1, 2, 3];
let arraySum = myArray.reduce((previous, current) =>  previous + current);
console.log(`Sum of array values is: ${arraySum}`);

```
---

## Exercise 6

```js 

let innerHtml = "<p>Click here to <a href='#Home'>return home</a></p>";
console.log(innerHtml);
```
---

## Exercise 7

```js 
let x = 7;
let y = 9;
let result = "to come";

if(x == y) {
  result = "Equal!";
} else {
  result = "Not equal!";
}

console.log(result);

```
---


## Exercise 8

```js 
function getNine() {
  let x = 6;
  let y = 3;
  return x + y;
}

let result = getNine();
console.log(result);

```
---

## Exercise 9

```js 

function raiseToPower(b, e) {
  return Math.pow(b, e);
}

let base = 2;
let exp = 3;
let power = raiseToPower(base, exp);
console.log(power);
```
---


## Exercise 10

```js 
function countToFive() {
  let firstFive = "12345";
  let len = firstFive.length;
  // Fix the line below
  for (let i = 0; i < len; i++) {
  // Do not alter code below this line
    console.log(firstFive[i]);
  }
}

countToFive();

```
---

## Exercise 11

```js 
function zeroArray(m, n) {
  // Creates a 2-D array with m rows and n columns of zeroes
  let newArray = [];
  let row = [];
  for (let i = 0; i < m; i++) {
    // Adds the m-th row into newArray
    
    for (let j = 0; j < n; j++) {
      // Pushes n zeroes into the current row to create the columns
      row.push(0);
    }
    // Pushes the current row, which now has n zeroes in it, to the array
    newArray.push(row);
  row  = [];
  }
  return newArray;
  
}

let matrix = zeroArray(3, 2);
console.log(matrix);

```
---

## Exercise 12

```js 
function myFunc() {
  for (let i = 1; i <= 4; i += 2) {
    console.log("Still going!");
  }
}

```
---
