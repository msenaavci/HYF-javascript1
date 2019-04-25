## Exercise 1

```js
function copy_array(arr) {
  // write this using JSON.stringify & .parse
var array_strified = JSON.stringify(arr);
    var array_copy = JSON.parse(array_strified);
    return array_copy;
 }

const array = ['a', 'b'];
const by_copy = copy_array(array);

console.assert(array[0] === by_copy[0]);
console.assert(array[1] === by_copy[1]);
console.assert(array !== by_copy);

```
---

## Exercise 2

```js
function start_new_array(arr) {
  // write this by building a new array from scratch
 var new_arr = [];
    for (var i =0; i <= arr.length - 1; i++) {
      new_arr.push(arr[i]);
    }
    return new_arr;
  }

const array = ['a', 'b'];
const by_new_start = start_new_array(array);

console.assert(array[0] === by_new_start[0]);
console.assert(array[1] === by_new_start[1]);
console.assert(array !== by_new_start);
```
---

## Exercise 3

```js
function copy_object(obj) {
  // write this using JSON.stringify & .parse
var object_strified = JSON.stringify(obj);
    var copy_object = JSON.parse(object_strified);
    return copy_object;
}

const object = {a: 1, b: 2};
const by_copy = copy_object(object);

console.assert(object.a === by_copy.a);
console.assert(object['b'] === by_copy['b']);
console.assert(object !== by_copy);
```
---

## Exercise 4

```js
function start_new_object(obj) {
  // write this by building a new object from scratch
var new_obj = {};
    for(let key in obj){
      new_obj[key] = obj[key];
    }
    return new_obj;
  }

const object = {a: 1, b: 2};
const by_new_start = start_new_object(object);

console.assert(object.a === by_new_start.a);
console.assert(object['b'] === by_new_start['b']);
console.assert(object !== by_new_start);
```
---
