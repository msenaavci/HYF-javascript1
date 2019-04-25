## Exercise 1


```js
* your function must pass all of these tests
  
  null, undefined            ->   true
  undefined, null            ->   true
  null, null                 ->   true
  undefined, undefined       ->   true
  null, (anything else)      ->   false
  undefined, (anything else) ->   false
  
  true, false                ->    false
  false, false               ->    true
  3, 3                       ->    true
  3.0, 3                     ->    true
  +0, -0                     ->    true
  "\t", '\t'                 ->    true
  -3, +3                     ->    false
       
  3, "3"                     ->    true
  "3", 3                     ->    true
  "3, "3"                    ->    true
  true, 1                    ->    true
  false, 0                   ->    true
  false, ""                  ->    true
  0, ""                      ->    true
  "e", true                  ->    false
  undefined, ""              ->    false
*/

const a = false, b = false;
const native = a == b;
const replication = loose_equality(a, b);

console.assert(native === replication, "replication === " + replication);

function loose_equality(x, y) { 
  // if both a and b are null or undefined, return true
  // if only one is null or undefined, return false
var x_ = x === null || x === undefined;
var y_ = y === null || y === undefined;
if(x || y) {
return x && y; 
}
  // if both arguments are the same type (num, string, or bool)
  //  compare them with === and return the result
const type_x = typeof_x;
const type_y = typeof_y;
var x_y = type_x === type_y
if(x_y) {
  return x === y;
}
  // if both are not the same type
  //  make sure both are type 'number'
  //  compare them with ===, and return the result
var x_num = Number(x);
var y_num = Number(y);
if(x_num===y_num){ 
  return x_num === y_num;
}
}

```
---
