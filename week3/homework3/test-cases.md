## Strict equality


```js 
{
  const test_cases = [
      {name: '3, 3', args: [3, 3], expected: true},
      {name: '3, "3"', args: [3, "3"], expected: false},
      {name: 'true, 1', args: [true, 1], expected: false},
      {name: 'false, 0', args: [false, 0], expected: false},
      {name: 'true, 0', args: [true, 0], expected: false},
      {name: 'null, 0', args: [null, 0], expected: false},
      {name: 'true, "true"', args: [true, true], expected: false},
      {name: 'false, false', args: [false, false], expected: true},
      {name: 'undefined, 0', args: [undefined, 0], expected: false},
      {name: '0, 0', args: [0, 0], expected: true},
      
      /* write 8 more passing test cases */
    ];
  function strict_equality(a, b) {
    return a === b;
  }
  run_tests(strict_equality, test_cases);
}
```
---

## typeof

```js 
const test_cases = [
      {name: 'null', args: [null], expected: 'object'},
      {name: 'undefined', args: [undefined], expected: 'undefined'},
      {name: '0', args: [0], expected: 'number'},
      {name: 'true', args: [true], expected: 'boolean'},
      {name: 'false', args: [false], expected: 'boolean'},
      {name: 'NaN', args: [NaN], expected: 'number'},
      {name: '"ask"', args: ["ask"], expected: 'string'}
      {name: '"1"', args: ["1"], expected: 'string'}
      
      /* write 6 more passing test cases */
    ];
  function _typeof(a) {
    return typeof a;
  }
  run_tests(_typeof, test_cases);
}
```
---


## Boolean

```js 
{
  const test_cases = [
      {name: 'null', args: [null], expected: false},
      {name: 'undefined', args: [undefined], expected: false},
      {name: '0', args: [0], expected: false},
      {name: '"0"', args: ["0"], expected: true},
      {name: '1', args: [1], expected: true},
      {name: '"false"', args: ["false"], expected: true},
      {name: 'NaN', args: [NaN], expected: false},
      {name: '""', args: [""], expected: false},
      {name: 'Infinity', args: [Infinity], expected: true},
      {name: 'true', args: [true], expected: true},
      {name: '-0', args: [-0], expected: false},
      {name: '" "', args: [" "], expected: true},
      /* write 10 more passing test cases */
    ];
  function to_boolean(a) {
    return Boolean(a);
  }
  run_tests(to_boolean, test_cases);
}
```
---


## Number

```js 
{
  const test_cases = [
      {name: 'null', args: [null], expected: 0},
      {name: 'undefined', args: [undefined], expected: NaN},
      {name: 'NaN', args: [NaN], expected:1},
      {name: '"2"', args: ["2"], expected: NaN},
      {name: '2', args: [2], expected: 2},      
      {name: '"2px"', args: ["2px"], expected: NaN},
      {name: 'true', args: [true], expected: NaN},

      /* write 10 more passing test cases */
    ];
  function to_number(a) {
    return Number(a);
  }
  run_tests(to_number, test_cases);
}

```
---

## Or

```js 
{
  const test_cases = [
      {name: '1, 1', args: [1, 1], expected: 1},
      {name: '0, 1', args: [0, 1], expected: 1},
      {name: '1, 0', args: [1, 0], expected: 1},
      {name: '0, 0', args: [0, 0], expected: 0},
      {name: 'true, false', args: [true, false], expected: true},
      {name: 'false,true', args: [false,true], expected: true},
      {name: 'false,false', args: [false,false], expected: false},
      {name: 'true,true', args: [true,true], expected: true},
      
      /* write 10 more passing test cases */
    ];
  function or(a, b) {
    return a || b;
  }
  run_tests(or, test_cases);
}
```
---


## and

```js 
{
  const test_cases = [
      {name: '1, 1', args: [1, 1], expected: 1},
      {name: '0, 1', args: [0, 1], expected: 0},
      {name: '1, 0', args: [1, 0], expected: 0},
      {name: '0, 0', args: [0, 0], expected: 0},
      {name: 'true, true', args: [true, true], expected: true},
      {name: 'false, true', args: [false, true], expected: false},
      {name: 'false, false', args: [false, false], expected: false},
      {name: 'true, false', args: [true, false], expected: false},
      {name: 'null, false', args: [null, false], expected: null},
      {name: '2, 3', args: [2, 3], expected: 3},
      {name: '3, 2', args: [3, 2], expected: 2},
      
      
      
    ];
  function and(a, b) {
    return a && b;
  }
  run_tests(and, test_cases);
}
```
---


## not

```js 
{
  const test_cases = [
      {name: '1', args: [1], expected: false},
      {name: '0', args: [0], expected: true},
      {name: 'true', args: [true], expected: false},
      {name: 'false', args: [false], expected: true},
      {name: 'NaN', args: [NaN], expected: true},
      {name: '2', args: [2], expected: false}, 
      {name: '"ask"', args: ["ask"], expected: false},
      {name: 'Infinity', args: [Infinity], expected: false},
      {name: '-Infinity', args: [-Infinity], expected: false},
      {name: '', args: [], expected: true},
      {name: ' ', args: [ ], expected: false},
      {name: 'undefined', args: [undefined], expected: true},
      
      
      /* write 10 more passing test cases */
    ];
  function not(a) {
    return !a;
  }
  run_tests(not, test_cases);
}
```
---


## ternary

```js 
{
  const test_cases = [
      {name: '1, "x", "y"', args: [1, 'x', 'y'], expected: 'x'},
      {name: '0, "x", "y"', args: [0, 'x', 'y'], expected: 'y'},
      {name: '0, 1, "y"', args: [0, 1, 'y'], expected: 'y'}, 
       {name: '1, 0, "y"', args: [1, 0, 'y'], expected: 'y'},
       {name: '1, 1, "y"', args: [1, 1, 'y'], expected: 1},
       {name: 'null, 0, 1', args: [null, 0, 1], expected: 1},
       {name: '0, null, 3', args: [0, null, 3], expected: 3},
       {name: '"", 0, "y"', args: ["", 0, 'y'], expected: 'y'},
       {name: '" ", 1, "y"', args: [" ", 1, 'y'], expected: 1},
       {name: '"e", "2", "y"', args: ["e", "2", 'y'], expected: "2"},
      /* write 10 more passing test cases */
    ];
  function ternary(a, b, c) {
    return a ? b : c ;
  }
  run_tests(ternary, test_cases);
}
```
---

##  greater than
```js 
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: true},
      {name: 'true, 1', args: [true, 1], expected: false},
      {name: 'false, 0', args: [false, 0], expected: false},
      {name: 'false, 1', args: [false, 1], expected: false},
      /* write 4 more passing test cases with only strings */
      {name: '"1","2"', args: ["1", "2"], expected: false},
      {name: '"gel", "go"', args: ["gel", "go"], expected: false},
      {name: '"go", "gel"', args: ["go", "gel"], expected: true},
      {name: '"2", "10"', args: ["2", "10"], expected: true},
      /* write 6 more passing test cases without NaN values */
      {name: 'null, 0', args: [null, 0], expected: false},
      {name: 'null, undefined', args: [null, undefined], expected: false},
      {name: '2, 1', args: [2, 1], expected: true},
      {name: '2, 10', args: [2, 10], expected: false},
      {name: '"", 1', args: ["", 1], expected: false},
      {name: '" ", ""', args: [" ", ""], expected: true},
      /* write 4 more passing test cases with NaN values */
      {name: 'NaN, 1', args: [NaN, 1], expected: false},
      {name: '1, NaN', args: [1, NaN], expected: true},
      {name: '3, NaN', args: [3, NaN], expected: true},
      {name: 'NaN, undefined', args: [NaN, undefined], expected: false},
    ];
  function greater_than(a, b) {
    return a > b;
  }
  run_tests(greater_than, test_cases);
}
```
---

## less than

```js 
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: false},
      {name: 'true, 1', args: [true, 1], expected: false},
      {name: 'false, 0', args: [false, 0], expected: false},
      {name: 'false, 1', args: [false, 1], expected: true},
      {name: '"1","2"', args: ["1", "2"], expected: true},
      {name: '"gel", "go"', args: ["gel", "go"], expected: true},
      {name: '"go", "gel"', args: ["go", "gel"], expected: false},
      {name: '"2", "10"', args: ["2", "10"], expected: false},
      /* write 6 more passing test cases without NaN values */
      {name: 'null, 0', args: [null, 0], expected: false},
      {name: 'null, undefined', args: [null, undefined], expected: false},
      {name: '2, 1', args: [2, 1], expected: false},
      {name: '2, 10', args: [2, 10], expected: true},
      {name: '"", 1', args: ["", 1], expected: true},
      {name: '" ", ""', args: [" ", ""], expected: false},
      /* write 4 more passing test cases with NaN values */
      {name: 'NaN, 1', args: [NaN, 1], expected: true},
      {name: '1, NaN', args: [1, NaN], expected: false},
      {name: '3, NaN', args: [3, NaN], expected: false},
      {name: 'NaN, undefined', args: [NaN, undefined], expected: false},
    ];
  function less_than(a, b) {
    return a < b;
  }
  run_tests(less_than, test_cases);
}
```
---

## subtraction

```js 
{
  const test_cases = [
      {name: 'true, 0', args: [true, 0], expected: 1},
      {name: 'true, 1', args: [true, 1], expected: 0},
      {name: 'false, 0', args: [false, 0], expected: 0},
      {name: 'false, 1', args: [false, 1], expected: -1},
      /* write 5 more passing test cases without NaN values*/
      {name: '5, 0', args: [5, 0], expected: 5},
      {name: 'true, "0"', args: [true, "0"], expected: 0},
      {name: '"a", "b"', args: ["a", "b"], expected: 0},
    
      
      /* write 5 more passing test cases with NaN values*/
    ];
  function subtraction(a, b) {
    return a - b;
  }
  run_tests(subtraction, test_cases);
}
```
---
