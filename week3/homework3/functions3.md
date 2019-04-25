## Exercise 1

```js
function a_word(_1, _2, _3, _4) { 
  
  function tour(_a, _b, _c, _d) {
    return _b + _a + _c + _d;
  }
  var word = tour("o","t","u","r");

  var result = word;
  return result;
}
const return_val = a_word("o", "t", "u", "r");
console.assert(return_val === 'tour', "wu-1: return_val === " + return_val);
```
---

## Exercise 2

```js
function a_word(_1, _2, _3, _4) { 
  
  function tour(_a, _b, _c, _d) {
    return _c + _a + _d + _b;
  }
  var word = tour("o","r","t","u");

  var result = word;
  return result;
}
const return_val = a_word("u", "t","o","r");
console.assert(return_val === 'tour', "wu-2: return_val === " + return_val);
```
---

## Exercise 1

```js
function eat(_x, _y, _z) {
    return _x + _y + _z;
  }
  var word_1 = eat("e","a","t");

  function ate(_x, _y, _z) {
    return _x + _y + _z;
  }
  var word_2 = ate("a","t","e");

  function tea(_x, _y, _z) {
    return _x + _y + _z;
  }
  var word_3 = tea("t","e","a");

  var result = word_1 + " " + word_2 + " " + word_3;
  return result;
}
const return_val = sentence("a", "e", "t");
console.assert(return_val === 'eat ate tea', "1: return_val === " + return_val);
```
---

## Exercise 2

```js
function eat(_x, _y, _z) {
    return _z + _y + _x;
  }
  var word_1 = eat("t","a","e");

  function ate(_x, _y, _z) {
    return _y + _x + _z;
  }
  var word_2 = ate("t","a","e");

  function tea(_x, _y, _z) {
    return _x + _z + _y;
  }
  var word_3 = tea("t","a","e");

  var result = word_1 + " " + word_2 + " " + word_3;
  return result;
}
const return_val = sentence("a", "e", "t");
console.assert(return_val === 'eat ate tea', "2: return_val === " + return_val);
```
---

## Exercise 3

```js
function sentence(_1, _2, _3, _4, _5) { 

  function space(_v, _w, _x, _y, _z) {
    return _v + _w + _x + _y + _z;
  }
  var word_1 = space(_1, _2, _3, _4, _5);

  function capes(_v, _w, _x, _y, _z) {
    return _v + _w + _x + _y + _z;
  }
  var word_2 = capes(_4, _3, _2, _5, _1);

  var result = word_1 + " " + word_2;
  return result;
}
const return_val = sentence("s", "p", "a", "c", "e");
console.assert(return_val === 'space capes', "3: return_val === " + return_val);
---
## Exercise 4

```js
function sentence(_1, _2, _3, _4, _5) { 

  function space(_v, _w, _x, _y, _z) {
    return _v + _w + _x + _y + _z;
  }
  var word_1 = space(_3, _4, _1, _5, _2);

  function capes(_v, _w, _x, _y, _z) {
    return _v + _w + _x + _y + _z;
  }
  var word_2 = capes(_5,_1,_4,_2,_3);

  var result = word_1 + " " + word_2;
  return result;
}
const return_val = sentence("a", "e", "s", "p", "c");
console.assert(return_val === 'space capes', "4: return_val === " + return_val);
```
---

## Exercise 5

```js
function sentence(_1, _2, _3, _4, _5) { 

  function cruel(_v, _w, _x, _y, _z) {
    return _v + _w + _x + _y + _z;
  }
  var word_1 = cruel(_3, _1, _4, _5, _2);

  function ulcer(_v, _w, _x, _y, _z) {
    return _v + _w + _x + _y + _z;
  }
  var word_2 = ulcer(_4,_2,_3,_5,_1);

  var result = word_1 + " " + word_2;
  return result;
}
const return_val = sentence("r","l","c","u","e");
console.assert(return_val === 'cruel ulcer', "5: return_val === " + return_val);
```
---

## Exercise 6

```js
function sentence(_1, _2, _3, _4, _5) { 

  function cruel(_v, _w, _x, _y, _z) {
    return _v + _w + _x + _y + _z;
  }
  var word_1 = cruel(_4,_5,_3,_1,_2);

  function ulcer(_v, _w, _x, _y, _z) {
    return _v + _w + _x + _y + _z;
  }
  var word_2 = ulcer(_3,_2,_4,_1,_5);

  var result = word_1 + " " + word_2;
  return result;
}
const return_val = sentence("e", "l", "u", "c", "r");
console.assert(return_val === 'cruel ulcer', "6: return_val === " + return_val);
```
---

## Exercise 7

```js
function sentence(_1, _2, _3, _4, _5) { 

  function cruel(_v, _w, _x, _y, _z) {
    return _x + _z + _w + _v + _y;
  }
  var word_1 = cruel(_1,_3,_4,_2,_5);

  function ulcer(_v, _w, _x, _y, _z) {
    return _z + _w + _y + _x + _v;
  }
  var word_2 = ulcer(_5,_2,_1,_4,_3);

  var result = word_1 + " " + word_2;
  return result;
}
const return_val = sentence("e", "l", "u", "c", "r");
console.assert(return_val === 'cruel ulcer', "7: return_val === " + return_val);
```
---

