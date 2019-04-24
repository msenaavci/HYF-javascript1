## Exercise 1

```js
function turtle(_1, _2, _3) {
  var result = "";
  var the_start = "tur";
  result = the_start + _1 + _2 + _3;
  return result;
}
const return_val = turtle("t", "l", "e");
console.assert(return_val === 'turtle', "2: return_val === " + return_val);
```
---

## Exercise 2

```js
function turtle(_1, _2) {
  var result = "";
  var the_start = "tu";
  var the_end = "le";
  result = the_start + _1 + _2 + the_end;
  return result;
}
const return_val = turtle("r", "t");
console.assert(return_val === 'turtle', "3: return_val === " + return_val);
```
---

## Exercise 3

```js
function turtle(_1, _2) {
  var result = "t" + _1 + "r" + _2;
  return result;
}
const return_val = turtle("u", "tle");
console.assert(return_val === 'turtle', "4: return_val === " + return_val)
```
---

## Exercise 4

```js
function turtle(_1, _2, _3) {
  var result = "t" + _2 + "r" + _1 + _3;
  return result;
}
const return_val_1 = turtle("t", "u", "le");
console.assert(return_val_1 === 'turtle', "5: return_val_1 === " + return_val_1);

const return_val_2 = turtle("t", "u", "le");
console.assert(return_val_2 === 'turtle', "5: return_val_2 === " + return_val_2);
```
---

## Exercise 5

```js
function turtle(_1, _2, _3) {
  var result = _1 + _2 + _3;
  return result;
}
const return_val_1 = turtle("tu","r","tle");
console.assert(return_val_1 === 'turtle', "6: return_val_1 === " + return_val_1);

const return_val_2 = turtle("t","ur","tle");
console.assert(return_val_2 === 'turtle', "6: return_val_2 === " + return_val_2);

const return_val_3 = turtle("tur","t","le");
console.assert(return_val_3 === 'turtle', "6: return_val_3 === " + return_val_3);

const return_val_4 = turtle("tu","rt","le");
console.assert(return_val_4 === 'turtle', "6: return_val_4 === " + return_val_4);

const return_val_5 = turtle("tur","tl","e");
console.assert(return_val_5 === 'turtle', "6: return_val_5 === " + return_val_5);

const return_val_6 = turtle("t","urt","le");
console.assert(return_val_6 === 'turtle', "6: return_val_6 === " + return_val_6);
```
---

## Exercise 6

```js
function turtle(_1, _2, _3, _4, _5) {
  var result = _4 + _2 + _5 + _4 + _1 + _3;
  return result;
}
const return_val = turtle("l","u","e","t","r");
console.assert(return_val === 'turtle', "7: return_val === " + return_val);
```
---


## Exercise 7

```js
function turtle(_1, _2, _3, _4, _5) {
  var result = _2 + _1 + _4 + _2 + "l" + _3;
  return result;
}
const return_val = turtle("u","t","e","r");
console.assert(return_val === 'turtle', "7: return_val === " + return_val);
```
---

## Exercise 8

```js
function turtle(_1, _2, _3, _4, _5) {
  _4 = _2;
  _1 = _3;
  var result = _4 + "u" + _1 + _4 + _5 + "e";
  return result;
}
const return_val = turtle("r","t","r","t","l");
console.assert(return_val === 'turtle', "9: return_val === " + return_val);
```
---

## Exercise 9

```js
function turtle(_1, _2, _3, _4, _5) {
  var _ = _4;
  _4 = _2;
  _1 = _3;
  _3 = _;
  var result = _4 + "u" + _1 + _4 + _3 + "e";
  return result;
}
const return_val = turtle("","t","r","l");
console.assert(return_val === 'turtle', "9: return_val === " + return_val);
```
---

